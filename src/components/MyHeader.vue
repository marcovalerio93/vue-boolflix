<template>
    <div class="bg">
        <div class="d-flex">
            <h1>BOOLFLIX</h1>
            <input type="text"/>
        </div>
    </div>  
</template>

<script>
export default {
    name:"MyHeader",

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
            }
            input{
                width: 20%;
                height: 40%;
                margin-top: 25px;
            }
        }
    


</style>