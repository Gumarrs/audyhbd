<template>
    <div class="video">
        <!-- Header -->
        <el-row>
            <el-col :xs="2" :sm="2" :md="2" :lg="2" :xl="2">
                <el-button @click="goBack()" class="back_button" type="danger" circle
                           icon="el-icon-d-arrow-left"></el-button>
            </el-col>
            <el-col :xs="24" :sm="24" :md="24" :lg="24" :xl="24">
                <h1>Video</h1>
            </el-col>
        </el-row>

        <!-- Content -->
        <div class="block" style="overflow:auto;">
            <youtube class="player" :video-id="videoId" ref="youtube" :width="540" :height="960"></youtube>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Video",
        data(){
            return {
                videoId : 'RaeLAwacDG4'
            }
        },
        methods: {
            goBack() {
                this.$router.go(-1);
            }
        }
    }
</script>

<style scoped>
    .back_button {
        margin-top: 15px;
        position: absolute;
    }
</style>