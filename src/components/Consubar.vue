<template>
    <div class="box">
        <div class="box-circle">
            <svg>
                <circle cx="17" cy="17" r="17"></circle>
                <circle id="barProg" cx="17" cy="17" r="17" > </circle>
            </svg>
            {{ consulta }}
        </div>
    </div>
</template>
<style scoped>
    .box{
        width:10px;
    }
    svg{
        width: 50px;
        height: 50px;
        margin-top: 10px;
    }
    circle{
        width: 50px; height: 50px;
        fill: none;
        stroke: black;
        stroke-width: 5;
        transform:translate(5px, 5px);
        stroke-dasharray: 106;
        stroke-dashoffset: 106;
    
    }
    circle:nth-child(1){
        stroke-dashoffset: 0;
        stroke: #111;
    }
    circle:nth-child(2){
        transition: stroke-dashoffset 5s;
        stroke: dodgerblue;
    }
</style>
<script>

    export default {
        name:"Consubar",
        props:{
            consulta : String,
            id : String

        },
        data(){
            return{
                
            }
        },
        methods:{
            progBar() {
                const bar = document.querySelector("#barProg");

                const consu = parseInt(this.consulta)
    
                bar.style.strokeDashoffset = 106 - (106 * consu) / 100;
                
                console.log(document.ENTITY_NODE)
            }

        },
        mounted(){
            this.progBar()
            
        }

}
</script>