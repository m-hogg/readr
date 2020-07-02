<template>
  <div class="h-screen flex flex-col">
    <div class="flex h-full">
      <div class="w-3/4 flex flex-col overflow-hidden">
        <book-list
          :books="books"
          :headers="headers"
          :editing="editing"
        />
      </div>
      <div class="w-1/4 flex flex-col py-20 bg-gray-200">
        <button-box />
        <info-box class="mt-10" />
      </div>
    </div>
  </div>
  
</template>

<script>
import BookList from '@/components/BookList.vue';
import ButtonBox from '@/components/ButtonBox.vue';
import InfoBox from '@/components/InfoBox.vue';

export default {
  name: 'Home',
  components: {
    BookList,
    ButtonBox,
    InfoBox
  },
  data() {
    return {
      headers: ['title', 'author'],
      books: [
          { id: 1, title: "Love and Responsibility", author: "JPII" },
          { id: 2, title: "Lord of the Rings", author: "JRR Tolkien" },
          { id: 3, title: "Lord of the Rings", author: "JRR Tolkien" },
          { id: 4, title: "Lord of the Rings", author: "JRR Tolkien" },
          { id: 5, title: "Lord of the Rings", author: "JRR Tolkien" },
          { id: 6, title: "Lord of the Rings", author: "JRR Tolkien" },
          { id: 7, title: "Lord of the Rings", author: "JRR Tolkien" },
          { id: 8, title: "Lord of the Rings", author: "JRR Tolkien" },
          { id: 9, title: "Lord of the Rings", author: "JRR Tolkien" },
          { id: 10, title: "Lord of the Rings", author: "JRR Tolkien" },
          { id: 11, title: "Lord of the Rings", author: "JRR Tolkien" },
          { id: 12, title: "Lord of the Rings", author: "JRR Tolkien" },
          { id: 13, title: "Lord of the Rings", author: "JRR Tolkien" },
          { id: 14, title: "Lord of the Rings", author: "JRR Tolkien" },
          { id: 15, title: "Lord of the Rings", author: "JRR Tolkien" },
          { id: 16, title: "Lord of the Rings", author: "JRR Tolkien" },
          { id: 17, title: "Lord of the Rings", author: "JRR Tolkien" },
          { id: 18, title: "Lord of the Rings", author: "JRR Tolkien" },
          { id: 19, title: "Lord of the Rings", author: "JRR Tolkien" },
          { id: 20, title: "Lord of the Rings", author: "JRR Tolkien" },
          { id: 21, title: "Lord of the Rings", author: "JRR Tolkien" },
          { id: 22, title: "Lord of the Rings", author: "JRR Tolkien" },
          { id: 23, title: "Lord of the Rings", author: "JRR Tolkien" },
          { id: 24, title: "Lord of the Rings", author: "JRR Tolkien" },
          { id: 25, title: "Lord of the Rings", author: "JRR Tolkien" },
          { id: 26, title: "Lord of the Rings", author: "JRR Tolkien" },
          { id: 27, title: "Lord of the Rings", author: "JRR Tolkien" },
          { id: 28, title: "Lord of the Rings", author: "JRR Tolkien" }
      ],
      editing: false
    }
  },
}
</script>
