<template>
    <div class="modal" v-if="showBlock" @click="stopTimer">
        <h1>Click to close ...</h1>

    </div>
</template>

<script>
export default {
    props: ['delay','isPlaying'],
    data() {
        return {
            showBlock: false,
            timer: null,
            reactionTime: 0,
        }
    },
    mounted() {
        console.log("Beggining to mount...", this.delay)
        setTimeout(() =>{
            this.showBlock=true
            this.startTimer()
        }, this.delay)
    },
    methods: {
        startTimer(){
            this.timer = setInterval(() =>{
                this.reactionTime += 10
            },10)
        },
        stopTimer() {
            clearInterval(this.timer)
            this.$emit("end",this.reactionTime)
        }
    }


}
</script>

<style>
.modal{
    width: 400px;
    background: greenyellow;
    margin:100px auto;
    padding: 20px;
    border-radius: 10px;
    color: white;
}

</style>