<template>
    <div class="messages">
        <!-- Header -->
        <el-row>
            <el-col :xs="2" :sm="2" :md="2" :lg="2" :xl="2">
                <el-button @click="goBack()" class="back_button" type="danger" circle
                           icon="el-icon-d-arrow-left"></el-button>
            </el-col>
            <el-col :xs="24" :sm="24" :md="24" :lg="24" :xl="24">
                <h1 style="margin-left: 50px">Messages</h1>
            </el-col>
        </el-row>

        <!-- Content -->
        <el-row type="flex" justify="center">
            <el-col :xs="24" :sm="20" :md="16" :lg="12" :xl="12">
                <div class="block" style="overflow:auto; min-height: 70vh">

                    <loading :active="loaderLoading"
                             :is-full-page="loaderFullPage"
                             :color="loaderColor"
                             :opacity="loaderOpacity"
                             :height="loaderHeight"
                             :width="loaderWidth"
                             :loader="loaderStyle"></loading>

                    <transition name="el-zoom-in-bottom">
                        <el-timeline class="messages_timeline" v-show="showTimeline">

                            <el-timeline-item>
                                <el-card>
                                    <el-image :src="img1" @load="onImgLoad"></el-image>
                                    <h3>This is the photo i took when we played genshin impact, in your pot</h3>
                                </el-card>
                            </el-timeline-item>

                            <el-timeline-item>
                                <el-card>
                                    <el-image :src="img2" @load="onImgLoad"></el-image>
                                    <h3>This is a photo I took in December 2021 when we first met</h3>
                                </el-card>
                            </el-timeline-item>

                            <el-timeline-item>
                                <el-card>
                                    <el-image :src="img3" @load="onImgLoad"></el-image>
                                    <h3>This is a photo I took when I was at the South Square in Yogyakarta</h3>
                                </el-card>
                            </el-timeline-item>

                            <el-timeline-item>
                                <el-card>
                                    <el-image :src="img4" @load="onImgLoad"></el-image>
                                    <h3>This is the photo I took when you bought the comic :3</h3>
                                </el-card>
                            </el-timeline-item>

                            <el-timeline-item>
                                <el-card>
                                    <el-image :src="img5" @load="onImgLoad"></el-image>
                                    <h3>Ini Juga</h3>
                                </el-card>
                            </el-timeline-item>

                            <el-timeline-item>
                                <el-card>
                                    <el-image :src="img6" @load="onImgLoad"></el-image>
                                    <h3>tiny </h3>
                                </el-card>
                            </el-timeline-item>

                            <el-timeline-item>
                                <el-card>
                                    <el-image :src="img7" @load="onImgLoad"></el-image>
                                    <h3>This is a photo from the solo matsuri, nice to meet you and your friends.. thank you</h3>
                                </el-card>
                            </el-timeline-item>
 <el-timeline-item>
                                <el-card>
                                    <el-image :src="img9" @load="onImgLoad"></el-image>
                                    <h3>Years by years you passed your birthday, you have grown into a fine woman btw</h3>
                                </el-card>
                            </el-timeline-item>

                            <el-timeline-item>
                                <el-card>
                                    <el-image :src="img10" @load="onImgLoad"></el-image>
                                    <h3>Well this is a photo of us.. that day i hope it will last forever.. anyway, I am rooting for your happiness. Ganbatte Hwaiting!! </h3>
                                </el-card>
                            </el-timeline-item>
                            <el-timeline-item>
                                <el-card>
                                    <el-image :src="img8" @load="onImgLoad"></el-image>
                                    <h3>And this is yesterday's photo at Mangafest UGM, thank you very much for accompanying me, the last one before the annoying kkn </h3>
                                </el-card>
                            </el-timeline-item>
     <el-timeline-item>
                                <el-card>
                                    <el-image :src="img11" @load="onImgLoad"></el-image>
                                    <h3>this flower is beautiful and pretty like you</h3>
                                </el-card>
                            </el-timeline-item>
                           

                            <el-timeline-item>
                                <el-card>
                                    <el-image :src="img12" @load="onImgLoad"></el-image>
                                    <h3>this is you and you are a beautiful woman, don't be insecure anymore.. :)</h3>
                                </el-card>
                            </el-timeline-item>

                             <el-timeline-item>
                                <el-card>
                                    <h3>Today is as beautiful as other days, but you realize another year has gone in a blink of the eye however</h3>
                                    <h3>Do you know..? today is just special, so special to you.. That's why</h3>
                                    <h3>Let's make the best celebration ever and let me share a piece of happiness to you</h3>
                                    <h3>I made all this as a birthday present to you</h3>
                                    <h3>Thanks for being there</h3>
                                    <h3>Thanks for the friendship and relationship we made</h3>
                                    <h3>Thanks for everything</h3>
                                    <h3>I wish you all the best, May your life be at ease, May all your wishes come true and Remember..</h3>
                                    <h3>Your ambitions, you live as a free bird flying in the blue sky is because God has your back</h3>
                                    <h3>This year will be better and I hope you'll find happiness along the way, keep your spirit up, enjoy every single moment with your most beautiful smile... ahh and make it the best memory</h3>
                                    <h3>Lastly...</h3>
                                </el-card>
                            </el-timeline-item>

                            <el-timeline-item>
                                <el-card>
                                    <h3>A Very Happy Birthday to You SharonClaudy</h3>
                                </el-card>
                            </el-timeline-item>

                        </el-timeline>
                    </transition>
                </div>
            </el-col>
        </el-row>
    </div>
</template>

<script>
    // Loading effect component
    import Loading from 'vue-loading-overlay';
    import 'vue-loading-overlay/dist/vue-loading.css';
   
    import img1 from '../assets/1.jpg'
    import img2 from '../assets/2.jpg'
    import img3 from '../assets/3.jpg'
    import img4 from '../assets/4.jpg'
    import img5 from '../assets/5.jpg'
    import img6 from '../assets/6.jpg'
    import img7 from '../assets/7.jpg'
    import img8 from '../assets/8.jpg'
    import img9 from '../assets/9.jpg'
    import img10 from '../assets/10.jpg'
    import img11 from '../assets/11.jpg'
     import img12 from '../assets/12.jpg'

    export default {
        name: "Messages",
        data() {
            return {
                // Display Timeline
                showTimeline: false,
                // Images
                // TODO : Modify the variables to cooperate with your images
                img1: img1,
                img2: img2,
                img3: img3,
                img4: img4,
                img5: img5,
                img6: img6,
                img7: img7,
                img8: img8,
                img9: img9,
                img10: img10,
                img11: img11,
                img12: img12,
                imagesLoaded: 0,
                
                totalImages : 11,
                // Loader
                loaderLoading: true,
                loaderColor: "#dd6161",
                loaderOpacity: 1,
                loaderStyle: "dots",
                loaderHeight: 60,
                loaderWidth: 60,
                loaderFullPage: false
            }
        },
        components: {
            Loading
        },
        methods: {
            goBack() {
                this.$router.go(-1);
            },
            onImgLoad() {
                this.imagesLoaded += 1;
                if (this.imagesLoaded === this.totalImages) {
                    console.log("Images Loaded");
                    setTimeout(() => this.loaderLoading = false, 500);
                    setTimeout(() => this.showTimeline = true, 800);
                }
            }
        }
    }
</script>

<style scoped>
    .messages_timeline {
        width: 80%;
        height: 83vh;
        margin-left: auto;
        margin-right: auto;
        
    }

    .back_button {
        margin-top: 15px;
        position: absolute;
    }
</style>
