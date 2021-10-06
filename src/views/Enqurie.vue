<template>
  <div id="main">
    <div class="header">
    <div class="heading">
      <h5>Sales</h5>
    </div>
      <div class="menu">
        <div>  <b-button>Add Member</b-button></div>
        <div>  <b-button>Save</b-button></div>
        <div>  <b-button>Update</b-button></div>
      </div>
    </div>
    <div id="body">
      <!-- <hr> -->
      <!-- <div class="col">
        <div class="inputgroup">
          <div class="label">First Name</div>
          <div class="inputf"><input type="text" ></div>
        </div>
      </div>

      <div class="col">
          <div class="inputgroup">
          <div class="label"></div>
          <div class="inputf"></div>
      </div>
      </div> -->
      <br>
      <b-table small :fields="fields" :items="items" responsive="sm">
        <template #cell(index)="data">
          {{data.index +1}}
        </template>
        <template #cell(name)="data">
          {{data.value.first}}, {{data.value.last}}
        </template>

      </b-table>
    </div>
    <div id="footer">

    </div>

  </div>
</template>

<script>
export default {
  name: "Enqurie",
  data() 
  {
    return{
      fields:[
        {key:'index', label:'Index'},
        {key:'name', label:'Full Name'},
        {key:'email', label:'Email ID'},
        {key:'mobile', label:'Mobile'},
        {key:'sex', label:'Sex'},
        {key:'gr', label:'Group Reg'},
        {key:'dob', label:'D.O.B'},
        {key:'age', label:'Age'},
        {key:'addr', label:'Address'},
        {key:'city', label:'City'},
        {key:'lead_source', label:'Lead Source'},
        {key:'status', label:'Status'},

 

        // {key:'gr', label:'Group Registration'},
 
      ],
      items: [
        { name:{first:'John', last:'Doe'}, email:'shrikant96@gmail.com', mobile: 7972168543, sex:'Male', gr:'Yes',dob:"06/06/1997", age:25, addr:"narsingh colony akot", city:"Akot",lead_source:"Google", status:'Active'},
        { name:{first:'jane', last:'Doe'}, email:'shrikant96@gmail.com', mobile: 8572168543, sex:'Female', gr:'Yes',dob:"06/06/1997", age:25, addr:"narsingh colony akot", city:"Akot",lead_source:"Google", status:'Active'},
        { name:{first:'Rubin', last:'Kincade'}, email:'shrikant96@gmail.com', mobile: 8972168543, sex:'Female', gr:'Yes',dob:"06/06/1997", age:25, addr:"narsingh colony akot", city:"Akot",lead_source:"Google", status:'Active'},
        { name:{first:'Shirley', last:'Partridge'}, email:'shrikant96@gmail.com', mobile: 7972168543, sex:'Female', gr:'Yes',dob:"06/06/1997", age:25, addr:"narsingh colony akot", city:"Akot",lead_source:"Google", status:'Active'},
        { name:{first:'John', last:'Aoe'}, email:'shrikant96@gmail.com', mobile: 7972168543, sex:'Male' ,gr:'Yes',dob:"06/06/1997", age:25, addr:"narsingh colony akot", city:"Akot",lead_source:"Google", status:'Active'},
      ]
    }
  }
};
</script>

<style scoped >
.header {
  /* background-color: rgb(52, 58, 64); */
  display: flex;
  margin-top:2%;
   
}
 
.header > div {
  width: 50%;
   
}
.menu {
  margin-left: 50%;
  /* background-color: rgb(52, 58, 64); */
  display: flex;
}
.menu  > div 
{
  margin-left: 2.5%;
  padding-top: 1%;
  padding-bottom: 1%;
}
/* .inputgroup{display: flex;} */
</style>