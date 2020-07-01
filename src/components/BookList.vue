<template>
    <div class="bg-white">
        <div>
            <button class="text-right py-2 px-5 hover:bg-gray-200 focus:outline-none">
                Edit
            </button>
        </div>
        <table class="table-auto w-full">
            <thead>
                <th class="border-t border-b px-4 py-2"><input type="checkbox" id="selectAll" v-model="allSelected"></th>
                <th
                    v-for="(header, index) in headers"
                    :key="index"
                    class="border-t border-b px-4 py-2 capitalize"
                >
                    {{ header }}
                </th>
            </thead>
            <template v-for="(book, index) in books">
                <tr :key="index" class="hover:bg-blue-200" @click="handleRowClick(book)">
                    <td class="border-t border-b px-4 py-2">
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
    </table>
    </div>
</template>

<script>
export default {
    name: "BookList",
    async mounted () {
        // Get the books! And the headers!
    },
    data () {
        return {
            headers: [
                'title',
                'author'
            ],
            books: [
                { id: 1, title: "Love and Responsibility", author: "JPII" },
                { id: 2, title: "Lord of the Rings", author: "JRR Tolkien" }
            ],
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