<template>
    <view>
        <block v-for="(item,index) in corecmsdata" :key="index">
            <!--�������޸���-->
            <corecmssearch :corecmsdata="item" v-if="item.widgetCode=='search' "></corecmssearch>
            <!--�л�-->
            <corecmstabbar :corecmsdata="item" v-if="item.widgetCode=='tabBar' "></corecmstabbar>
            <!--���棨�޸���-->
            <corecmsnotice :corecmsdata="item" v-if="item.widgetCode=='notice' "></corecmsnotice>
            <!--ͼƬ�ֲ����޸���-->
            <corecmsimgSlide :corecmsdata="item" v-if="item.widgetCode=='imgSlide' "></corecmsimgSlide>
            <!--�Ż�ȯ���޸���-->
            <corecmscoupon :corecmsdata="item" v-if="item.widgetCode=='coupon' "></corecmscoupon>
            <!--�ո��޸���-->
            <corecmsblank :corecmsdata="item" v-if="item.widgetCode=='blank' "></corecmsblank>
            <!--�����ı����������޸���-->
            <corecmstextarea :corecmsdata="item" v-if="item.widgetCode=='textarea' "></corecmstextarea>
            <!--��Ƶ���޸���-->
            <corecmsvideo :corecmsdata="item" v-if="item.widgetCode=='video' "></corecmsvideo>
            <!--ͼƬ�����޸���-->
            <corecmsimgWindow :corecmsdata="item" v-if="item.widgetCode=='imgWindow' "></corecmsimgWindow>
            <!--ͼƬ--���޸���-->
            <corecmsimgSingle :corecmsdata="item" v-if="item.widgetCode=='imgSingle' "></corecmsimgSingle>
            <!--��Ʒ���޸���-->
            <corecmsgoods :corecmsdata="item" v-if="item.widgetCode=='goods' "></corecmsgoods>
            <!--���£��޸���-->
            <corecmsarticle :corecmsdata="item" v-if="item.widgetCode=='article' "></corecmsarticle>
            <!--���·��ࣨ�޸���-->
            <corecmsarticleClassify :corecmsdata="item" v-if="item.widgetCode=='articleClassify' "></corecmsarticleClassify>
            <!--�����Զ��嵼�����޸���-->
            <corecmsnavBar :corecmsdata="item" v-if="item.widgetCode=='navBar' "></corecmsnavBar>
            <!--�Ź����޸���-->
            <corecmsgroupPurchase :corecmsdata="item" v-if="item.widgetCode=='groupPurchase' "></corecmsgroupPurchase>
            <!--�����¼���޸���-->
            <corecmsrecord :corecmsdata="item" v-if="item.widgetCode=='record' "></corecmsrecord>
            <!--ƴ�ţ��޸���-->
            <corecmspinTuan :corecmsdata="item" v-if="item.widgetCode=='pinTuan' "></corecmspinTuan>
            <!--�����޸���-->
            <corecmsservice :corecmsdata="item" v-if="item.widgetCode=='service' "></corecmsservice>
            <!--�������-->
            <corecmsadpop :corecmsdata="item" v-if="item.widgetCode=='adpop' "></corecmsadpop>
            <!--�ı����ݣ��޸���-->
            <corecmsContent :corecmsdata="item" v-if="item.widgetCode=='content' "></corecmsContent>
        </block>
    </view>
</template>

<script>
    import corecmsimgSlide from '@/components/corecms-page/corecms-imgSlide.vue'
    import corecmssearch from '@/components/corecms-page/corecms-search.vue'
    import corecmsnotice from '@/components/corecms-page/corecms-notice.vue'
    import corecmscoupon from '@/components/corecms-page/corecms-coupon.vue'
    import corecmsblank from '@/components/corecms-page/corecms-blank.vue'
    import corecmstextarea from '@/components/corecms-page/corecms-textarea.vue'
    import corecmsvideo from '@/components/corecms-page/corecms-video.vue'
    import corecmsimgWindow from '@/components/corecms-page/corecms-imgWindow.vue'
    import corecmsimgSingle from '@/components/corecms-page/corecms-imgSingle.vue'
    import corecmsgoods from '@/components/corecms-page/corecms-goods.vue'
    import corecmsarticle from '@/components/corecms-page/corecms-article.vue'
    import corecmsarticleClassify from '@/components/corecms-page/corecms-articleClassify.vue'
    import corecmsnavBar from '@/components/corecms-page/corecms-navBar.vue'
    import corecmsgroupPurchase from '@/components/corecms-page/corecms-groupPurchase.vue'
    import corecmsrecord from '@/components/corecms-page/corecms-record.vue'
    import corecmspinTuan from '@/components/corecms-page/corecms-pinTuan.vue'
    import corecmsservice from '@/components/corecms-page/corecms-service.vue'
    import corecmstabbar from '@/components/corecms-page/corecms-tabbar.vue'
    import corecmsadpop from '@/components/corecms-page/corecms-adpop.vue'
    import corecmsContent from '@/components/corecms-page/corecms-content.vue'

    export default {
        name: 'corecmsPage',
        components: {
            corecmsimgSlide,
            corecmssearch,
            corecmsnotice,
            corecmscoupon,
            corecmsblank,
            corecmstextarea,
            corecmsvideo,
            corecmsimgWindow,
            corecmsimgSingle,
            corecmsgoods,
            corecmsarticle,
            corecmsarticleClassify,
            corecmsnavBar,
            corecmsgroupPurchase,
            corecmsrecord,
            corecmspinTuan,
            corecmsservice,
            corecmstabbar,
            corecmsadpop,
            corecmsContent
        },
        props: {
            corecmsdata: {
                default: function () {
                    return []
                }
            }
        }
    }
</script>
