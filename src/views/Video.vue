<template>
<VideoContainer />
</template>

<script>
import VideoContainer from "../components/VideoContainer.vue"
import axios from "axios"
export default {
    name: "Video",

    components: {
        VideoContainer
    },

    data() {
        return {
        roomId: null,
        buttonContainer : document.getElementsByClassName("button-container")
        }
    },

    async created() {
        const config = {headers: {'Access-Control-Allow-Origin': '*'}};
        this.roomId = await axios.get("http://localhost:3030", config).then(result => result.data.roomId)
        console.log(this.roomId)
        
    }
}
</script>

<style lang="scss" scoped>
</style>