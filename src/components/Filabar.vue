<template>
    <div class="barra-fila">
        <div class="progfill" :style="{width, background }" ></div>
    </div>
</template>
<style scoped>
    .barra-fila{
        width: 100px;
        height: 10px;
        background-color: #999;
        overflow: hidden;
        border-radius: 10px;
        border: 0.5px solid rgba(0, 0, 0, 0);
    }
    .progfill{
        height:100%;
        box-shadow: 0 0 0 10px rgba(136, 136, 136, 0.557);
        
    }
    
</style>
<script>
export default {
    name:"Filabar",
    props:{
        fila: Number,
        vez: String
    },
    data(){
        return{
            width: "",
            background: ''
            
        }
    },
    methods:{
        ProgressBar(){            
            const porc =  (this.fila * this.vez * 200) / 100
            
            this.width = porc + "%"
            
            this.changingColor(porc)
        },
        changingColor(i){
            if(i < 30){
                this.background = 'rgb(63, 143, 63)'
            }else if (i >= 30 && i <= 60){
                this.background = 'rgb(225, 225, 70)'
            }else {this.background = 'rgb(209, 34, 34)' }
        }
    },
    computed:{
        
    },
    mounted(){
        this.ProgressBar()
    }
}
</script>