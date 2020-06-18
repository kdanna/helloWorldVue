<template>
    <div>
        <div> he is {{details.age}} year old</div>
        <div v-for="(color, index) in details.color" :key="index">
            <p>{{color}}</p>
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