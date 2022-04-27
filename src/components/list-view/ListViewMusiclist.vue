
<template>
    <footer>
        <div class="footer-first">
            <div class="footer-first-left">
                <svg t="1651048862725" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="10612" width="40" height="40"><path d="M69.662 516.461a444.57 452.238 0 1 0 889.14 0 444.57 452.238 0 1 0-889.14 0Z" fill="#d81e06" p-id="10613"></path><path d="M407.56 714.368V303.616l355.722 205.376z" fill="#ffffff" p-id="10614"></path></svg>
                <p class="footer-first-left-one">播放全部</p>
                <span class="footer-first-left-two">共{{obj.tracksLength}}首</span>
            </div>

            <div class="footer-first-right">
                <p class="footer-first-right-one">+收藏</p>
            </div>
        </div>
        <div class="footer-second" v-for="(item,index) in obj.tracks">
            <span class="footer-second-one">{{index+1}}</span>
            <p class="footer-second-two" title="{{item.name}}"> {{item.name}}</p>
            <!--            歌曲名-->
            <p class="footer-second-three" :title="item.al.name">{{item.al.name}}</p>
            <!--            简介-->

            <div class="footer-thirds">
                <svg t="1651048862725" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="10612" width="20" height="20"><path d="M69.662 516.461a444.57 452.238 0 1 0 889.14 0 444.57 452.238 0 1 0-889.14 0Z" fill="#d81e06" p-id="10613"></path><path d="M407.56 714.368V303.616l355.722 205.376z" fill="#ffffff" p-id="10614"></path></svg>
                <svg t="1651048787296" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="7631" width="20" height="20"><path d="M981.333333 533.333333a21.333333 21.333333 0 0 1-21.333333 21.333334H448a21.333333 21.333333 0 0 1 0-42.666667h512a21.333333 21.333333 0 0 1 21.333333 21.333333zM533.333333 170.666667h426.666667a21.333333 21.333333 0 0 0 0-42.666667H533.333333a21.333333 21.333333 0 0 0 0 42.666667z m426.666667 725.333333H64a21.333333 21.333333 0 0 0 0 42.666667h896a21.333333 21.333333 0 0 0 0-42.666667zM89.66 696.753333C117.333333 715.186667 153.646667 725.333333 192 725.333333s74.7-10.146667 102.34-28.58c14.253333-9.5 25.56-20.746667 33.613333-33.44C336.833333 649.333333 341.333333 634.3 341.333333 618.666667V182a140.893333 140.893333 0 0 0 30.966667 27.82A21.18 21.18 0 0 0 376.666667 212c8.713333 3.2 16.773333 8.606667 23.953333 16.086667 16.733333 17.42 23.806667 41.146667 26.533333 53.733333a21.333333 21.333333 0 0 0 41.706667-9.026667c-4.5-20.773333-14.666667-50.513333-37.466667-74.266666-11.04-11.493333-23.64-20.093333-37.493333-25.606667-10.306667-7.126667-19.44-16.58-27.153333-28.133333-19.64-29.393333-24.373333-64.04-25.446667-82.08A21.333333 21.333333 0 0 0 298.666667 64v479.586667c-1.413333-1.02-2.846667-2-4.326667-3.006667C266.7 522.146667 230.353333 512 192 512s-74.666667 10.146667-102.34 28.58C75.406667 550.08 64.1 561.333333 56.046667 574 47.166667 588 42.666667 603.033333 42.666667 618.666667s4.5 30.666667 13.38 44.666666c8.053333 12.666667 19.36 23.92 33.613333 33.42z" fill="#5C5C66" p-id="7632"></path></svg>
            </div>
        </div>
    </footer>
</template>

<script>
    export default {
        name: "ListViewMusiclist",
        props: ['obj'],
    }
</script>

<style scoped lang="less">
    footer {
        width: 100%;
        margin: 0 auto;
        height: 400px;
        /*border: blue 1px solid;*/

        .footer-first {
            width: 100%;
            height: 40px;
            /*border: #59ff00 1px solid;*/
            margin: 0 auto;
            list-style: none;

            .footer-first-left {
                width: 180px;
                height: 40px;
                position: relative;
                /*border: orange 1px solid;*/
                display: inline-block;

                .footer-first-left-one {
                    font-size: 18px;;
                    font-weight: bold;
                    display: inline-block;
                    position: absolute;
                    top: -10px;
                }

                .footer-first-left-two {
                    font-weight: lighter;
                    position: absolute;
                    display: inline-block;
                    top: 10px;
                    left: 120px;
                    text-align: center;
                    line-height: 100%;
                }
            }

            .footer-first-right {
                width: 80px;
                height: 80%;
                background: #ef3a07;
                border-radius: 15px;
                display: inline-block;
                float: right;
                top: 5px;
            }

            .footer-first-right-one {
                font-size: 14px;
                color: #e7e1e1;font-weight: bold;
                margin-top: 8px;margin-left: 20px;
                margin-right: 20px;
            }
        }

        .footer-second {
            list-style: none;
            /*border: 1px salmon solid;*/
            padding-top: 10px;


            .footer-second-one {
                /*border: 1px seagreen solid;*/
                display: inline-block;
                margin-top: 18px;
                height: 18px;
                width: 10px;
            }

            .footer-second-two {
                /*border: 1px #24096c solid;*/
                height: 18px;
                font-size: 14px;
                width: 70%;
                overflow: hidden;
                /*margin:0 auto;*/
                font-weight: bold;
                margin-top: -28px;
                margin-left: 22px;
            }

            .footer-second-three {
                /*border: 1px #790961 solid;*/
                font-size: 12px;
                font-weight: lighter;
                width: 70%;
                overflow: hidden;
                margin-top: -14px;
                margin-left: 22px;
            }


            .footer-thirds {
                width: 20px;
                /*border: 1px solid red;*/
                height: 50px;display: inline-block;
                float: right;margin-top: -50px;
            }
        }
    }
</style>