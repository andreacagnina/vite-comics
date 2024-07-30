<script>
export default {
    props: {
Card: Object
    }
    
}
</script>

<template>
<div class="col-2 content my-3"> 
    <a href=""> 
        <img :src="Card.thumb" :alt="Card.series" class="w-100"> 
        <h6 class="mt-2">{{Card.series}}</h6> 
    </a> 
</div>
</template>

<style lang="scss" scoped>
img {
    aspect-ratio: 1/1;
}
    
</style>