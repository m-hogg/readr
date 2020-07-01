<template>
  <div class="flex">
    <div class="w-3/4">
      <div>
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
