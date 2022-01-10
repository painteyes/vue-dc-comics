<template>

    <div class="cover">

        <div class="cover-image">
            <img :src="coverObject.thumb" :alt="coverObject.series">
        </div>

        <div class="cover-title">
            {{ coverObject.series }}
        </div>

    </div>
    
</template>


<script>

    export default {
        name: 'Cover',
        props: ['coverObject']
    }

</script>


<style scoped lang="scss">

    .cover {

        width: calc((100% / 6) - 20px);
        margin: 20px 10px;  
        display: flex;
        flex-direction: column;
        
        .cover-image {
            height: 200px;
            overflow: hidden;
            margin: auto;
        }

        .cover-title {
            color: white;
            text-transform: uppercase;
            font-size: 13px;
            margin: 10px auto;
    
        }
    }

</style>