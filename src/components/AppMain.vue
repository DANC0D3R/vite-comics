<script>
import Button from './Button.vue'
import Card from './Card.vue'
export default {
    name: 'AppMain',
    components: { Button, Card },
    data() {
        return {
            ButtonText: 'Load more'
        }
    },
    props: {
        comics: Array
    }
}
</script>

<template>
    <div>
        <div class="jumbo">
            <img src="../assets/img/jumbotron.jpg" alt="jumbotron">
        </div>
        <div class="container">
            <h2>Current series</h2>
            <!-- Card Section -->
            <div class="card-section">
                <!-- Card -->
                <Card v-for="comic in comics"></Card>
            </div>
            <div class="text-center">
                <Button :text="ButtonText"></Button>
            </div>
        </div>
    </div>
</template>

<!-- Stile -->
<style lang="scss" scoped>
@use '../assets/scss/variables' as *;
.jumbo {
    height: 350px;

    overflow: hidden;
    img {
        width: 100%;
    }
}
h2 {
    display: inline-block;
    transform: translateY(-50%);

    padding: 5px 10px;
    
    font-weight: bold;
    text-transform: uppercase;

    color: #FFFFFF;
    background-color: var(--dc-blue);
}
.card-section {
        display: flex;
        flex-wrap: wrap;
}
.text-center {
    text-align: center;
}
</style>