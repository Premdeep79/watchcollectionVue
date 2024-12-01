<template>
    <div class="watches-list">
        <div v-for="watch of watches" :key="watch.watch_name" > 
            <SingleWatch :watch=watch />
        </div>
    </div>
</template>
<script>
import SingleWatch from './SingleWatch.vue'

export default {
    name: 'WatchesList',
    props:{
        watches: Array
    },
    components:{
        SingleWatch
    }
    
}
</script>
<style scoped>
    .watches-list{
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        gap: 1rem;
        padding: 1rem;
        width: 65%;
        margin: auto;
    }
</style>
