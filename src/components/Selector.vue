<template>
    
    <ul>
        <li :class="cryptoNow == 'BTC' ? 'active' : '' " @click="setCrypto('BTC')">Bitcoin</li>
        <li :class="cryptoNow == 'ETH' ? 'active' : '' " @click="setCrypto('ETH')">ETH</li>
        <li :class="cryptoNow == 'USDT' ? 'active' : '' " @click="setCrypto('USDT')">USDT</li>
    </ul>
    

</template>

<script>

export default {
    props: {
        setCrypto: {
            type: Function, 
            required: true
        },
        cryptoNow: {
            type: String,
            required: true
        }
    }
}

</script>

<style scoped>

ul {
    list-style: none;
    width: 200px;
    padding: 0;
    border-radius: 3px;
    border: 3px solid #000;
}

li {
    display: block;
    background-color: #1A032D;
    color: #fff;
    padding: 20px 0;
}
li:hover, li.active {
    background-color: #24043e;
    cursor: pointer;
}



</style>
