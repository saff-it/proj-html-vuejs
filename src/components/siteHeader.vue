<template>
    <header>

        <nav class="container ms_top-header">

            <div class="ms_logo-container">
                <img src="../assets/img/white-logo-2.png" alt="Logo">
            </div>

            <div class="ms_nav-list">

                <ul>
                    <li>casa</li>
                    <li>casa</li>
                    <li>casa</li>
                </ul>

                <button>
                    Sign In
                </button>

            </div>
        </nav>

        <div class="ms_hero">

        </div>

    </header>
</template>

<script>
export default {

}
</script>

<style lang="scss">
@import "../styles/general.scss";
@import "../styles/variables.scss";


header{
    background-color: $colorBg9;
}

nav.ms_top-header{
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.ms_logo-container img{
    width: 75%;
    padding: 15px 0;
    
}

.ms_nav-list{
    display: flex;
    align-items: center;
    

    ul{
        list-style: none;
        margin: 0 30px;
        

        li{
           display: inline-block; 
           margin: 0 10px;
           color: white;
           
        }

    }

    button{
        border: none;
        border-radius: 20px;
        padding: 6px 18px;
        font-size: 0.9rem;
        background-color: $colorBg3;
    }
}

</style>