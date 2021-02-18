<template>
    <div>
        <input type="text" v-model.number="km"/>

        <span> m : {{ m }}</span>
        <span> cm : {{ cm }}</span>
        <span> mm : {{ mm }}</span>
    </div>
</template>



<script lang="ts">

export default {
    name:"Mesure",
    data() {
        return{
          km: 0,
        }
    },
    computed:{
        m(): number{
            return this.km * 1000;
        },

        cm(): number{
            return this.m * 100;
        },

        mm(): number{
            return this.cm * 10;
        } // avec des computed, maintenant go faire avec des watcher
        
    },
    //aec les watcher, tu crée 4 datas km,m,cmet mm puis dans le wa tu fais this.m = value*1000 / this.cm = this.m * 100
}


</script>


<style>

</style>