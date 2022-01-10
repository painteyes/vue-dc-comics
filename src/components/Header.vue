<template>

    <div class="container">

        <div class="logo">
            <img src="../assets/img/dc-logo.png" alt="">
        </div>

        <div class="navbar">

            <ul>

                <li 
                v-for='item,index in navbarItems' :key="index"
                :class="{'current':item.current}"
                @mouseenter="item.current=true"
                @mouseleave="item.current=false"
                >
                    {{item.text.toUpperCase()}}
                </li>

            </ul>

        </div>

    </div>

</template>

<script>

    export default {
        name:"Header",
        data: function(){
            return {
                navbarItems: [
                    {
                        text:'Characters',
                        current: false,
                    },
                    {
                        text:'Comics',
                        current: false,
                    },
                    {
                        text:'Movies',
                        current: false,
                    },
                    {
                        text:'TV',
                        current: false,
                    },
                    {
                        text:'Games',
                        current: false,
                    },
                    {
                        text:'Collectibiles',
                        current: false,
                    },
                    {
                        text:'Videos',
                        current: false,
                    },
                    {
                        text:'Fans',
                        current: false,
                    },
                    {
                        text:'News',
                        current: false,
                    },
                    {
                        text:'Shop',
                        current: false,
                    }

                ]
            }
        }
    }
    
</script>

<style scoped lang='scss'>

    @import "../style/variables.scss";
    @import "../style/mixin.scss";
    
    .container{
        @include base-container;
        background-color: white;
        height: 150px;
        display: flex;
        align-items: center;
        justify-content: space-between  
    };

    .logo{
        width: 10% ;
        max-width: 80px;
        float: left;
    }

    .navbar{

        width: 90% ;
        float: left;
        height: 100%;

        ul{
            text-align: right;
            
            li{
                min-width: 30px;
                text-align: center;
                font-family: 'Open Sans Condensed', sans-serif;
                line-height: 145px;
                display: inline-block;
                margin: 0 20px;
                cursor: pointer;              
                
                &.current{
                    border-bottom: 5px solid $brand_primary_color;  
                    color: $brand_primary_color;
                }
            } 
        }
    }
    
</style>