<template>
    <ListViewImg :obj="obj"/>
    <ListMucilFen :obj="obj"/>
</template>

<script>
    import ListViewImg from "@/components/list-view/ListViewImg";
    import ListMucilFen from "@/components/list-view/ListMucilFen";
    export default {
        name: "ListViewBack",
        components: {ListMucilFen, ListViewImg}
    }
</script>

<style scoped>

</style>