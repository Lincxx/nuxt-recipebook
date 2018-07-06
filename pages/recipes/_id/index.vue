<template>
 <section class="single-recipe">
   <h1>{{recipe.title}}</h1>
   <div>
     <img class="recipe-image" :src="recipe.thumbnail" :alt="recipe.title">
   </div>
   <p>{{recipe.descriptionText}}</p>
 </section>
</template>


<script>
export default {
  asyncData(context){
    return new Promise((resolve, reject) => {
      setTimeout(()=> {
        resolve({
          recipe:[
            {
              id: "1",
              title: "Tasty Pizza",
              previewText: "One of the easiest and tastiest pizza around",
              descriptionText: "This is really delicious meal",
              thumbnail: "http://static.t13.cl/images/sizes/1200x675/1487787154-pizza.jpg"
            },
            {
              id: "2",
              title: "Tasty Hamburger",
              previewText: "One of the easiest and tastiest hamburgers around",
              descriptionText: "This is really delicious meal",
              thumbnail: "https://images.theconversation.com/files/180401/original/file-20170731-22175-67v3q2.jpg?ixlib=rb-1.1.0&rect=0%2C589%2C5472%2C2654&q=45&auto=format&w=1356&h=668&fit=crop"
            }
          ].find(el => el.id === context.params.id)
        })
      }, 1500)
    })
  },
}
</script>


<style scoped>
.single-recipe {
  display: flex;
  flex-flow: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  padding:30px;
}

.recipe-image {
  width: 700px;
}
</style>
