<template>
    <div class="content">
        <div class="content__container content__container--right">
            <div class="content__textcontainer">
                <div class="content__text">
                    <h1 class="content-typography__large">"Hey B whats poppin?"</h1>
                </div>
            </div>
            <div class="content__imagecontainer" id="image1">
            </div>
        </div>
        <div class="content__container content__container--left">
            <div class="content__imagecontainer" id="image2">
            </div>
            <div class="content__textcontainer">
                <div class="content__text">
                    <p class="content-typography__text">
                        Everyday im Hustelin
                        Everyday im Hustelin
                        Everyday im Hustelin
                        Everyday im Hustelin
                        Everyday im Hustelin
                        Everyday im Hustelin
                        Everyday im Hustelin
                        Everyday im Hustelin
                        Everyday im Hustelin
                        Everyday im Hustelin
                    </p>
                </div>
            </div>
        </div>
        <div class="content__container content__container--right">
            <div class="content__textcontainer">
                <div class="content__text">
                    <p class="content-typography__text">We ballin</p>
                </div>
            </div>
            <div class="content__imagecontainer" id="image3">
            </div>
        </div>
        <div id="instafeeder"></div>
    </div>
</template>

<script>
    $(function() {
        $('#image1').waypoint(function() {
            $('#image1').addClass('slidein-right');
        }, {
            offset: '50%'
        });
    });

    $(function() {
        $('#image2').waypoint(function() {
            $('#image2').addClass('slidein-left');
        }, {
            offset: '50%'
        });
    });

    $(function() {
        $('#image3').waypoint(function() {
            $('#image3').addClass('slidein-right');
        }, {
            offset: '50%'
        });
    });

    import { mapGetters } from 'vuex';
    import { mapMutations } from 'vuex';
    import { mapActions } from 'vuex';

    export default {
        data() {
            return {
                loading: false,
            }
        },
        methods: {
            loadInstagram: function() {
                this.$store.dispatch('asyncChangeInstagram');
            },
        },
//        computed: {
//            ...mapGetters([
//                'getGithubName',
//                'getGithubAvatar',
//                'getGithubCompany',
//                'getGithubLocation',
//                'getGithubLoading'
//            ]),
//        },
        mounted: function() {
            this.loadInstagram();
        }
    }
</script>
