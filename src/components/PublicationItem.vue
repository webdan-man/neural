<template>
    <div class="publication"
         @mouseover="mouseoverAction"
         @mouseleave="mouseleaveAction"
         :class="{'active': hover}"
    >
        <div class="container" :style="actionStyle">
            <div class="main">
                <div class="photo_group">
                    <div class="photo_actions">
                        <a href="./"><img src="../../public/chronology/access.svg" alt=""></a>
                        <a href="./"><img src="../../public/chronology/chose.svg" alt=""></a>
                        <a href="./"><img src="../../public/chronology/star_full.svg" alt=""></a>
                        <a href="./"><img src="../../public/chronology/lock.svg" alt=""></a>
                    </div>
                    <div class="photo">
                        <img :src="item.imgUrl" alt="">
                        <div class="status" :class="item.status"></div>
                    </div>
                    <div class="photo_menu"><img src="../../public/chronology/photo_menu.svg" alt=""></div>
                </div>
                <div class="title">
                    <p class="name">{{item.name}}, <span>{{item.age}}</span></p>
                    <p class="location">{{item.location}}</p>
                </div>
                <div class="actions">
                    <button><img src="../../public/chronology/live.svg" alt=""></button>
                    <button class="active"><img src="../../public/chronology/gift.svg" alt=""></button>
                    <button><img src="../../public/chronology/travel.svg" alt=""></button>
                </div>
                <div class="buttons">
                    <button>Go massager</button>
                    <button>+ Subscribe</button>
                </div>
            </div>
            <AboutMe v-if="hover"/>
        </div>
    </div>
</template>

<script>
    const AboutMe = () => import('@/components/AboutMe')
    export default {
        name: "PublicationItem",
        props: {
            publicationList: Array,
            item: Object,
            index: Number
        },
        components: {
            AboutMe
        },
        data() {
            return {
                hover: false,
                actionStyle: {

                }
            }
        },
        methods: {
            mouseoverAction (event) {
                if ((document.documentElement.clientWidth - event.pageX) < 330) this.actionStyle = {'left': '-305px'};
                this.hover = true
            },
            mouseleaveAction () {
                this.actionStyle = {};
                this.hover = false
            }
        }
    }
</script>

<style scoped lang="scss">

    .publication {
        width: 257px;
        height: 346px;
        margin-bottom: 20px;
        position: relative;
        z-index: 1;
        &.active {
            z-index: 2;
            display: flex;
            flex-direction: row;
            justify-content: space-between;
            cursor: pointer;
            .container {
                width: 561px;
                display: flex;
            }
        }
        .container {
            border-radius: 5px;
            background: #FFFFFF;
            position: absolute;
            top: 0;
            bottom: 0;
            left: 0;
            width: 100%;
            padding: 20px 0 10px;
            .main {
                width: 100%;
                .photo_group {
                    width: 100%;
                    display: flex;
                    align-items: flex-start;
                    justify-content: center;
                    .photo_actions {
                        display: flex;
                        flex-direction: column;
                        a {
                            margin-bottom: 6px;
                        }
                    }
                    .photo {
                        position: relative;
                        display: flex;
                        margin: 0 4px;
                        img {
                            border-radius: 50%;
                        }
                        .status {
                            position: absolute;
                            bottom: 15px;
                            right: 10px;
                            width: 20px;
                            height: 20px;
                            border: 2px solid #FFFFFF;
                            border-radius: 50%;
                            &.online {
                                background: #00CF72;
                            }
                        }
                    }
                    .photo_menu {
                        display: flex;
                        cursor: pointer;
                    }
                }
                .title {
                    text-align: center;
                    display: flex;
                    align-items: center;
                    flex-direction: column;
                    .name {
                        color: #28263C;
                        font-weight: bold;
                        font-size: 18px;
                        line-height: 21px;
                        span {
                            font-weight: bold;
                            color: #c5c5c5;
                        }
                    }
                    .location {
                        color: #6E6C79;
                        font-size: 13px;
                        line-height: 18px;
                        background-image: url("../../public/chronology/pointer_user.svg");
                        background-position: top 3px left;
                        margin-top: 5px;
                        padding-left: 11px;
                    }
                }
                .actions {
                    display: flex;
                    align-items: center;
                    justify-content: center;
                    margin-top: 30px;
                    button {
                        background: #98B8E8;
                        border-radius: 7px;
                        width: 36px;
                        height: 36px;
                        margin: 0 5px;
                        display: flex;
                        align-items: center;
                        justify-content: center;
                        &.active {
                            background: #2E99E9;
                        }
                    }
                }
                .buttons {
                    margin-top: 10px;
                    display: flex;
                    align-items: center;
                    justify-content: center;
                    button {
                        color: #2E99E9;
                        font-weight: 300;
                        font-size: 14px;
                        line-height: 18px;
                        border: 1px solid #2E99E9;
                        border-radius: 7px;
                        padding: 8px 14px;
                        margin: 0 5px;
                    }
                }
            }
        }
    }
</style>