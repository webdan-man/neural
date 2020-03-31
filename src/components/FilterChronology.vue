<template>
    <div class="filter">
        <div class="containter">
            <div class="block">
                <button>Publications</button>
                <button class="active">People</button>
            </div>
            <div class="block">
                <button>Online</button>
                <button>Subscribe</button>
            </div>
        </div>
        <button class="button"><img src="" alt="">Subscribe</button>
    </div>
</template>

<script>
    export default {
        name: "Filter"
    }
</script>

<style scoped lang="scss">
    .filter {
        display: flex;
        align-items: center;
        justify-content: space-between;
        .containter {
            display: flex;
            align-items: center;

            .block {
                display: flex;
                margin: 0 15px;
                button {
                    color: #6E6C79;
                    font-size: 14px;
                    line-height: 16px;
                    font-weight: normal;
                    border: 1px solid #6E6C79;
                    height: 30px;
                    padding: 17px 14px;
                    margin: 0 5px;
                }
            }
        }
        .button {

        }
    }
</style>