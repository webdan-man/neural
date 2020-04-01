<template>
    <div class="publication_group">
        <PublicationItem
                :key="index"
                v-for="(item, index) in publicationList"
                :item="item"
                :publicationList="publicationList"
                :index="index"
        />
    </div>
</template>

<script>
    import PublicationItem from '@/components/PublicationItem'
    export default {
        name: "PublicationGroup",
        data() {
            return {
                // eslint-disable-next-line no-unused-vars
                publicationList: new Array(15).fill(1).map(item => ({name: 'Evgeniya', age: '22', location: 'Ukraine, Kiev', imgUrl: require('../../public/chronology/catalog_item.jpg'), status: 'online'})),
            }
        },
        components: {
            PublicationItem
        }
    }
</script>

<style scoped lang="scss">
.publication_group {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: space-between;
}
</style>