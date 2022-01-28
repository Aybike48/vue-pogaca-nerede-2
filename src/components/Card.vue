<template>
    <div class="container">
        <div @click="sendtoParent" class="card" >
            <img src="/src/assets/vue-js-egitim-background.jpg" alt="">
        </div>
    </div>
</template>
<script>
    export default {
        data(){
            return{
                answer : Math.ceil(Math.random()*5)
            }
        },
        methods : {
            sendtoParent(){
                this.$emit("data",this.answer)             
            },
        }
}
</script>

<style scoped>
    .card{
        width: 200px;
        height: 232px;
        display: flex;
        justify-content: space-evenly;
        border-radius: 10px;
        border: 4px solid rgb(121, 109, 109);
    }
    .card:hover{
        box-shadow: 0px 5px 48px  #666;
        transition: box-shadow .5s;
    }

</style>