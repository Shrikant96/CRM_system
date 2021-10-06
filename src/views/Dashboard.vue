<template>
  <div>
    <b-navbar toggleable="lg" type="dark" variant="dark" >
      <b-navbar-brand to="#">Blaze Engine</b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <!-- <b-nav-item to="#">Link</b-nav-item> -->
          <b-nav-item  @click="openComp='Sales_Dash'">Dashboard</b-nav-item>
          
          <b-nav-item-dropdown text="Sales" right>
            <b-dropdown-item @click="openComp='Enqurie'">Enquries</b-dropdown-item>
            <b-dropdown-item to="#">Clients</b-dropdown-item>
            <b-dropdown-item to="#">Attendance</b-dropdown-item>
          </b-nav-item-dropdown>
          
          <b-nav-item-dropdown text="Finance" right>
            <b-dropdown-item to="#">Invoices</b-dropdown-item>
            <b-dropdown-item to="#">Settings</b-dropdown-item>
          </b-nav-item-dropdown>
          <b-nav-item to="#">Employee</b-nav-item>
          <b-nav-item to="#">Subscripition</b-nav-item>
          <!-- <b-nav-item to="#" disabled>Disabled</b-nav-item> -->
        </b-navbar-nav>
        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <b-nav-form>
            <b-form-input
              size="sm"
              class="mr-sm-2"
              placeholder="Search"
            ></b-form-input>
            <b-button size="sm" class="my-2 my-sm-0" type="submit"
              >Search</b-button
            >
          </b-nav-form>
          <b-nav-item-dropdown text="Lang" right>
            <b-dropdown-item to="#">EN</b-dropdown-item>
            <b-dropdown-item to="#">ES</b-dropdown-item>
            <b-dropdown-item to="#">RU</b-dropdown-item>
            <b-dropdown-item to="#">FA</b-dropdown-item>
          </b-nav-item-dropdown>

          <b-nav-item-dropdown right>
            <!-- Using 'button-content' slot -->
            <template #button-content>
              <em>User</em>
            </template>
            <b-dropdown-item to="#">Profile</b-dropdown-item>
            <b-dropdown-item to="#">Sign Out</b-dropdown-item>
          </b-nav-item-dropdown>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
    
    <component :is="openComp" />
      
     

  </div>
</template>
<script>
import Sales_Dash from "@/components/Sales_Dash.vue";
import Enqurie from "@/views/Enqurie.vue";

export default{
  name:"Dashboard",
  components:{
    Sales_Dash,
    Enqurie,
  },
  data(){
    return{
      openComp:'Sales_Dash',

    };
  }
}
</script>

<style scoped >


</style>