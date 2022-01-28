<template>
    <div class="container">
        <h1>TEBRİKLER KAZANDINIZ!</h1>
        <button  @click="yeniOyun">Tekrar Oyna!</button>
        
    </div>
    
</template>
<style scoped>
    .container{
        position: absolute;
        background: white;
        color: darkgreen;
        width: 100%;
        height: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
        top: 0px!important;
        left: 0px;

    }
    h1{
        
        font-size: 80px;
    }
    button{
        width: 300px;
        height: 50px;
        color: darkgreen;
        font-size: 30px;
        border-radius: 10px;
        border: 1px solid darkgreen;
        margin-bottom: 200px;
        cursor: pointer;
        transition: all .5s;       
    }
    button:hover{
        background-color:green ;
        color: white;
        transition: all .5s;
    }
</style>
<script>
    export default {
        methods : {
            yeniOyun(){
                window.location.reload();

            }
        }

    }
</script>
