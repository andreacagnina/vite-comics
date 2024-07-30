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
@use '../styles/partials/typographyColor' as *;
img {
    aspect-ratio: 1/1;
    &:hover {
        border: 10px inset lighten($brand_primary, 30%);
    }
}
    
</style>