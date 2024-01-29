<script>
    export default {
        name: "Contador",
        data: () => {
            return {
                numero: 0,
            };
        },
        
        methods: {
            incrementar () {
                this.numero++;
            },
            decrementar (){
                this.numero--;
            },
            resetear () {
                this.numero = 0;
            }
        }
    };

</script>

<template>
    <h1>El valor del contador es: {{numero}}</h1>
    <input type="button" value="Incremetar" v-on:click="incrementar" />
    <input type="button" value="Decremetar" :disabled="numero <= 0"  v-on:click="decrementar"/>
    <input type="button" value="Resetear" :disabled="numero === 0" @click="resetear"/>
</template>

<style>
    body{
        background-color: #AC7D88;
    }
    input{
        background-color: #85586F;
        border-radius: 20px;
        margin-left: 20px;
        border: none;
        padding: 10px;
    }
</style>

