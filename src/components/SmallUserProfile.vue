<template>
    <div>
<div>
    <p>{{user[`name`]}}</p>
    <p>{{user[`age`]}}</p>
    <p v-if="user[`is_premium`]===true">Premium</p>
    <p v-else>not-Premium</p>
    <button @click="user_clicked">CLICK ME</button>


</div>
    </div>
</template>

<script>
    export default {
        props: {
            user: Object,
    },
    methods: {
        user_clicked(){
            this.$emit(`user_clicked`,this.user[`name`])
        }
        }
    }
</script>

<style scoped>

</style>