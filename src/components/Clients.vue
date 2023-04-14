<template>
  <table border>
    <tr>
        <th>Nom</th>
        <th>Prénom</th>
        <th>Téléphone</th>
        <th>Adresse</th>
        <th>Code Postal</th>
        <th>Ville</th> 
    </tr>
    <tr v-for="(customer,index) in list" :key="index">
        <td>{{ customer.lastname }}</td>
        <td>{{ customer.firstname }}</td>   
        <td>{{ customer.phoneNumber }}</td>
    </tr>
  </table>
</template>

<script>

export default {
    name: 'CliEnts',
    props: ['list']
}
</script>

<style>
    th {
        font-family: Verdana, Geneva, Tahoma, sans-serif;
        font-size: 120%;
        text-align: center;
        background-color: rgb(39, 173, 173);
    }

    td{
        font-size: 100%;
        text-align: center;
    }
</style>