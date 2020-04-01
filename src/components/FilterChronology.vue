<template>
    <div class="filter">
        <div class="container">
            <div class="block">
                <button>Publications</button>
                <button class="active">People</button>
            </div>
            <div class="block">
                <button>Online</button>
                <button>Subscribe</button>
            </div>
        </div>
        <button class="button"><img src="../../public/chronology/add_post.svg" alt="">Add Publication</button>
    </div>
</template>

<script>
    export default {
        name: "FilterChronology"
    }
</script>

<style scoped lang="scss">
    .filter {
        display: flex;
        justify-content: space-between;
        margin: 20px 0;
        align-items: flex-start;
        .container {
            display: flex;
            align-items: center;
            .block {
                display: flex;
                margin: 0 12px;
                &:first-of-type {
                    margin-left: 0;
                }
                button {
                    color: #6E6C79;
                    font-size: 14px;
                    line-height: 16px;
                    font-weight: normal;
                    border: 1px solid #6E6C79;
                    height: 30px;
                    margin: 0 5px;
                    padding: 0 13px 0 14px;
                    border-radius: 5px;
                    &:first-of-type {
                        margin-left: 0;
                    }
                    &:hover, &.active {
                        color: #2E99E9;
                        border: 1px solid #2E99E9;
                    }
                }
            }
        }
        .button {
            background: #2E99E9;
            border-radius: 5px;
            color: #FFFFFF;
            font-weight: normal;
            font-size: 16px;
            line-height: 19px;
            width: 171px;
            height: 33px;
            display: flex;
            justify-content: space-between;
            padding: 0 15px;
            margin-right: 4px;
            img {
                /*margin-right: 10px;*/
            }
        }
    }
</style>