<template>
    <div>
<div>
    <p>{{user[`name`]}}</p>
    <p>{{user[`age`]}}</p>
    <p v-if="user[`is_premium`]===true">Premium</p>


</div>
    </div>
</template>

<script>
    export default {
        props: {
            user: Object,
        },
    }
</script>

<style scoped>

</style>