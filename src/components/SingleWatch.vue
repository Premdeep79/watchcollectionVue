<template>
    <div class="watch-container">
        <div class="img-container">
            <img :src="watch.image" alt="watch-img" />
        </div>
        <div class="details">
            <h2 class="brand">{{watch.brand}}</h2>
            <p class="watch_name">{{watch.watch_name}}</p>
            <p class="year_of_manufacture"> {{watch.model}} | {{watch.year_of_manufacture}}</p>
            <p class="price">{{watch.price}}</p>
            <p class="features"> special features : {{watch.features}}</p>
        </div>
    </div>
</template>

<script>
    export default{
        name: 'SingleWatch',
        props:{
            watch: Object
        }
    }
</script>

<style scoped>
.brand {
    text-align: center;
    letter-spacing: 1px;
    color: coral;
}
.watch_name, .year_of_manufacture{
    text-align: center;
    padding: 5px 0;
}
   .watch-container {
    width: 350px;
    background-color: #000;
    color: #FFF;
   }
   .img-container{
    width: 100%;
   }
   .img-container img{
    width: 100%;
   }
   .details{
    padding: 1rem;
    font-family: math;
   }
   .price{
    color: greenyellow;
    text-align: center;
    font-size: 1.5rem;
    padding: 5px 0;
   }
   .features{
    font-size: 0.8rem;
   }
</style>