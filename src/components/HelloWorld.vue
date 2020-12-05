<template>
    <div class="hello">
        <h1>{{ msg }}</h1>
        <h2>やっほー！</h2>
    </div>
</template>

<script>
export default {
    name: 'HelloWorld',
    props: {
        msg: String
    },
    data() {
        return {
            env: null
        }
    },
    mounted() {
        this.env = process.env.VUE_APP_USE_MOCK
    }
}
</script>
