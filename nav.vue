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
                <ul>
                    <!-- help -->
                    <li class="help">
                        <img src="https://image.flaticon.com/icons/svg/906/906794.svg" alt="">
                        <div><a href="">Help</a></div>
                    </li>
                    <!-- user account-->
                    <li class="account">
                        <img src="https://image.flaticon.com/icons/svg/118/118781.svg" alt="">
                        <div><a href="">Account</a></div>
                    </li>
                    <!-- cart -->
                    <li class="cart">
                        <img src="https://image.flaticon.com/icons/svg/70/70369.svg" alt="">
                        <div><a href="">Cart</a></div>
                    </li>
                </ul>
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
    max-width: 1100px;
    margin: 0;
    margin: 0 auto !important;
    font-family: 'Open Sans', sans-serif;
    background: #F0F0F0;
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
    background-color: #fec200;
    /*background-color: #03a9f4de;*/
}



/* smart phone & tablet portrait */

nav {
    display: grid;
    grid-template-columns: 1fr auto auto auto;
    justify-items: start;
    text-align: center;
    box-shadow: 0 0 5px 0 #929774;
}

nav>div {

    /*text-transform: uppercase;*/
    font-size: .8em;
    padding: 1rem 1rem;
}


div {
    display: block;
    justify-content: space-between;
}

li { display: block; margin-left: 17px; }

div>a {
    text-decoration: none;
    font-weight: 600;
    /*color: #292A29;*/
    color: black;
    font-size: .9em;
}

li>img {
    width: 1.8em;
    height: 1.2em;

}

*,
input[type=search] {
    box-sizing: border-box;
}

* {box-sizing: border-box;}

.logo {
    text-align: center;
    font-size: 28px;
    letter-spacing: .2em;
}

.search {
    display: inline;
    max-width:100%;
    min-width: 280px;

}

.search-flex-block {
    display: flex;

}

#search-field {
    width: 500px;
    cursor: pointer;
    background-color: #fffffff2;
    margin: 0;
    border: none;
    border-top-right-radius: 5px;
    border-bottom-right-radius: 5px;
    text-rendering: auto;
    letter-spacing: normal;
    word-spacing: normal;
    text-indent: 0px;
    text-shadow: none;
    text-align: start;
}

.search-svg {
    background-color: white;
    border-top-left-radius: 5px;
    border-bottom-left-radius: 5px;
    padding-left: 5px;
    padding-top: 5px;
    width: 35px;
    padding-right: 10px;
}

#search-field:focus {
    outline: none;
    color: #AAAFAA;
    letter-spacing: 1px;
    height: auto;
    max-width: auto;
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

.responsive-section {
    display: flex;
    color: white;
    margin-bottom: -4px;
}

.responsive-section>ul, li {
    display: inline-flex;
    margin-bottom: -4px;
}

.help {
    cursor: pointer;
    margin-left: none;
}

.account {
    cursor: pointer;
}

.cart {
    cursor: pointer;
}



/* desktop, laptop, landscape tablets */

@media (min-width: 33rem) {

    nav>div {
        display: grid;
        justify-items: center;
        text-align: center;
    }

    nav {
        grid-template-columns: 1fr 4fr auto;
    }

    #search-field {
        cursor: pointer;
        background-color: #fffffff2;
        margin: 0;
        border: none;
        border-top-right-radius: 5px;
        border-bottom-right-radius: 5px;
        text-rendering: auto;
        letter-spacing: normal;
        word-spacing: normal;
        text-indent: 0px;
        text-shadow: none;
        text-align: start;
    }

    .search-field {
        width: 400px;
    }

    .responsive-section > ul {
        display: flex;
        list-style-type: none;
        text-align: center;
    }

    li {
        margin-left: 20px;
    }

    .help {
    cursor: pointer;
    margin-left: -40px;
}

}
</style>
