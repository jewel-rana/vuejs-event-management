<template>
    <div>
        <div class="container">
            <h1>{{ title }}</h1>
            <EventCard v-for="event in events" :key="event.id" :event="event" />
        </div>
    </div>
</template>

<script>
import EventCard from '@/components/EventCard.vue';
import EventService from '@/services/EventService.js';
export default {
    components: {
        EventCard
    },
    data() {
        return {
            title: "Event List",
            events: []
        }
    },
    created(){
        EventService.getEvents()
        .then(response => {
            this.events = response.data;
        })
        .catch( error => {
            console.log(error);
        });
    }
}
</script>