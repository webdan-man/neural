<template>
    <section>
        <div class="wrap">
            <FilterChronology />
            <PublicationGroup />
        </div>
    </section>
</template>

<script>
    import FilterChronology from '@/components/FilterChronology'
    import PublicationGroup from '@/components/PublicationGroup'
    export default {
        name: "Section",
        components: {
            FilterChronology,
            PublicationGroup
        }
    }
</script>

<style scoped>

</style>