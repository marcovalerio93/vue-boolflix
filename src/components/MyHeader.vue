<template>
    <div class="bg">
        <div class="d-flex">
            <h1>BOOLFLIX</h1>
            <div>
                <input type="text" placeholder="search" v-model="searchByText"/>
                <button @click="$emit('search', searchByText)">Cerca</button>
            </div>
            
        </div>
    </div>  
</template>

<script>
export default {
    name:"MyHeader",
    data () {
        return{
            searchByText: ''
        }
    }
    

}
</script>

<style scoped lang="scss">
   
    .bg{
        width: 100%;
        background-color: black;
    }   

    div .d-flex{
    height: 70px;
    margin: 10px;
    display: flex;
    justify-content: space-between;

        h1{
        color: red;
        margin-top: 15px;
        }
       input{
           width: 80%;
           height: 40%;
           margin-top: 15px;
        }
    }

</style>