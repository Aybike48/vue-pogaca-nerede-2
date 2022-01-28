<template>
    <div class="container">
        <h1>MAALESEF KAYBETTİNİZ</h1>
        <button  @click="yeniOyun">Yeniden Dene!</button>
        
    </div>
    
</template>
<style scoped>
    .container{
        position: absolute;
        background-color:darkred ;
        width: 100%;
        height: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
        top: 0px!important;
        left: 0px;

    }
    h1{
        color: white;
        font-size: 80px;
    }
    button{
        width: 300px;
        height: 50px;
        color: darkred;
        font-size: 30px;
        border-radius: 10px;
        border: none;
        margin-bottom: 200px;
        cursor: pointer;
        transition: all .5s;       
    }
    button:hover{
        background-color:rgb(172, 55, 156) ;
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
