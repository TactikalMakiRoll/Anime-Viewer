<template>
    <div class="login">
        <a href="#">
            <img class="login__logo" src="../assets/images/logo.png" alt="Ani-viewer logo, link to home page">
        </a>
        <div class="flex-center">
            <form class="login__form">
                <fieldset>
                    <legend class="login__form-header">Log in</legend>
                    <label class="login__form-label" for="email">email</label>
                    <input class="login__form-input" placeholder="Enter your email" type="text" id="email" name="user_email" />
                    <label class="login__form-label" for="password">password</label> 
                    <input class="login__form-input" placeholder="Password" type="password" id="password" name="user_password" />
                </fieldset>
                
                <button class="login__form-button" type="submit">Login</button>
                <div class="login__form-remember">
                    <div>
                        <input type="checkbox" name="remember" id="remember"> 
                        <label for="remember">Remember me?</label> 
                    </div>
                </div>

                <a href="#">Need help?</a>

                <div class="login__socials">
                    <p>Or log in using Google account:</p>
                    <a href="#"><img class="login__social" src="../assets/images/googleLogin.png" alt="google login"></a>
                </div>

            </form>
        </div>
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
    background-size: cover;

    padding: 45px 45px 0 45px;
    overflow: hidden;

    &__logo{
        max-width: 169px;
    }

    &__form{
        margin-top:1rem;
        padding: 3.75rem 4.25rem;
       
        background-color: rgba(0,0,0,0.7);
        border-radius: 5px;
    }

    &__form *+*{
        margin-bottom:1rem;
    }

    &__form-header{
        margin-bottom: 2rem;
        font-size: 2em;
        font-weight: bold;
    }
    
    &__form-label{
        display: none;
    }

    &__form-input{
        display: block;
        width: 100%;
        
        margin-bottom: 1rem;
        padding: 1rem 1.25rem;
        
        border:none;
        border-radius: 5px;
        background-color: rgba(51,51,51,1);

        font-weight: bold;
        color: rgba(140,140,140,1);
    }

    &__form-button{
        width: 100%;
        padding: 1rem 1.25rem;

        background-color: rgba(169,16,19,1);
        border: none;
        border-radius: 5px;

        font-weight: bold;
        color: rgba(255,255,255,1);
    }

    &__socials{
        margin-top:1rem;
        text-align: center;
        font-weight: lighter;
    }

    &__social{
        width:2.5rem;
        margin-top: 1rem;
        padding:5px;
        border: 3px rgb(53, 124, 238) solid;
        border-radius:10px;
        background-color: rgb(237, 236, 236);
    }

    &__social:hover{
        background-color: rgb(255, 255, 255);
        border-color: rgb(23, 89, 196) solid;
    }
}

@media screen and (max-width:31.25em) {

    body{
        font-size: 0.8em;
    }
    
    .login{
        padding-left:0;
        text-align: center;
    }
}

</style>
