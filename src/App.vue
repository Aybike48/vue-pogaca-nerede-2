<template> 
    <div>
        <component :is="whichComponent"> </component>
        <GameCard @data="selectedPhoto=$event"> </GameCard>
        <Card @data="answer=$event"></Card>
        <p>{{answer}} </p>
        <p>{{selectedPhoto}}</p>
        <canvas key="canvas" id="canvas" ></canvas>
            
    </div>
        
    
</template>
<script>
import GameCard from "./components/GameCard.vue"
import Fail from "./components/Fail.vue"
import Celebrate from './components/Celebrate.vue'
import Card from "./components/Card.vue"
export default {
    data(){
        return{
            whichComponent : "GameCard",
            answer:"",
            selectedPhoto:""
        }
    },
    components : {
        GameCard,
        Celebrate,
        Fail,
        Card
    }

}
</script>
<style>
    body{
        background-color:bisque;
        text-align: center;
        font-family: sans-serif;
        color: #666;
    }
    img{
        width: 100%;
        height: 100%;
    }
    .container{
        display: flex;
        justify-content: space-evenly;
        padding-top:100px ;
    }
    .shadow{
        box-shadow: 0px 5px 48px #30969f!important;
        transition: box-shadow .5s;
    }
</style>
