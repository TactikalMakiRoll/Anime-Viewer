<template>
    <header class="header">
        <nav>
            <a href="#" class="header__logo">
                <img
                    class="logo"
                    src="../assets/images/logo.png"
                    alt="Ani-viewer logo, link to home page"
                />
            </a>
            <ul class="header__nav">
                <li class="header__link"><a href="#">Home</a></li>
                <li class="header__link"><a href="#">Series</a></li>
                <li class="header__link"><a href="#">Movies</a></li>
                <li class="header__link"><a href="#">OVA</a></li>
                <li>
                    <a class="header__link" href="#">
                        <img
                            class="header__search"
                            src="../assets/icons/search.svg"
                            alt="search link"
                        />
                    </a>
                </li>
            </ul>
        </nav>
        <div class="header__profile-container">
            <button class="header__profile">
                <img src="../assets/images/ProfileIMG.png" alt="" class="header__profile-pic">
            </button>
            <ul class="dropdown" aria-label="dropdown">
                <li class="dropdown__link">
                    <a href="#">
                        <img class="dropdown__icon" src="../assets/icons/account.svg" alt="">
                        Account
                    </a>
                </li>
                <li class="dropdown__link">
                    <a href="#">
                        <img class="dropdown__icon" src="../assets/icons/help.svg" alt="">
                        Help Center
                    </a>
                </li>
                <li class="dropdown__link dropdown__link--sign"><a href="#">Sign out</a></li>

            </ul>
        </div>

    </header>
</template>

<script setup>

</script>

<style lang="scss">
    .header{
        display: flex;
        padding: 1.25rem 13.375rem;
        justify-content: space-between;
    }
    .header__logo{
        margin-right: 3.125rem;
    }
    .header__nav{
        display: inline-flex;
    }
    .header__link{
        text-decoration: none;
        font-weight: bold;
    }
    
    .header__link:hover{
        text-decoration: underline;
    }

    .header__link + .header__link{
        margin-left:1.25rem;
    }

    .header__search{
        max-height: 1.25rem;
        color: white;
    }

    .header__profile-container{
        position: relative;
    }

    .header__profile:hover{
        cursor: pointer;
    }

    .header__profile-pic{
        vertical-align: middle;
    }
    
    .header__profile::after{
        content: "▼";
        color:white;
        vertical-align: middle;
        margin-left: 5px;
    }

    .dropdown{
        min-width: 12rem;
        position: absolute;
        left:-100%;
        visibility: hidden;
        background-color: rgba(0,0,0,0.7);
        box-shadow: 0 2px 5px 0 rgba(255,255,255,.1);
        font-weight: bold;
        transition: opacity 0.25s ease-in-out;
        opacity: 0;
        transform: translateY(-10px);
        transition: transform 0.15s ease-in-out;
        pointer-events: none;
    }
    
    .dropdown__link{
        padding: 0.875rem;
    }

    .dropdown__icon{
        height: 1.5rem;
        color: white;
        filter: invert(100%);
        vertical-align: middle;
        margin-right:5px;
    }

    .dropdown__link--sign{
        padding-top: 1rem;
        text-align: center;
        border-top: 2px solid white;
    }

    .dropdown__link:hover{
        background-color: rgba(127, 90, 240,0.3);
        cursor: pointer;
    }

    .header__profile:focus ~ .dropdown{
        visibility: visible;
        opacity: 1;
        display: block;
        transform: translateY(0);
        pointer-events: auto;
    }
    
</style>