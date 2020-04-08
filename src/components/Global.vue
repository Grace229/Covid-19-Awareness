<template>
    <div id="app">
    

        <b-card-group deck>
  <b-card no-body header>
 <b-container class="bv-example-row">
  <b-row>
    <!-- <div>
  <b-list-group horizontal>
    <b-col class="col left"><b-list-group-item variant="secondary">COUNTRY</b-list-group-item></b-col>
    <b-col class="col left1"><b-list-group-item variant="primary">NEW</b-list-group-item></b-col>
    <b-col class="col left2"><b-list-group-item variant="warning">CONFIRMED</b-list-group-item></b-col>
    <b-col class="col left3"><b-list-group-item variant="success">RECOVERED</b-list-group-item></b-col>
<b-col class="col left4"><b-list-group-item variant="danger">DEATH</b-list-group-item></b-col>
  </b-list-group>
</div> -->


  </b-row>
</b-container>
<div class="contain">
  <span id="content"><h1>GLOBAL CASES OF CORONA VIRUS</h1></span>
  <span>Country</span>
  <span>new</span>
  <span>recovered</span>
  <span>confirmed</span>
   <span>death</span>
  
</div>

<b-list-group v-for="data in datas" :key='data.id'>
  <div class="contain">
  <span>{{ data.place }}</span>
  <span> <b-badge variant="primary" pill>{{ data.new }}</b-badge></span>
  <span> <b-badge variant="warning" pill>{{ data.confirmed }}</b-badge></span>
  <span><b-badge variant="success" pill>{{ data.recovered }}</b-badge></span>
  <span><b-badge variant="danger"  pill>{{ data.death }}</b-badge></span>
 
  
</div>

 
  
 
 
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
          place:'USA',
          new:'29609',
          recovered:'22539',
          confirmed:'399979',
          death:'12912'
        },
        {
          id: 2,
          place:'Spain',
          new:'5267',
          recovered:'48021',
          confirmed:'146690',
          death:'14555'
        },
           {
          id: 3,
          place:'Italy',
          new:'3039',
          recovered:'24392',
          confirmed:'135586',
          death:'17127'
        },
           {
          id: 4,
          place:'France',
          new:'11102',
          recovered:'19523',
          confirmed:'110070',
          death:'10343'
        },
            {
          id: 5,
          place:'Germany',
          new:'4289',
          recovered:'36081',
          confirmed:'109329',
          death:'2096'
        },
            {
          id: 6,
          place:'China',
          new:'56',
          recovered:'77628',
          confirmed:'83188',
          death:'3342'
        },
            {
          id: 7,
          place:'Iran',
          new:'2089',
          recovered:'27039',
          confirmed:'64586',
          death:'3993'
        },
            {
          id: 8,
          place:'United Kingdom',
          new:'3670',
          recovered:'332',
          confirmed:'55957',
          death:'6171'
        },
            {
          id: 9,
          place:'Turkey',
          new:'3892',
          recovered:'1582',
          confirmed:'34109',
          death:'725'
        },
            {
          id: 10,
          place:'Belgium',
          new:'1380',
          recovered:'4681',
          confirmed:'23403',
          death:'2240'
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

.contain{
  grid-template-columns: repeat(5,1fr);
  grid-auto-rows: minmax(100px, auto);
  display: grid;
   text-align: center;
  font-weight: bolder;
}
#content{
  grid-column: 1 / 6;
}
span{
border: 1px solid #f8f9fa;
}

/* 
h1{
 
} */
@media only screen and (max-width: 500px) and (min-width: 320px){
  #app{
  display: inline-flex;
  }
}
#app{
  margin-top: 50px;

}

</style>