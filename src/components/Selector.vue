<template>
    
    <ul>
        <li :class="current == 'BTC' ? 'active' : '' " @click="selectItem('BTC')">Bitcoin</li>
        <li :class="current == 'ETH' ? 'active' : '' " @click="selectItem('ETH')">ETH</li>
        <li :class="current == 'USDT' ? 'active' : '' " @click="selectItem('USDT')">USDT</li>
    </ul>
    

</template>

<script>

export default {
    props: {
        setCrypto: {
            type: Function, 
            required: true
        }
    },
    data() {
        return {
            current: ''
        }
    },
    methods: {
        selectItem(val) {
            this.setCrypto(val);
            this.current = val;
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
