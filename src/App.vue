

<template>
  <div class="container">
      <!-- Step 3 must use the component-->
      <HeaderTop bookName="Laptop Giant" 
       authorName="Laptop Models"/>
      <BookBox :books="books"/>
  </div>

</template>

<script>


// Step 1: Import components
import HeaderTop from './components/HeaderTop.vue'
import BookBox from './components/BookBox.vue'



export default{
    name: 'App',

    // step 2: must register the component
    components: {
    HeaderTop,
    BookBox
},
    data(){
      return{
        books:[]
      }
    },
      methods:{
        //promiss 
          async fetchLaptop(){
          const res = await fetch ("https://laptop-giant-app.herokuapp.com/api")
          const data = await res.json()
          console.log(data)

          return data.Laptop
        }
      },
      async created(){
        this.books = await this.fetchLaptop()
      }
  }

</script>


<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
*{
box-sizing: border-box;
margin: 0;
padding: 0;
}
body{
font-family:  'Monsterrat', sans-serif;
}
.container{
max-width: 100%;
min-height: 300px;
overflow:  auto;
margin: 30px auto;
border: 0.3 em solid black;
border-radius: 5px
}

div{
margin-bottom: 0.5em;
}
</style>
