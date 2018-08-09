<template>
    <div v-bind:data-hello="'Hello ' + msg" class="hello">
        See my "data-hello" attribute in your browser's developer tool
    </div>
</template>

<script lang="ts">
    import {Component, Prop, Vue} from 'vue-property-decorator';

    @Component
    export default class HelloWorld extends Vue {
        @Prop() private msg: string = "Vue!";
    }
</script>

<style scoped>
    .hello {
        border: 1px solid red;
    }
</style>