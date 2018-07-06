<template>
  <section class="recipes">
    <Recipe
    thumbnail="https://images.theconversation.com/files/180401/original/file-20170731-22175-67v3q2.jpg?ixlib=rb-1.1.0&rect=0%2C589%2C5472%2C2654&q=45&auto=format&w=1356&h=668&fit=crop"
    title="Tasty Hamburger"
    id="1"
    previewText="One of the easiest and tastiest hamburgers around"
    />
    <Recipe
    thumbnail="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQUaAVeXXVawHZryxJ0gIY_4yNv2hTbuZhGZRYQOEQuCCICvsZo"
    title="Tasty Pizaa"
    id="2"
    previewText="One of the easiest and tastiest pizza around"
    />
  </section>
</template>

<script>
import Recipe from '@/components/Recipe'

export default {
  components: {
    Recipe
  }
}
</script>

<style scoped>
.recipes {
  display: flex;
  flex-flow: row wrap;
  justify-content: center;
  align-items: center;
}

.recipe{
  box-sizing: border-box;
  width: 280px;
  padding: 8px;
  border: 1px solid #ccc;
  box-shadow: 0 2px 2px #aaa;
  margin: 10px;
}

.thumbnail {
  background-position: center;
  background-size: cover;
  width: 100%;
  height: 200px;
}
</style>


