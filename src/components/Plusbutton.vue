<template>
    <div class="base" :style="this.none">
        <div @click="clicou()" id="plus" :style="this.transform">+</div>
    </div>
</template>
<style scoped>
    .base {
        background-color: rgb(41, 41, 222);
        width: 60px;
        height: 60px;
        border-radius: 50%;
        display: flex;
        justify-content: center;
        align-items: center;
        position: absolute;
        right:90px; 
        margin-top: 5%;
        transition: 1.5s;
    
    }
    #plus{
        font-size: 55px;
        list-style: none;
        color: wheat;
        font-weight: bolder;
        text-shadow: 2px 2px 2px rgb(52, 49, 43);
        transition: color 8s;
        cursor: pointer;
    }
</style>
<script>
export default {
    name:"Plusbutton",
    data(){
        return{
          transform: "",
          none:''
        }
    },
    methods:{
    }
}
</script>