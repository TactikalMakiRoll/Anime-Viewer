<template>
    <div class="login">
        <a href="#">
            <img class="login__logo" src="../assets/images/logo.png" alt="Ani-viewer logo, link to home page">
        </a>
        <form class="login__form">
            <fieldset>
                <legend class="login__form-header">Log in</legend>
                <label class="login__form-label" for="email">email</label>
                <input class="login__form-input" type="text" id="email" name="user_email" />
                <label class="login__form-label" for="password">password</label> 
                <input class="login__form-input" type="password" id="password" name="user_password" />
            </fieldset>
            
            <button class="login__form-button" type="submit">Login</button>
            <div class="login__remember">
                <input type="checkbox" name="remember" id="remember"> 
                <label for="remember">Remember me?</label> 
                <a href="#">
                    <p>Need help?</p>
                </a>
            </div>

            <div class="login__socials">
                <a href="#"><img class="login__social" src="../assets/images/googleLogin.png" alt="google login"></a>
            </div>

        </form>
    </div>
</template>

<script setup></script>

<style lang="scss">
.login{
    min-width: 100vw;
    min-height: 100vw;
    background: linear-gradient(
          rgba(0, 0, 0, 0.7), 
          rgba(0, 0, 0, 0.7)
        ),
        url(../assets/images/loginBG.webp) center center no-repeat;
    
    padding: 45px 0 0 45px;

    &__logo{
        max-width: 169px;
    }

    &__form{
        margin-top:172px;
    }
}
body{
    color:white;
}
</style>
