<template>
    <div class="modal" v-if="showBlock">
        <h1>Click to close ...</h1>

    </div>
</template>

<script>
export default {
    props: ['delay'],
    data() {
        return {
            showBlock: false,
        }
    },
    mounted() {
        console.log("Beggining to mount...", this.delay)
        setTimeout(() =>{this.showBlock=true}, this.delay)
    },
    updated() {
        console.log("Updated......")
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