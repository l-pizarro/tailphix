<template>
    <div class="w-full flex items-center">
        <div class="w-5 h-5">
            <button class="w-full h-full border-2 rounded focus:outline-none" v-bind:class="{ 'border-gray-300': !check, 'border-indigo-200 bg-indigo-400': check }" @click="tap()"></button>
        </div>
        <span class="ml-4 text-lg" v-bind:class="{ 'text-gray-500': !check, 'text-gray-600': check }" v-if="showLabel">{{label}}</span>
    </div>
</template>

<script>
export default {
    name: 'checkbox',
    props: [
        "showLabel",
        "label"
    ],
    data() {
        return {
            check: false
        }
    },
    methods: {
        tap() {
            this.check = !this.check;
            this.$emit('onCheck');
        }
    }
}
</script>