<template>
    <div>
        <div class=" border-solid  border-1 mx-2 border-gray-600 bg-gray-200 shadow-lg h-64 border-gray-800 p-5 w-64 hover:shadow-xl hover:cursor-pointer" v-for="destination in destinations" :key="destination.name">
            <h3 class="font-medium font-2xl">{{destination.name}}</h3>
            <img :src="destination.image">
            <slot></slot>
            <p> {{destination.description}}</p>
        
        </div>
    </div>
</template>

<script>
    export default {
        name:'Card',
        props:['destinations']
    }
</script>

<style lang="scss" scoped>

</style>