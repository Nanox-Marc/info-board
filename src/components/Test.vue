<template>
      <ul>
        <li v-for="(book, index) in books" :key="index">
          Title: {{ book.title }} ----- Author: {{ book.author }}
        </li>
      </ul>
      *******************************************************
      <ul>
        <li v-for="book in books" :key="book.id">
          Title: {{ book.title }} ----- Author: {{ book.author }}
        </li>
      </ul>

      ******************************************************
      <br>
      <button @click="toggleVisibility">Toggle Visibility</button>
      <p v-if="isVisible">You can see me now!</p>

      *****************************************************

      <br>
      <div :class="{ active: isActive, inactive: !isActive }">This div's class is conditional</div>
      <button @click="toggleActive">Toggle Active</button>


</template>
  
<script> 
export default {
    name: 'Test',
    data() {
        return {
            isVisible: true,
            isActive: true,
            books: [
              { id: 1, title: "asdf", author: "4567"},
              { id: 2, title: "ghjk", author: "1234"},
              { id: 3, title: "qwert", author: "4321"},
              { id: 4, title: "zxcvb", author: "9876"}
            ]
        }
    },
    methods: {
      toggleVisibility() {
        this.isVisible = !this.isVisible;
      },

      toggleActive() {
        this.isActive = !this.isActive;
      }
    }
}
</script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  
</style>
  