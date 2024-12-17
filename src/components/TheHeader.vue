<template>
   <div>
        <div>

        </div>
        
        <div>
            <label>Nome seu burro</label>
            <br>
            <input 
                v-model="name"
                type="text"
            ><br>
            {{ name }}
        </div>

        <br>

        <div>
            <label>Sports</label>
            <select v-model="sports">
                <option value="">Escolha</option>
                <option value="football">Football</option>
                <option value="basketball">Basketball</option>
                <option value="tennis">Tennis</option>
            </select> <br>

        {{  sports }}
        </div>

        <div>
            <label>Newsletter</label>
            <input
                v-model="newsletter"
                type="radio"
                value="Sim"
            >Sim
            <input
                v-model="newsletter"
                type="radio"
                value="Não"
            >Não
            <br>
            {{ newsletter }}
        </div>
        
        <br>

        <div>
           <label>Contrato</label>
           <input 
                v-model="contract"
                type="checkbox"
                value="Sim"
           > Aceita nossos termos...
           <br>
           {{ contract }}
        </div>
   </div>
</template>

<script>
    export default {
        name: 'App',
        data() {
            return {
               name: 'Ygao',
               sports: 'footbal',
               newsletter: '',
               contract: false
            }
        }
    }
</script>

<style>
    .title {
        font-size: 40px;
        color: red; 
    }
    .text {
        font-size: 16px;
        color: blue;
    }
    .header {
        background-color: black;
        color: white;
    }
</style>