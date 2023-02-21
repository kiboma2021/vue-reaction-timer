<template>
    <div class="backdrop">
        <div class="modal">
            <h1>Click to close ...</h1>

        </div>
    </div>
  
</template>

<script>
export default {
    props: ['delay'],
    methods: {}

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

.backdrop{
    top: 0;
    position: fixed;
    background: rgba(0, 0, 0, 0.486);
    width: 100%;
    height: 100%;
  


}

</style>