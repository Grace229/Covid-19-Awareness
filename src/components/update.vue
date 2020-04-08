<template>
    <div id="app">
    <h1>CASES OF CORONA VIRUS IN AFRICA</h1>

        <b-card-group deck>
  <b-card no-body header>
 <b-container class="bv-example-row">
  <b-row>
    <div>
  <b-list-group horizontal>
    <b-col class="col left"><b-list-group-item variant="secondary">COUNTRY</b-list-group-item></b-col>
    <b-col class="col left1"><b-list-group-item variant="primary">NEW</b-list-group-item></b-col>
    <b-col class="col left2"><b-list-group-item variant="warning">CONFIRMED</b-list-group-item></b-col>
    <b-col class="col left3"><b-list-group-item variant="success">RECOVERED</b-list-group-item></b-col>
<b-col class="col left4"><b-list-group-item variant="danger">DEATH</b-list-group-item></b-col>
  </b-list-group>
</div>


  </b-row>
</b-container>
<b-list-group v-for="data in datas" :key='data.id'>
  <b-list-group-item class="d-flex justify-content-between align-items-center">
  
    <b-container class="bv-example-row">
  <b-row>
    <b-col>{{ data.place }}</b-col>
    <b-col class="col item1" > <b-badge variant="primary" pill>{{ data.new }}</b-badge></b-col>
    <b-col  class="col item2"><b-badge variant="warning" pill>{{ data.confirmed }}</b-badge></b-col>
    <b-col  class="col item3"><b-badge variant="success" pill>{{ data.recovered }}</b-badge></b-col>
    <b-col  class="col item4"> <b-badge variant="danger"  pill>{{ data.death }}</b-badge></b-col>
  </b-row>
</b-container>   
  </b-list-group-item>
</b-list-group> 
</b-card>
</b-card-group>
    </div>
</template>
<script>
export default {
    name:"update",
    data(){
      return{
         datas:[
        {
          id: 1,
          place:'South Africa',
          new:'80',
          recovered:'95',
          confirmed:'1585',
          death:'9'
        },
        {
          id: 2,
          place:'Algeria',
          new:'80',
          recovered:'90',
          confirmed:'1251',
          death:'130'
        },
           {
          id: 3,
          place:'Egypt',
          new:'85',
          recovered:'241',
          confirmed:'1070',
          death:'71'
        },
           {
          id: 4,
          place:'Morocco',
          new:'128',
          recovered:'70',
          confirmed:'961',
          death:'69'
        },
            {
          id: 5,
          place:'Cameroon',
          new:'46',
          recovered:'17',
          confirmed:'555',
          death:'9'
        },
            {
          id: 6,
          place:'Tunisia',
          new:'58',
          recovered:'5',
          confirmed:'553',
          death:'19'
        },
            {
          id: 7,
          place:'Burkina Faso',
          new:'16',
          recovered:'66',
          confirmed:'318',
          death:'16'
        },
            {
          id: 8,
          place:'Cote d"ivoire',
          new:'51',
          recovered:'25',
          confirmed:'245',
          death:'1'
        },
            {
          id: 9,
          place:'Mauritius',
          new:'10',
          recovered:'7',
          confirmed:'227',
          death:'7'
        },
            {
          id: 10,
          place:'Nigeria',
          new:'16',
          recovered:'44',
          confirmed:'254',
          death:'5'
        },
        
      ],
   
      }
    }
}
</script>
<style scoped>
#list{
    margin-right: 20px;
}
.col.item1{
/* margin-left: 30px; */
}

.col.left2{
  margin-left: 10px;
}
.col.left3{
  margin-left: 10px;
}
col.item4{
  /* margin-left: 100px; */
}
col.item3{
  /* margin-left: 90px; */
} 
.col.left4{
  margin-left: 10px;
}
/* .col.left1{
  margin-left: 30px;
} */
h1{
  text-align: center;
  font-weight: bolder;
}

@media only screen and (max-width: 500px) and (min-width: 320px){
  #app{
  display: inline-flex;
  }
}
#app{
  margin-top: 50px;
  height: 100px;
}

</style>