<template>
  <div class="flex">
    <div class="w-1/4">
      fjkjds
    </div>
    <div class="w-1/2">
      <div class="border-current rounded-lg bg-white mt-5">
        <div class="p-5 mt-5 text-3xl">Reading List</div>
        <book-list />
      </div>  
    </div>
    <div class="w-1/4">
      Coming soon! Info box
    </div>
  </div>
</template>

<script>
import BookList from '@/components/BookList.vue';

export default {
  name: 'Home',
  components: {
    BookList
  },
}
</script>
