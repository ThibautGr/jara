<template>
  <div class="home">
    <TicketsList :tickets="tickets"/>
  </div>
</template>

<script>
// @ is an alias to /src
//import HelloWorld from '@/components/HelloWorld.vue'
import TicketsList from "@/components/Tickets/TicketsList";
import ticketsService from '@/services/tickets';
export default {
  name: 'Home',
  components: {
    TicketsList,
  },
  data(){
    return{
      tickets : []
    }
  },
  async beforeCreate(){
    const tickets = await ticketsService.getTickets();
    this.tickets = tickets;
  }
}
</script>
