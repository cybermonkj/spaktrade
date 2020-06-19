<template>
    <div>
        <v-carousel class="carousel">
            <v-carousel-item
             v-for="(item, i) in items"
             :key="i"
             :src="item.img"
            ></v-carousel-item>
        </v-carousel>

        <!-- <img src="@/assets/finance.svg" alt=""> -->
    </div>
</template>

<script>

export default {
    data() {
        return {
            items: [
                {
                    img: 'https://42f2671d685f51e10fc6-b9fcecea3e50b3b59bdc28dead054ebc.ssl.cf5.rackcdn.com/illustrations/finance_0bdk.svg'
                },
                {
                    src: 'https://42f2671d685f51e10fc6-b9fcecea3e50b3b59bdc28dead054ebc.ssl.cf5.rackcdn.com/illustrations/investing_7u74.svg'
                },
                {
                    src: 'https://42f2671d685f51e10fc6-b9fcecea3e50b3b59bdc28dead054ebc.ssl.cf5.rackcdn.com/illustrations/personal_finance_tqcd.svg'
                },
                {
                    src: 'https://42f2671d685f51e10fc6-b9fcecea3e50b3b59bdc28dead054ebc.ssl.cf5.rackcdn.com/illustrations/around_the_world_v9nu.svg'
                },
                {
                    src: 'https://42f2671d685f51e10fc6-b9fcecea3e50b3b59bdc28dead054ebc.ssl.cf5.rackcdn.com/illustrations/business_deal_cpi9.svg'
                },
            ],
        }
    },
}
</script>

<style scoped>
    .carousel {
        margin-top: 0rem !important;
    }
</style>