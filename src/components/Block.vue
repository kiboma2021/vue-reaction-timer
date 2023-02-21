<template>
    <div class="backdrop">
        <div class="modal">
            <h1>Modal heading</h1>

        </div>
    </div>
  
</template>

<script>
export default {

}
</script>

<style>
.modal{
    width: 400px;
    background: greenyellow;
    margin:100px auto;
    padding: 20px;
    border-radius: 10px;    

}

.backdrop{
    top: 0;
    position: fixed;
    background: rgba(0, 0, 0, 0.486);
    width: 100%;
    height: 100%;
    margin-top: -2rem;


}

</style>