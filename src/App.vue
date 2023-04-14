<template>
  <button @click="newOrder">Nouvelle commande</button>
  <h1>Cahier de commandes</h1>
  <span>Aujourd'hui, nous sommes le {{ date }} et il est {{ time }}</span>  

  <h2>Afficher les commandes du : 
    <input type="date" @click="showList"><br>
    <span>Voici les commandes du jour</span> 
    <orders :listOrders="orders"></orders>
  </h2>

  <h2>Liste des clients</h2>
  <clients :list="customers"></clients>

</template>

<script>
import Clients from './components/Clients.vue'
import Orders from './components/Orders.vue'

export default {
  name: 'App',
  components: {
    Clients,
    Orders,
  }, 
  data(){
    return{
        customers: [
          {firstname: "Maddy", lastname: "Alletru", phoneNumber: "0000000000"},
          {firstname: "Valentin", lastname: "Bailleul", phoneNumber: "0000000000"}, 
          {firstname: "Julie", lastname: "Corbec"},
          {lastname: "Peiniau", phoneNumber: "0000000000"},
        ], 
        
        date: new Date().toLocaleDateString(),
        time: new Date().toLocaleTimeString(),

        orders: [
          {orderNumber: "001", clientName: 'Client1', clientPhone: "0000000000", description: "blablablabbablablalblbalba"}, 
          {orderNumber: "002", clientName: 'Client2', clientPhone: "0000000000", description: "blablablabbablablalblbalba"}, 
          {orderNumber: "003", clientName: 'Client3', clientPhone: "0000000000", description: "blablablabbablablalblbalba"},
        ]
    }
  }, 
  methods:{
    showList(){
      alert('test')
    }, 
    newOrder(){
      alert('test')
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
