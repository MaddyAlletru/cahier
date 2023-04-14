<template>
  <span v-for="(order,index) in listOrders" :key="index">
    {{ order.orderNumber }}
    {{ order.clientName }}
    {{ order.clientPhone }}
    {{ order.description }} 
</span>
</template>

<script>

export default {
    name: 'OrdeRs',
    props: '[listOrders]'
}
</script>

<style>

</style>