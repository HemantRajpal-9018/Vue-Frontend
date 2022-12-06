<template>
        <div>

            <h2>{{book.Brand}}</h2>
            <h4>{{book.Operating_System}}</h4>
            <h4>{{book.Processor}}</h4>
            <h4>{{book.Memory}}</h4>
            <h4>{{book.Storage_Size}}</h4>
            <h4>{{book.Release_Year}}</h4>
            <h4>{{book.Model_Number}}</h4>
            


        </div>

</template>

<script>

    export default{
        name: 'BookItem',
        props: {
            book: Array
        }
    }
    

</script>


<style scoped>


h4{
    margin: 2px;
    color:#ff4500;
}
h2{
    color:red;
}
div{
     background-color: #7CF3A0;
     color:#81B622;
     color: black;
     padding: 1em;
     margin: 5px;   
     border-radius: 30px;
    }




</style>