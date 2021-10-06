<template>
    <div class="container">
        <div class="logo mx-auto cont">
             <h3><p>One account. Access all Services.</p></h3>
             <hr>
             <br>
             <form action="">
                 <label for="email"><p>Email/ID</p></label>
                 <input type="text" placeholder="example@gmail.com" id="email">
                 <br><br>
                 <label for="pass"><p>Password</p></label>
                 <input type="password" placeholder="password">
             </form>
        </div>
        <br>
        <div class="links mx-auto cont" >
            <div>
                <b-form-checkbox size="md"><p>Keep me Signed</p></b-form-checkbox>
            </div>
            <div>
                <b-link href="#foo">Forgot Password?</b-link>
            </div>
        </div>
         
        <div class="footerlinks mx-auto cont">
                 <b-button block variant="primary">SignIn</b-button>
            
        </div>
         
        <div class="cont mx-auto">
            <hr>
        </div>
         
        <div class="lk mx-auto cont">
                <p>Login with</p><b-link href="#foo"> Google</b-link>
        </div>
        <br>
        <div class=" lk mx-auto cont">
                <p>Don't have Account </p><b-link href="#foo">Request?</b-link>
        </div>
    </div>
</template>

<script>
export default {}
</script>

<style scoped lang="scss">
 
    p{
        font-weight: bold;
        font-family:'Roboto', sans-serif;
    }
 
    input
    {
        border-color: rgb(206, 212, 218);
        border-radius: 5px;
        border-width: 1px;
        height: 34px;
        outline: none;
    }
    input:focus
    {
        border-color: rgb(48, 138, 235);
        box-shadow: 0px 0px 5px rgb(95, 166, 243);
    }
    .container
    {
        display: flex;
        // background-color:burlywood ;
        justify-content: center;
        flex-direction: column;
       
 
    }
    .cont
        {
            background-color: whitesmoke;
            width:40%;
            

        }
    .logo{
        // background-color: cornsilk;
        width: 40%;
        text-align: center;
        margin-top: 5%;
        padding-top: 2%;
   
    }
    hr
    {
        width: 20%;
    }
    input{
        margin-left: 2%;
    }
    .links{

        display: flex;
        width: 40%;
        text-align: center;
        // background-color: cyan;
        justify-content: center;
    }
    .links > div {
        margin: 10px;
    }
    
    .footerlinks{
        text-align: center;
        width:40% ;
    }
    p{display: inline;}
    b-button{
    background-color: rgb(240, 75, 48);
}
.lk{text-align: center;}
@import url('https://fonts.googleapis.com/css2?family=Roboto&display=swap');
</style>