<template>

    <footer>

        <div class="row-1">

            <div class="container">

                <!-- Col left -->
                <div class="menu-list">

                    <div class="column">

                        <div>

                            <div class="title">{{menuList[0].title.toUpperCase()}}</div>
                            
                            <ul>
                                <li v-for='text,index in menuList[0].list' :key="index">
                                    {{text}}
                                </li>
                            </ul>
                        </div>

                        <div>

                            <div class="title">{{menuList[1].title.toUpperCase()}}</div>
                            
                            <ul>
                                <li v-for='text,index in menuList[1].list' :key="index">
                                    {{text}}
                                </li>
                            </ul>
                        </div>
                    </div>

                    <div class="column">

                        <div class="title">{{menuList[2].title.toUpperCase()}}</div>
                            
                        <ul>
                            <li v-for='text,index in menuList[2].list' :key="index">
                                {{text}}
                            </li>
                        </ul>
                    </div>

                    <div class="column">

                        <div class="title">{{menuList[3].title.toUpperCase()}}</div>
                            
                        <ul>
                            <li v-for='text,index in menuList[3].list' :key="index">
                                {{text}}
                            </li>
                        </ul>
                    </div>
                </div>

                <!-- Col right -->
                <div class="logo">
                    <img src="../assets/img/dc-logo-bg.png" alt="">
                </div>
            </div>

            
        </div>

        <div class="row-2">
            <div class="container">

            </div>
        </div>

    </footer>

</template>


<script>

    export default {

        name:"Footer",

        data: function(){
            return{
                menuList: [
                    {
                        title: 'DC Comics',
                        list : ['Character','Comics','Movies', 'TV', 'Games', 'Videos', 'News']
                    },
                    {
                        title: 'Shop',
                        list : ['Shop DC','Shop DC Collectibles']
                    },
                    {
                        title: 'DC',
                        list : ['Terms of Use', 'Privacy policy (New)', 'Ad Choice', 'Advertising', 'Jobs', ' Subscription', 'Talent Workshops', 'CPSC Certificates', 'Ratings', 'Shop Help','Contact Us']
                    },
                    {
                        title: 'Sites',
                        list : ['DC','MAD Magazine','DC Kids','DC Universe', 'DC Power Visa']
                    },
                ]
            }
        }
    }

</script>


<style scoped lang='scss'>

    @import "../style/mixin.scss";

    footer{  
        color:white
    }

    .row-1{

        background-image: url('../assets/img/footer-bg.jpg');
        height: 400px;
        overflow: hidden;
        
        .container{
            @include base-container;
            display: flex;
            justify-content: space-between;
            align-items: center; 
            height: 100%;
        }
    }  

    .row-2{
        background-color: #303030;
        height: 80px;
    }
    
    .title{
        font-family: 'Open Sans Condensed', sans-serif;
        font-size: 25px;
        margin: 10px 0;
    }

    .menu-list{
        display: flex;
    }

    .column{

        margin-right: 40px;

        ul{

            color: lightgrey;

            li{
                margin-top: 3px;
            }
        }
    }

</style>