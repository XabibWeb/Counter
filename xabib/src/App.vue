<template>
    <div>
            <p>Count: <strong>{{count}}</strong></p>
            <button class="plus" @click="increment">+</button>
            <button class="minus" @click="decrement">-</button>
    </div>
</template>

<script>
export default{
    data() {
        return{
            count: 0,
        }
    },
    methods: {
        increment() {
            this.count += 1
        },
        decrement() {
            this.count -= 1
        },
    },
    
}


</script>

<style>
#app {
    width: 100vw;
    height: 100vh;
    font-family: Arial, Helvetica, sans-serif;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    display: flex;
    justify-content: center;
    align-items: center;
    
}

p{
    font-size: 24px;
    text-align: center;
}

.plus,
.minus{
    width: 55px;
    height: 55px;
    font-size: 30px;
    color: #fff;
    transition: all .3s ease;
}

.plus{
    border: 1px solid #08b208;
    background-color: #08b208;
    border-radius: 5px 0 0 50%;
}

.minus{
    border: 1px solid #ff0000;
    background-color: #ff0000;
    border-radius: 0 5px 50% 0;
}

.plus:hover{
    box-shadow: 0 0 10px 5px #08b20882
}

.minus:hover{
    box-shadow: 0 0 10px 5px #ff00007d
}



</style>
