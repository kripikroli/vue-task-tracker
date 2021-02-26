<template>
    <button v-on:click="onClick()" v-bind:style="{background: color}" class="btn">{{ text }}</button>
</template>

<script>
export default {
    name: 'Button',
    props: {
        text: String,
        color: String
    },
    methods: {
        onClick() {
            console.log('Clicked');
        }
    }
}
</script>