<template>
    <div class="container">
        <div class="row page-content">
            <div class="col-md-12" style="padding: 0px 20px">
                <div class="message-header mt-10">
                    <div class="col-image message-image-wrapper">
                        <img src="../../img/product_default.jpg" class="mesage-image" />
                        <div class="time-location">
                            19:00 TailWind
                        </div>
                    </div>

                    <div class="message-function">
                        <button class="btn btn-black btn-white">???</button>

                        <div class="header-bottom-des">Message Here</div>
                    </div>
                </div>

                <div class="message-container">
                    <div class="message-row">
                        <div class="message-content other-message">
                            <div class="message-left flex-4">
                                <img src="../../img/avarta1.jpg" class="user-avarta"/>
                                <div class="username">Tigress</div>
                            </div>
                            <div class="message-right flex-8">
                                Hello, How are you?
                            </div>
                        </div>
                    </div>

                    <div class="message-row">
                        <div class="message-content mine">
                            <div class="message-left flex-4">
                                <img src="../../img/avarta2.jpg" class="user-avarta"/>
                                <div class="username">Panda</div>
                            </div>
                            <div class="message-right flex-8">
                                Hello, How are you?
                            </div>
                        </div>
                    </div>
                    <div class="message-row">
                        <div class="message-content mine">
                            <div class="message-left flex-4">
                                <img src="../../img/avarta2.jpg" class="user-avarta"/>
                                <div class="username">Panda</div>
                            </div>
                            <div class="message-right flex-8">
                                Hello, How are you?
                            </div>
                        </div>
                    </div>
                    <div class="message-row">
                        <div class="message-content mine">
                            <div class="message-left flex-4">
                                <img src="../../img/avarta2.jpg" class="user-avarta"/>
                                <div class="username">Panda</div>
                            </div>
                            <div class="message-right flex-8">
                                Hello, How are you?
                            </div>
                        </div>
                    </div>
                    <div class="message-row">
                        <div class="message-content mine">
                            <div class="message-left flex-4">
                                <img src="../../img/avarta2.jpg" class="user-avarta"/>
                                <div class="username">Panda</div>
                            </div>
                            <div class="message-right flex-8">
                                Hello, How are you?
                            </div>
                        </div>
                    </div>
                </div>

                <div class="message-send">
                    <input type="text" class="message-input" />
                    <button class="btn btn-black">Send</button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Message",
    data() {
        return {
            //
        }
    },
    created() {
    },
    methods: {}
}
</script>
