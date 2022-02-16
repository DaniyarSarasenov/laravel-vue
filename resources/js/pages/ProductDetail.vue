<template>
    <div class="container">
        <div class="row page-content">
            <div class="col-md-12" style="padding: 0px 20px">
                <div class="col-md-12 mb-10">
                    <img class="detail-image" src="../../img/product_default.jpg">
                </div>

                <div class="col-md-12 detail-description mb-10">
                    Our comprehensive guide to CSS flexbox layout. This complete guide explains everything about flexbox, focusing on all the different possible properties for the parent element (the flex container) and the child elements (the flex items).
                </div>

                <div class="col-md-12 detail-time-location mb-10">
                    <i class="fa fa-mobile"></i>Mandal
                    <i class="fa fa-clock"></i> 14:00
                </div>

                <div class="col-md-12 mb-10">
                    <button type="submit" class="btn btn-black" @click="this.$router.push('/dashboard')">
                        List
                    </button>
                </div>
                <div class="col-md-12 mb-10">
                    <button type="submit" class="btn btn-black" @click="this.$router.push('/editproduct/1')">
                        Edit
                    </button>
                </div>
                <div class="col-md-12 mb-10">
                    <button type="submit" class="btn btn-black" @click="this.$router.push('/message/1')">
                        Message
                    </button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "ProductDetail",
    data() {
        return {
            //
        }
    },
    created() {
    },
    methods: {

    },
    beforeRouteEnter(to, from, next) {
        if (!window.Laravel.isLoggedin) {
            window.location.href = "/login";
        }
        next();
    }
}
</script>
