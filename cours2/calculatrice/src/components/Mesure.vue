<template>
    <div>
        {{ convertedKM }} km
        {{ convertedM }} m
        {{ convertedCM }} cm
        {{ convertedMM }} mm
    </div>
</template>



<script lang="ts">

export default {
    name:"Mesure",
    data() {
        return{
          km: 0,
          m: 0,
          cm: 0,
          mm: 0
        }
    },
    computed:{
        conversion(){
            if(this.km){

            }else if(this.m){

            }else if(this.cm){

            }else if(this.mm){
                //return [km,m,cm]
            }
        }
    },
    emits:['convertedKM', 'convertedM', 'convertedCM', 'convertedMM']
}


</script>


<style>

</style>