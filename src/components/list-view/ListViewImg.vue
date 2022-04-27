<template>

    <div class="HeaderCenter">
        <div class="backgrount-father">
        <img :src="obj.imgs" alt="" class="backgrount">
        </div>
        <img :src="obj.imgs" alt="">
        <p class="HeaderCenter-one">{{obj.names}}</p>
        <div class="HeaderCenter-three">
            <img :src="obj.avatarUrl" alt="">
            <p>{{obj.nickname}}</p>
        </div>
        <p class="HeaderCenter-two">{{obj.description}}</p>
    </div>

</template>

<script>
    export default {
        name: "ListViewImg",
        props: ['obj'],
        methods: {
            goback() {
                this.$router.go(-1)
            }
        },
        data(){
           return{

           }
        },

    }
</script>

<style scoped lang="less">

    .HeaderCenter {
        width: 100%;
        height: 150px;
        /*border: #42b983 1px solid;*/
        margin: 0 auto;
        .HeaderCenter-one {
            width: 50%;
            display: inline-block;
            font-size: 14px;
            font-weight: bold;
            margin-left: 20px;
            margin-top: 10px;
            /*border: #42b983 1px solid;*/
        }

        .HeaderCenter-two {
            width: 50%;
            height: 62px;
            /*border: #42b983 1px solid;*/
            overflow: hidden;float: right;
            font-size: 10px;
            margin-right: 20px;
        }

        img {
            float: left;
           width: 130px;
            height: 130px;
            margin-top: 10px;
            margin-left: 20px;
        }

        .HeaderCenter-three {
            width:50%;
            height: 30px;
            /*border: #42b983 1px solid;*/
            float: right;
            margin-top: -20px;
            margin-right: 40px;

            img {
                width: 20px;
                height: 20px;
                margin-top: 5px;
                margin-right: 2px;
                border-radius: 15px;
            }

            p {
                padding-bottom: 10px;
                padding-left: 30px;
                font-size: 12px;
                /*border: #42b983 1px solid;*/
            }

        }
        span {
            margin-left: 20px;
            border: #42b983 1px solid;
        }

    }
    .backgrount-father{
    .backgrount{
        width: 100%;
        height: 30%;
        filter: saturate(100%) blur(20px);
        z-index: -1000;
        position: fixed;
    }}
</style>