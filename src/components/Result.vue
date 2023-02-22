<template>
  <div>
    <h1>The result is {{score}} ms</h1>
    <h2>{{ this.rank }}</h2>
  </div>
</template>

<script>

export default {
    props: ['score'],
    data() {
        return {
            rank: null,
        }
    },
    mounted() {
        if (this.score < 600){
            this.rank = "Very good work Ben"
        }
        else if (this.score <1000) {
            this.rank = "Good work, though you can do better"
        }
        else {
            this.rank = "Too slow Ben"
        }
    }

}
</script>

<style>

</style>