<template>
    <div class="container">
        <div class="row">
            
        </div>
    </div>
</template>
    
<script>
    import axios from 'axios';
    export default {
        name: 'AlbumsSection',
        mounted(){
            axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((res) =>{
                console.log(res.data);
            });
        }
    }
</script>

<style lang="scss" scoped></style>