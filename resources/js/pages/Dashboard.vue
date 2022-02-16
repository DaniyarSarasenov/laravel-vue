<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-md-12">
                <div class="col-md-12 page-title">
                    Preparing
                </div>
            </div>

            <div class="col-md-12 page-content">
                <div class="col-md-6 col-sm-6 col-image">
                    <router-link :to="{name: 'productdetail', params: { id: 1 }}">
                        <img class="product-image" src="../../img/product_default.jpg"/>
                        <div class="time-location">
                            13:00 TailWind
                        </div>
                    </router-link>
                </div>
                <div class="col-md-6 col-sm-6 col-image">
                    <img class="product-image" src="../../img/product_default.jpg"/>
                    <div class="time-location">
                        13:01 TailWind
                    </div>
                </div>
                <div class="col-md-6 col-sm-6 col-image">
                    <img class="product-image" src="../../img/product_default.jpg"/>
                    <div class="time-location">
                        13:00 TailWind
                    </div>
                </div>
                <div class="col-md-6 col-sm-6 col-image">
                    <img class="product-image" src="../../img/product_default.jpg"/>
                    <div class="time-location">
                        13:00 TailWind
                    </div>
                </div>
                <div class="col-md-6 col-sm-6 col-image">
                    <img class="product-image" src="../../img/product_default.jpg"/>
                    <div class="time-location">
                        13:00 TailWind
                    </div>
                </div>
                <div class="col-md-6 col-sm-6 col-image">
                    <img class="product-image" src="../../img/product_default.jpg"/>
                    <div class="time-location">
                        13:00 TailWind
                    </div>
                </div>
                <div class="col-md-6 col-sm-6 col-image">
                    <img class="product-image" src="../../img/product_default.jpg"/>
                    <div class="time-location">
                        13:00 TailWind
                    </div>
                </div>
                <div class="col-md-6 col-sm-6 col-image">
                    <img class="product-image" src="../../img/product_default.jpg"/>
                    <div class="time-location">
                        13:00 TailWind
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Dashboard",
    data() {
        return {
            name: null,
        }
    },
    created() {
        if (window.Laravel.user) {
            this.name = window.Laravel.user.name
        }
    },
    beforeRouteEnter(to, from, next) {
        if (!window.Laravel.isLoggedin) {
            window.location.href = "/login";
        }
        next();
    }
}
</script>
