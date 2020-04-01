<template>
    <footer>
        <div class="wrap">
            <div class="logo"><img src="../../public/chronology/logo_footer.svg" alt=""></div>
            <div class="language">
                <p>Language:</p>
                <select v-model="selected">
                    <option value="en">En</option>
                    <option value="ua">Ua</option>
                    <option value="ru">Ru</option>
                </select>
            </div>
        </div>
    </footer>
</template>

<script>
    export default {
        name: "Footer",
        data () {
            return {
                selected: 'en'
            }
        }
    }
</script>

<style scoped lang="scss">
footer {
    height: 50px;
    background: #FFFFFF;
    margin-top: 30px;
    margin-bottom: 53px;
    .wrap {
        padding: 10px 0;
        display: flex;
        justify-content: space-between;
        .logo {
            display: flex;
        }
        .language {
            display: flex;
            align-items: center;
            p {
                color: #6E6C79;
                font-weight: normal;
                font-size: 12px;
                margin-right: 5px;
            }
            select {
                background: none;
                border: none;
            }
            select, option {
                color: #6E6C79;
                font-weight: bold;
                font-size: 12px;
            }
        }
    }
}
</style>