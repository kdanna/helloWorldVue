<template>
    <div>
        <div v-for="(detail, index) in details" :key="index">
            <li>{{detail}}</li>
        </div>
    </div>
</template>

<script>

export default {
    name: 'Details',
    props: {
        details: Object,
    }
}
</script>

<style scoped>

</style>