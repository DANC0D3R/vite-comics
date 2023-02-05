<script>
export default {
    name: 'Button',
    props: {
        text: String
    }
}
</script>

<template>
    <button>{{ text }}</button>
</template>

<style lang="scss" scoped>
@use '../assets/scss/variables' as *;
button{
    margin: 20px 0;
    padding: 5px 10px;

    font-size: 16px;
    font-family: $font-condensed;
    font-weight: bold;
    text-transform: uppercase;

    color: #FFFFFF;
    background-color: var(--dc-blue);

    cursor: pointer;
}
</style>