<template>
    <div class="page-wrapper">
        <div class="big-dot"></div>
        <div class="page-container">
            <div class="login-header">
                <div class="text-center" style="margin: 20px 0px 20px 0px;">
                    <a href="#" @click="this.$router.push('/message/1')">
                        <img class="logo-image" src="../img/logo.png" />
                    </a>
                </div>

                <nav class="navbar navbar-expand-lg navbar-light">
                    <div class="collapse navbar-collapse" v-if="!isLoggedIn">
                        <router-link to="/login" class="nav-item nav-link">login</router-link>
                        <router-link to="/register" class="nav-item nav-link">Register</router-link>
                    </div>

                    <div class="navbar-collapse" v-else>
                        <div class="message-menu">
                            <a href="#" v-on:click.prevent="showMessageDropDown=!showMessageDropDown; showDropDown=false;">
                                <i class="fa fa-envelop"></i>
                                <img src="../img/envelope-regular.svg" />
                            </a>

                            <transition name="slide-fade2">
                                <div class="popup w4 mt1" v-if="showMessageDropDown">
                                    <ul class="menu list pl0 pa0 ma0">
                                        <li class="list">
                                            <a href="#" class="dd-link pointer hover-bg-moon-gray" @click="showMessageDropDown=!showMessageDropDown; this.$router.push('/message/1')" > 
                                                <div class="message-pop-row unread">
                                                    <div class="left-side">
                                                        <img src="../img/avarta2.jpg" />
                                                    </div>
                                                    <div class="right-side">
                                                        <div class="username">Panda</div>
                                                        <div class="message-line">I dont understand your requirements.</div>
                                                    </div>
                                                </div>
                                            </a>
                                        </li>

                                        <li class="list">
                                            <a href="#" class="dd-link pointer hover-bg-moon-gray" > 
                                                <div class="message-pop-row">
                                                    <div class="left-side">
                                                        <img src="../img/avarta1.jpg" />
                                                    </div>
                                                    <div class="right-side">
                                                        <div class="username">tigress</div>
                                                        <div class="message-line">how are you? I have on question.</div>
                                                    </div>
                                                </div>
                                            </a>
                                        </li>
                                        <li class="list">
                                            <a href="#" class="dd-link pointer hover-bg-moon-gray" > 
                                                <div class="message-pop-row">
                                                    <div class="left-side">
                                                        <img src="../img/avarta1.jpg" />
                                                    </div>
                                                    <div class="right-side">
                                                        <div class="username">tigress</div>
                                                        <div class="message-line">how are you? I have on question.</div>
                                                    </div>
                                                </div>
                                            </a>
                                        </li>
                                        <li class="list">
                                            <a href="#" class="dd-link pointer hover-bg-moon-gray" > 
                                                <div class="message-pop-row">
                                                    <div class="left-side">
                                                        <img src="../img/avarta1.jpg" />
                                                    </div>
                                                    <div class="right-side">
                                                        <div class="username">tigress</div>
                                                        <div class="message-line">how are you? I have on question.</div>
                                                    </div>
                                                </div>
                                            </a>
                                        </li>
                                        <li class="list">
                                            <a href="#" class="dd-link pointer hover-bg-moon-gray" > 
                                                <div class="message-pop-row">
                                                    <div class="left-side">
                                                        <img src="../img/avarta1.jpg" />
                                                    </div>
                                                    <div class="right-side">
                                                        <div class="username">tigress</div>
                                                        <div class="message-line">how are you? I have on question.</div>
                                                    </div>
                                                </div>
                                            </a>
                                        </li>
                                        <li class="list">
                                            <a href="#" class="dd-link pointer hover-bg-moon-gray" > 
                                                <div class="message-pop-row">
                                                    <div class="left-side">
                                                        <img src="../img/avarta1.jpg" />
                                                    </div>
                                                    <div class="right-side">
                                                        <div class="username">tigress</div>
                                                        <div class="message-line">how are you? I have on question.</div>
                                                    </div>
                                                </div>
                                            </a>
                                        </li>
                                    </ul>
                                </div>
                            </transition>
                        </div>

                        <div class="profile-menu">
                            <a href="#" v-on:click.prevent="showDropDown=!showDropDown; showMessageDropDown=false;">
                                <img src="../img/avarta1.jpg" />
                            </a>

                            <transition name="slide-fade">
                                <div class="popup w4 mt1" v-if="showDropDown">
                                    <ul class="menu list pl0 pa0 ma0">
                                        <li class="list">
                                            <a href="#" class="dd-link pointer hover-bg-moon-gray" @click="showDropDown=!showDropDown; this.$router.push('/addproduct')"> My List</a>
                                        </li>
                                        <li class="list">
                                            <a href="#" class="dd-link pointer hover-bg-moon-gray" @click="showDropDown=!showDropDown; this.$router.push('/myproduct')"> List</a>
                                        </li>
                                        <li class="list">
                                            <a href="#" class="dd-link pointer hover-bg-moon-gray" @click="showDropDown=!showDropDown; this.$router.push('/setting')"> Setting</a>
                                        </li>
                                        <li class="list">
                                            <a href="#" class="dd-link pointer hover-bg-moon-gray" @click="logout"> Logout</a>
                                        </li>
                                    </ul>
                                </div>
                            </transition>
                        </div>
                        <!-- router-link to="/books" class="nav-item nav-link">Avatar</router-link>
                        <a class="nav-item nav-link" style="cursor: pointer;" @click="logout">Logout</a -->
                    </div>
                </nav>
            </div>

            <router-view/>

            <div class="col-md-12" v-if="isLoggedIn">
                <div class="col-md-12 footer">
                    <div class="foot-letter mb-10">
                        <span>Privacy Policy</span>
                        <span>Inquiries</span>
                    </div>
                    <div class="foot-letter">© 2021 EKIMA</div>
                </div>
            </div>
            
        </div>
        <div class="phone-receiver"></div>
    </div>
</template>

<script>

export default {
    name: "App",
    components: {
        
    },

    data() {
        return {
            isLoggedIn: false,
            showDropDown: false,
            messages: [],
            showMessageDropDown: false
        }
    },
    created() {
        if (window.Laravel.isLoggedin) {
            this.isLoggedIn = true
        }
    },
    methods: {
        logout(e) {
            this.showDropDown=!this.showDropDown;

            e.preventDefault()
            this.$axios.get('/sanctum/csrf-cookie').then(response => {
                this.$axios.post('/api/logout')
                    .then(response => {
                        if (response.data.success) {
                            window.location.href = "/login";
                        } else {
                            console.log(response)
                        }
                    })
                    .catch(function (error) {
                        console.error(error);
                    });
            })
        }
    },
}
</script>
