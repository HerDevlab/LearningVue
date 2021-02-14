<template>
    <div>
      {{ calcul }}
    </div>
</template>



<script lang="ts">

export default {
    name:"Calcul",
    props:{
        num1: Number,
        num2: Number,
        signe: String
    },
    computed:{
        calcul(){
            switch(this.signe){
                case '+':
                    return this.num1 + this.num2
                case '-':
                    return this.num1 - this.num2
                case '*':
                    return this.num1 * this.num2
                case '/':
                    return this.num1 / this.num2
                case '%':
                    return this.num1 % this.num2
            }
        }
    },
    emits:['resultat']
}
</script>




<style>

</style>