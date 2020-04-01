<template>
    <header>
        <div class="wrap">
            <a href="./" class="logo">
                <img src="../../public/chronology/logo.svg" alt="">
            </a>
            <input class="search" type="search" placeholder="Search">
            <div class="action_block">
                <div class="money">
                    <img src="../../public/chronology/credit.svg" alt="">
                    <span>0.00</span>
                </div>
                <div class="user">
                    <div class="img">
                        <img src="../../public/chronology/user.jpg" alt="">
                    </div>
                    <p class="name">Bill</p>
                    <button class="user_menu"><img src="../../public/chronology/poligon.svg" alt=""></button>
                </div>
                <a href="./" class="notification">
                    <img src="../../public/chronology/events.svg" alt="">
                </a>
                <a href="./" class="messages">
                    <img src="../../public/chronology/mail.svg" alt="">
                </a>
            </div>
        </div>
    </header>
</template>

<script>
    export default {
        name: "Header"
    }
</script>

<style scoped lang="scss">
    header {
        display: flex;
        background: #FFFFFF;
        padding: 7px 0;
        .wrap {
            display: grid;
            grid-template-columns: 200px 400px auto;
            a.logo {
                display: flex;
                img {

                }
            }
            .search {
                height: 27px;
                background-color: #FAFAFA;
                border-radius: 5px;
                width: 360px;
                color: #C5C5C5;
                font-size: 12px;
                line-height: 18px;
                margin-left: 24px;
                padding-left: 20px;
                margin-top: 10px;
                background-image: url("../../public/chronology/search.svg");
                background-repeat: no-repeat;
                background-position: center right 12px;
            }
            .action_block {
                display: flex;
                flex-direction: row-reverse;
                align-items: center;
                .money {
                    display: flex;
                    align-items: center;
                    border-left: 1px solid #C5C5C5;
                    height: 44px;
                    padding: 0 0 0 14px;
                    img {
                        margin-right: 6px;
                    }
                    span {
                        font-weight: bold;
                        font-size: 18px;
                        color: #2E99E9;
                    }
                }
                .user {
                    display: flex;
                    align-items: center;
                    margin-right: 16px;
                    margin-left: 17px;
                    .img {
                        border-radius: 50%;
                        margin-right: 18px;
                        display: flex;
                    }
                    .name {
                        color: #29333F;
                        font-size: 14px;
                        line-height: 16px;
                        font-weight: bold;
                        margin-right: 17px;
                    }
                    .user_menu {
                        display: flex;
                        align-items: center;
                        justify-content: center;
                    }
                }

                .notification {
                    align-items: center;
                    margin: 0 13px;
                }
                .messages {
                    align-items: center;
                    margin: 0 12px;
                }
            }
        }
    }
</style>