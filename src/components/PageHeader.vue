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
                <li><a class="header__link" href="#">Home</a></li>
                <li><a class="header__link" href="#">Series</a></li>
                <li><a class="header__link" href="#">Movies</a></li>
                <li><a class="header__link" href="#">OVA</a></li>
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
        <div class="header__profile">
            <img src="../assets/images/ProfileIMG.png" alt="" class="header__profile-pic">
        </div>

    </header>
</template>

<script setup>

</script>

<style lang="scss">
    .header{
        display: flex;
        padding: 1.25rem 13.375rem;
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
    .header__search{
        max-height: 1.25rem;
        color: white;
    }
</style>