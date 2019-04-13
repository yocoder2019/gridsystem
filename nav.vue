<template>
    <!DOCTYPE html>
    <html lang="en">

    <head>
        <meta charset="UTF-8">
        <title>Grid layout example</title>
        <link href="https://fonts.googleapis.com/css?family=Open+Sans:400,600" rel="stylesheet">
    </head>
    <header>
        <nav>
            <!-- logo -->
            <div class="logo">
                <a href="">eTiqets</a>
            </div>
            <!-- search form -->
            <div class="search">
                <form action="">
                    <span class="search-flex-block">
                        <img src="https://image.flaticon.com/icons/svg/808/808731.svg" class="search-svg" height="44" width="44" alt="">
                        <input type="text" id="search-field" placeholder="Search event, places, adventure parks">
                    </span>
                </form>
            </div>
            <div class="responsive-section">
                <!-- help -->
                <div class="help">
                    <img src="assets/help.svg" alt="">
                    <div><a href="">Help</a></div>
                </div>
                <!-- user account-->
                <div class="account">
                    <img src="https://image.flaticon.com/icons/svg/118/118781.svg" alt="">
                    <div><a href="">Account</a></div>
                </div>
                <!-- cart -->
                <div class="cart">
                    <img src="https://image.flaticon.com/icons/svg/70/70369.svg" alt="">
                    <div><a href="">Cart</a></div>
                </div>
            </div>
        </nav>
    </header>

    <body>
    </body>

    </html>
</template>
<script>
</script>
<style>
/* general layout */
body {
    margin: 0 auto !important;
    font-family: 'Open Sans', sans-serif;
    background: #F0F0F0;


    display: grid;

    grid-template-areas:
    "header header header";

    grid-template-rows: 80px 1fr 15%







}

h1,
h2,
h3,
h4,
h5,
h6 {
    font-family: 'Crimson Text', serif;
}

header {
    grid-area: header;
    width: 100% !important;
    background-color: #fec200 !important;
    /*background-color: #03a9f4de;*/
}

/* smart phone & tablet portrait */
nav>div {
    /*text-transform: uppercase;*/
    font-size: .9em;
    padding: 1rem 1rem;
}

nav {
    display: grid;
    justify-items: start;
    text-align: center;
    box-shadow: 0 0 5px 0 #929774;
}

div>img {
    width: 1.7em;
    height: 1.4em;
    color: white;
    padding-right: 5px;
}

div>a {
    text-decoration: none;
    font-weight: 600;
    /*color: #292A29;*/
    color: white;
}

div>img {
    width: 1.6em;
    height: 1.2em;
    color: white;
    padding-right: 5px;
}

*, input[type=search] {
    box-sizing: border-box;
}

div {
    display: block;
    width:
}

.logo {
    text-align: center;
    font-size: 30px;
    letter-spacing: 3px;
    font-weight: 500;
}

.search {
    order: 4;
}

.search-flex-block {
    display: flex;

}

#search-field {
    background-color: #fffffff2;
    margin: 0;
    border: none;
    width: 28rem;
    border-top-right-radius: 5px;
    border-bottom-right-radius: 5px;
    text-rendering: auto;
    letter-spacing: normal;
    word-spacing: normal;
    text-indent: 0px;
    text-shadow: none;
    display: inline-block;
    text-align: start;
}


.search-svg {
    background-color: white;
    border-top-left-radius: 5px;
    border-bottom-left-radius: 5px;
    padding-left: 5px;
    padding-top: 5px;
    width: 25px;
    padding-right: 10px;
}

#search-field:focus {
    outline: none;
    color: #AAAFAA;
    font-size: 14px;
    letter-spacing: 1px;
}



#search-field::input::hover {
    background-color: #EBDAAD;
    cursor: pointer;
}

#search-field::placeholder {
    color: #AAAFAA;
    font-size: 13px;
    letter-spacing: .3px;
}

.search-btn {
    padding-bottom: 1px;
    border-top-right-radius: 5px;
    border-bottom-right-radius: 5px;
    margin-left: 1px;
    border-left: 5px solid #A2ACA4;
    background-color: white;
    color: #848D86;
    cursor: pointer;
    border: none;
    font-size: .9em;
    font-weight: 600;
}

.help {

    cursor: pointer;
}

.account {

    cursor: pointer;
}

.cart {

    cursor: pointer;
}

.responsive-section {
    display: flex;
    line-height: 1.1rem;
}

.responsive-section>div {
    padding-right: 2rem;
}


@media (max-width: 52rem) {
    nav {
        display: grid;
        grid-template-columns: 1fr auto auto auto;
    }

    .search {
        display: none;
    }

    nav>div {
        text-align: center;
        justify-items: center;
    }
}


@media (max-width: 20rem) {
    nav {
        display: grid;
        grid-template-columns: 1fr auto auto auto;
    }

    .search {
        display: none;
    }

    div>img {
        display: none;
    }

    nav>div {
        text-align: center;
        justify-items: center;
    }
}



/* desktop, laptop, landscape tablets */

@media (min-width: 52rem) {

    nav>div {
        display: grid;
        justify-items: center;
        text-align: center;
        color: white;
    }

    nav {
        grid-template-columns: 1fr 250fr auto auto;
    }

    .responsive-section {
        display: flex;
        flex-wrap: nowrap;
        align-items: flex-start;
        justify-content: space-around;
        color: white;
    }

    .search {
        order: 0;
        max-width: 20rem;
    }



}
</style>
