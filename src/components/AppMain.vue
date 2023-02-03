<script>
export default {
    name: 'AppMain',
}
</script>

<template>
    <div>
        <span>Content goes here</span>
    </div>
</template>

<style lang="scss" scoped>
    div{
        display: flex;
        justify-content: center;
        align-items: center;

        height: calc(100vh - 150px - 600px);
        
        background-color: #191919;
        span{
            font-size: 30px;
            
            color: #FFFFFF;
        }
    }
</style>