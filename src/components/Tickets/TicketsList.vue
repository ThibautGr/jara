<template>
  <div>
      <h1 v-for="ticket in tickets" :key="ticket.id">{{ticket.ticketNumber}} </h1>
  </div>
</template>

<script>
export default {
name: "TicketsList",
  props : {
    tickets : Array
  }
}
</script>

<style scoped>

</style>