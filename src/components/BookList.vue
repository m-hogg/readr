<template>
    <div class="bg-white m-20 overflow-auto rounded-md">
        <table class="table-auto w-full">
            <thead>
                <th v-if="editing" class="border-b px-4 py-2 sticky top-0 bg-white"><input type="checkbox" id="selectAll" v-model="allSelected"></th>
                <th
                    v-for="(header, index) in headers"
                    :key="index"
                    class="border-b px-4 py-2 capitalize sticky top-0 bg-white"
                >
                    {{ header }}
                </th>
            </thead>
            <tbody>
                <template v-for="(book, index) in books">
                    <tr :key="index" class="hover:bg-blue-200" @click="handleRowClick(book)">
                        <td v-if="editing" class="border-t border-b px-4 py-2">
                            <input type="checkbox" v-model="selectedBooks" :value="book.id">
                        </td>
                        <td
                            v-for="(header, index) in headers"
                            :key="index" 
                            class="border-t border-b px-4 py-2"
                        >
                            {{ book[header] }}
                        </td>
                    </tr>
                </template>
            </tbody>
        </table>
    </div>
</template>

<script>
export default {
    name: "BookList",
    props: {
        books: {
            type: Array,
            default: () => []
        },
        headers: {
            type: Array,
            default: () => []
        },
        editing: {
            type: Boolean,
            default: false
        }
    },
    data () {
        return {
            selectedBooks: []
        }
    },
    computed: {
        allSelected: {
            get () {
                return this.books.length === this.selectedBooks.length;
            },
            set (val) {
                this.selectedBooks = val ? this.books.map((book) => (book.id)) : [];
            }
        }
    },
    methods: {
        handleRowClick ({ id }) {
            this.selectedBooks.includes(id) ?
                this.selectedBooks.splice(this.selectedBooks.indexOf(id), 1) :
                this.selectedBooks.push(id);
        }
    }
}
</script>