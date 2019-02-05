<template>
    <my-page title="截图制作" :page="page">
        <app-list :data="groups" />
    </my-page>
</template>

<script>
    export default {
        data () {
            return {
                groups: [
                    {
                        name: '微信',
                        apps: [
                            {
                                name: '微信首页',
                                desc: '',
                                icon: '/static/img/fun.svg',
                                to: 'xxx',
                                href: 'https://faker.yunser.com/#/weixin/homepage',
                                target: '_blank'
                            },
                            {
                                name: '微信聊天',
                                desc: '',
                                icon: '/static/img/fun.svg',
                                to: 'xxx',
                                href: 'https://faker.yunser.com/#/weixin/chat',
                                target: '_blank'
                            },
                            {
                                name: '微信红包',
                                desc: '',
                                icon: '/static/img/fun.svg',
                                to: 'xxx',
                                href: 'https://faker.yunser.com/#/weixin/hongbao',
                                target: '_blank'
                            },
                            {
                                name: '微信转账',
                                desc: '',
                                icon: '/static/img/fun.svg',
                                to: 'xxx',
                                href: 'https://faker.yunser.com/',
                                target: '_blank'
                            },
                            {
                                name: '微信零钱',
                                desc: '',
                                icon: '/static/img/fun.svg',
                                to: 'xxx',
                                href: 'https://faker.yunser.com/#/weixin/lingqian',
                                target: '_blank'
                            }
                        ]
                    },
                    {
                        name: '支付宝',
                        apps: [
                            {
                                name: '支付宝账单',
                                desc: '',
                                icon: '/static/img/fun.svg',
                                to: 'xxx',
                                href: 'https://faker.yunser.com/#/zhangdan/zhangdan',
                                target: '_blank'
                            },
                            {
                                name: '支付宝余额',
                                desc: '',
                                icon: '/static/img/fun.svg',
                                to: 'xxx',
                                href: 'https://faker.yunser.com/',
                                target: '_blank'
                            },
                            {
                                name: '余额宝',
                                desc: '',
                                icon: '/static/img/fun.svg',
                                to: 'xxx',
                                href: 'https://faker.yunser.com/#/zfb/yeb',
                                target: '_blank'
                            },
                            {
                                name: '蚂蚁花呗',
                                desc: '',
                                icon: '/static/img/fun.svg',
                                to: 'xxx',
                                href: 'https://faker.yunser.com/#/huabei/huabei',
                                target: '_blank'
                            }
                        ]
                    }
                ],
                page: {
                    menu: [
                        {
                            type: 'icon',
                            icon: 'apps',
                            href: 'https://app.yunser.com/',
                            target: '_blank',
                            title: '应用'
                        }
                    ]
                }
            }
        },
        computed: {
        },
        mounted() {
        },
        methods: {
            init() {
            },
            fileChange(e) {
            },
            sizeStr: function (size) {
            }
        }
    }
</script>

<style lang="scss" scoped>
@import '../scss/var';

.tool-list {
    max-width: 840px;
    margin: 0 auto;
    @include clearfix;
    .list-item {
        position: relative;
        float: left;
        width: 260px;
        height: 96px;
        padding: 8px;
        margin: 2px 16px 16px 2px;
        background-color: #fff;
        //border: 1px solid #ccc;
        cursor: pointer;
        &:hover {
            background-color: #f9f9f9;
            // box-shadow: 0 3px 10px rgba(0,0,0,.156863), 0 3px 10px rgba(0,0,0,.227451);
            //border-color: #09c;
            .icon {
                display: block;
            }
        }
        &.active {
            border: 1px solid #f00;
        }
    }
    a {
        display: block;
        height: 100%;
        color: #666;
    }
    .img {
        float: left;
        width: 72px;
        height: 72px;
        margin-right: 16px;
        background-color: #fff;
        border: 1px solid #e9e9e9;
        border-radius: 8px;
    }
    .info {
        float: left;
    }
    .text {
        font-size: 18px;
        color: #000;
    }
    .header {
        overflow: hidden;
    }
    .desc {
        max-width: 150px;
        margin-top: 8px;
    }
    .icon-heart {
        display: none;
        position: absolute;
        top: 8px;
        right: 8px;
        &:hover {
            color: #f00;
        }
    }
    .icon-close {
        display: none;
        position: absolute;
        top: 32px;
        right: 8px;
        &:hover {
            color: #f00;
        }
    }
}
@media all and (max-width: 400px){
    .tool-list {
        .list-item {
            width: 100%;
            margin-right: 0;
        }
    }
}
</style>
