<template>
    <div>
        
            <div class="card-media">
                <!-- media container -->
                <div class="card-media-object-container">
                    <div class="card-media-object" style="background-image: url(https://s9.postimg.cc/y0sfm95gv/prince_f.jpg);"></div>
                    <span class="card-media-object-tag subtle">Selling Fast</span>
                    <ul class="card-media-object-social-list">
                        <li v-for="attendee in event.atendees">
                            <img src="https://s10.postimg.cc/3rjjbzcvd/profile_f.jpg" class="">
                        </li>
                    </ul>
                </div>
                <!-- body container -->
                <div class="card-media-body">
                    <div class="card-media-body-top">
                        <span class="subtle">{{ event.date }}, {{ event.time }}</span>
                        <div class="card-media-body-top-icons u-float-right">
                        <svg fill="#888888" height="16" viewBox="0 0 24 24" width="16" xmlns="http://www.w3.org/2000/svg">
                            <path d="M0 0h24v24H0z" fill="none"/>
                            <path d="M18 16.08c-.76 0-1.44.3-1.96.77L8.91 12.7c.05-.23.09-.46.09-.7s-.04-.47-.09-.7l7.05-4.11c.54.5 1.25.81 2.04.81 1.66 0 3-1.34 3-3s-1.34-3-3-3-3 1.34-3 3c0 .24.04.47.09.7L8.04 9.81C7.5 9.31 6.79 9 6 9c-1.66 0-3 1.34-3 3s1.34 3 3 3c.79 0 1.5-.31 2.04-.81l7.12 4.16c-.05.21-.08.43-.08.65 0 1.61 1.31 2.92 2.92 2.92 1.61 0 2.92-1.31 2.92-2.92s-1.31-2.92-2.92-2.92z"/>
                        </svg>
                        <svg fill="#888888" height="16" viewBox="0 0 24 24" width="16" xmlns="http://www.w3.org/2000/svg">
                            <path d="M17 3H7c-1.1 0-1.99.9-1.99 2L5 21l7-3 7 3V5c0-1.1-.9-2-2-2z"/>
                            <path d="M0 0h24v24H0z" fill="none"/>
                        </svg>
                        </div>
                    </div>
                    <span class="card-media-body-heading">{{ event.title }}</span>
                    <div class="card-media-body-supporting-bottom">
                        <span class="card-media-body-supporting-bottom-text subtle">{{ event.address }}</span>
                        <span class="card-media-body-supporting-bottom-text subtle u-float-right">Free &ndash; {{ event.price }}</span>
                    </div>
                    <div class="card-media-body-supporting-bottom card-media-body-supporting-bottom-reveal">
                        <span class="card-media-body-supporting-bottom-text subtle">#Music #Party</span>
                        <router-link :to="{ name: 'event-show', params: { id: event.id }}" class="card-media-body-supporting-bottom-text card-media-link u-float-right">VIEW EVENTS</router-link>
                    </div>
                </div>
            </div>
    </div>
</template>

<script>
    export default {
        props: {
            event: Object
        }
    }
</script>

<style scoped>
h1 {
    color: green;
}
</style>