<template>
    <section>

        <div class="container">
            <ul>
                <li v-for='icon,index in icons' :key='index'>
                    <img :src="require('../assets/img/' + icon.src)" alt="">
                    <span>{{icon.text.toUpperCase()}}</span>
                </li>
            </ul>
            
        </div>   
    </section>
</template>

<script>
export default {
    name:"PreFooter",
    data: function(){
        return{
            icons: [
                {
                    src:'buy-comics-digital-comics.png',
                    text: 'Digital Comics'
                },
                {
                    src:'buy-comics-merchandise.png',
                    text: 'DC Merchandise'
                },
                {
                    src:'buy-comics-shop-locator.png',
                    text: 'Subscription'
                },
                {
                    src:'buy-comics-subscriptions.png',
                    text: 'Comic Shop Locator'
                },
                {
                    src:'buy-dc-power-visa.svg',
                    text: 'CDC Power Visa'
                }
            ]
        }
    }

}
</script>

<style scoped lang='scss'>

    @import "../style/variables.scss";
    @import "../style/mixin.scss";

    section{
        height: 150px;
        background-color: $brand_primary_color;

        display: flex;
        justify-content: center;
        align-items: center;
    }

    .container{

        @include base-container;

        ul{
            display: flex;
            justify-content: center;
            align-items: center;

            li{
                margin: 0 30px;
                font-size: 15px ;
                font-family: sans-serif;

                display: flex;
                justify-content: center;
                align-items: center;

                color: white;

                img{
                    width: 50px;
                    
                    margin-right: 15px;
                }
            }
        }
    }

</style>