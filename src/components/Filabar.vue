<template>
    <div class="barra-fila">
        <div class="progfill" :style="{width, background}" ></div>
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
                this.background = 'green'
            }else if (i >= 30 && i <= 60){
                this.background = 'yellow'
            }else {this.background = 'red' }
        }
    },
    computed:{
        
    },
    mounted(){
        this.ProgressBar()
    }
}
</script>