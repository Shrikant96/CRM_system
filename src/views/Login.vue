<template>
  <b-container class="bv-example-row ">
    <br /><br /><br>
    <b-card tag="article" style="max-width: 22rem" class="mx-auto">
      <b-card-text>
        <h2>LogIn</h2>
        <br>
        <b-form>
            <b-form-group
            class="ml-0"
            description=" "
            label-for="email"
            label="Email/ID"
            >
                <b-form-input 
                id="email" 
                size="sm" 
                placeholder="example@gmail.com"
                type="email"
                 >
                </b-form-input>
            </b-form-group>

            <b-form-group
            label=Password
            label-for="password">

                <b-form-input
                id=password
                size="sm"
                placeholder="password"
                type="password">
                </b-form-input>

            </b-form-group>
        </b-form>
      </b-card-text>

       <b-form-group>
            <b-button class="" style="background-color: rgb(240, 75, 48); border:none">LogIn</b-button>
            <b-button class="m-1">SignUp</b-button>
       </b-form-group>
    </b-card>
  </b-container>
</template>

<script>
export default
{
    name:'Login'
};
</script>

<style scoped lang="scss">
 
h2{
    text-align: center;
    text-decoration: underline;
}
b-button{
    background-color: rgb(240, 75, 48);
}
</style>