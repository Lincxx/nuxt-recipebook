<template>
  <section class="recipes">
    <Recipe
    v-for="recipe in recipes"
    :key="recipe.id"
    :thumbnail=recipe.thumbnail
    :title=recipe.title
    :id=recipe.id
    :previewText=recipe.previewText
    />

  </section>
</template>

<script>
import Recipe from '@/components/Recipe'

export default {
  components: {
    Recipe
  },
  asyncData(){
    return new Promise((resolve, reject) => {
      setTimeout(()=> {
        resolve({
          recipes:[
            {
              id: "1",
              title: "Tasty Pizza",
              previewText: "One of the easiest and tastiest pizza around",
              thumbnail: "http://static.t13.cl/images/sizes/1200x675/1487787154-pizza.jpg"
            },
            {
              id: "2",
              title: "Tasty Hamburger",
              previewText: "One of the easiest and tastiest hamburgers around",
              thumbnail: "https://images.theconversation.com/files/180401/original/file-20170731-22175-67v3q2.jpg?ixlib=rb-1.1.0&rect=0%2C589%2C5472%2C2654&q=45&auto=format&w=1356&h=668&fit=crop"
            }
          ]
        })
      }, 1500)
    })
  },
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


