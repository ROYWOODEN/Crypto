<template>

<h2>Избранное</h2>
<div @click="getFromFavs(index)" :class="favs" v-for="(el, index) in favs" :key="index">
    <span class="fav-span">{{ el.from }}</span>
    <span class="fav-span">{{ el.to }}</span>
</div>

</template>

<script>


export default {
    props: {
        favs: {
            type: Array,
            required: true
        },
        getFromFavs: {
            type: Function,
            required: true
        }
    }
}


</script>

<style scoped>

div {
    display: flex;
    /* flex-direction: row; */
    justify-content: space-between;
    width: 500px;
    margin: 10px auto;
    transition: all 500ms ease;
}

span {
    padding: 10px 15px;
    background-color: #8c00ff;
    color: #fff;
}
div:hover {
    opacity: 0.7;
    transform: scale(1.1);
    cursor: pointer;
}


</style>
