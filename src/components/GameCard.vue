<template>
    <div class="gamecard">
        <h1>POGAÇA NEREDE ?</h1>
        
        <span>Açık kartlardan birini seçtiktenden sonra kapalı karta tıklayın.</span>
        <div class="container">
            <div @click="selectedPhoto=1" :class="{'shadow' : selectedPhoto == 1}" class="card">        
                <img src="/src/assets/card-1.jpg" alt="">            
            </div>
            <div :class="{'shadow' : selectedPhoto == 2}" @click="selectedPhoto=2" class="card">
                <img src="/src/assets/card-2.jpg" alt="">
            </div>
            <div :class="{'shadow' : selectedPhoto == 3}" @click="selectedPhoto=3" class="card">
                <img src="/src/assets/card-3.jpg" alt="">
            </div>
            <div :class="{'shadow' : selectedPhoto == 4}" @click="selectedPhoto=4" class="card">
                <img src="/src/assets/card-4.jpg" alt="">
            </div>
            <div :class="{'shadow' : selectedPhoto == 5}" @click="selectedPhoto=5" class="card">
                <img src="/src/assets/card-5.jpg" alt="">
            </div>  
            <p>{{selectedPhoto}}</p>    
        </div>
        
              
            
    </div>
    
</template>
<script>

export default {
    data(){
        return {
            selectedPhoto : " ",         
        }        
    },
    methods : {
        sendtoParent(){   
            this.$emit("data",this.selectedPhoto)        
        }
        
    }
}
</script>

<style scoped>
    .card{
        height: 232px;
        width: 200px;
        transition: box-shadow .5s;
        border-radius: 10px;
        border: 4px solid rgb(121, 109, 109);

    }
    .card:hover{
        box-shadow: 0px 5px 48px  #666;
        transition: box-shadow .5s;
    }

</style>