<template>
    <div class="about_me">
        <div class="info">
            <p class="title"><img src="../../public/chronology/info.svg" alt=""> About Me</p>
            <p class="text">I am very beautiful girl, and I know it. But I don't feel myself quen , because I didn't meet <a href="./">Continue Reading</a></p>
        </div>
        <div class="publications">
            <p>Publications</p>
            <div class="block">
                <div class="story img"><img src="../../public/chronology/post.jpg" alt=""><span></span></div>
                <div class="story movie"><img src="../../public/chronology/post.jpg" alt=""><span></span></div>
                <div class="story img"><img src="../../public/chronology/post.jpg" alt=""><span></span></div>
                <div class="story img"><img src="../../public/chronology/post.jpg" alt=""><span></span></div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "AboutMe"
    }
</script>

<style scoped lang="scss">
.about_me {
    border-left: 1px solid #c5c5c5;
    width: 630px;
    padding: 0 13px;
    overflow: auto;
    .info {
        margin-top: -4px;
        .title{
            color: #28263C;
            font-weight: bold;
            font-size: 18px;
            line-height: 21px;
            display: flex;
            img {
                margin-right: 10px;
            }
        }
        .text {
            color: #6E6C79;
            font-weight: normal;
            font-size: 14px;
            line-height: 16px;
            margin-top: 3px;
            a {
                color: #2E99E9;
            }
        }
    }
    .publications {
        margin-top: 23px;
        p {
            color: #28263C;
            font-weight: bold;
            font-size: 18px;
            line-height: 21px;
        }
        .block {
            display: flex;
            flex-wrap: wrap;
            margin-top: 15px;
            justify-content: space-between;
            .story {
                margin: 7px 0;
                position: relative;
                span {
                    position: absolute;
                    width: 40px;
                    height: 40px;
                    border-radius: 5px;
                    background: rgba(0, 0, 0, 0.5);
                    display: inline-block;
                    top: 7px;
                    right: 7px;
                }
                .img {
                    background-image: url("../../public/chronology/photo.svg");
                }
                .movie {
                    background-image: url("../../public/chronology/video.svg");
                }
            }
        }
    }
}
</style>