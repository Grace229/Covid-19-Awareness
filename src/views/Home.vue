<template>
  <div id="appy">
    <Navbar />
    <Header />
      <Symptom />
     <h1  style="font-weight: bold;text-align: center;margin-top:40px;">Preventive Measures</h1>
      <b-container class="bv-example-row">
  <b-row>
    <b-col cols="5">
      <img :src="require('@/assets/header2.webp')">
  <img :src="require('@/assets/header1.jpg')">


      </b-col>
     <b-col cols="7">
     <Prevention v-for="item in items" :prevent='item' :key='item' />
  
 </b-col>
  </b-row>
</b-container>
     <b-container class="bv-example-row"> 

  <b-row>
    <b-col cols="3">
      <h1 style="font-weight: bold;">Nigerian Cases</h1>
     <b-list-group v-for="data in datas" :key='data.id'>
  <b-list-group-item class="d-flex justify-content-between align-items-center">
   {{ data.place }}
    <b-badge variant="primary" pill>{{ data.number }}</b-badge>
  </b-list-group-item>
</b-list-group>
    </b-col>
     <b-col cols="9">   
  
         <Update /> 
      </b-col>
  </b-row>
</b-container> 
  
  </div>
</template>
<script>

     import Prevention  from '../components/prevention.vue'
      import Header  from '../components/header.vue'
       import Update  from '../components/update.vue'
         import Navbar  from '../components/Navbar.vue'
           import Symptom  from '../components/symptom.vue'
          
  
  
export default {
  name: 'Home',
  components:{
Prevention,
Header,
Update,
Navbar,
Symptom

  },
  data(){
    return{
        datas:[
        {
           id: 1,
          place:'Lagos',
          number:'115'
        },
          {
           id: 2,
          place:'Abuja',
          number:'45'
          },
            {
           id: 3,
          place:'Osun',
          number:'20'
          },
            {
           id: 4,
          place:'Oyo',
          number:'9'
          },
            {
           id: 5,
          place:'Edo',
          number:'9'
          },
            {
           id: 6,
          place:'Bauchi',
          number:'6'
          },
            {
           id: 7,
          place:'Akwa Ibom',
          number:'5'
          },
            {
           id: 8,
          place:'Ogun',
          number:'4'
          },
            {
           id: 9,
          place:'Kaduna',
          number:'4'
          },
            {
           id: 10,
          place:'Enugu',
          number:'2'
          },
            {
           id: 11,
          place:'Ondo',
          number:'1'
          },
          {
           id: 12,
          place:'Rivers',
          number:'1'
          },
           {
           id: 13,
          place:'Benue',
          number:'1'
          },
          
      ],
    items:[
      {
        id: 1,
        image: require('@/assets/hand.png'),
        title: 'Wash your hands',
        note: 'Wash your hands often with soap and water for at least 20 seconds, or use an alcohol-based hand sanitizer that contains at least 60% alcohol.Clean and disinfect high-touch surfaces daily.'


      },
       {
        id: 2,
         image: require('@/assets/nose.jpg'),
        title: 'Avoid touching your eyes, nose and mouth.',
        note: 'Cover your mouth and nose with your elbow or a tissue when you cough or sneeze. Throw away the used tissue.'

      },
       {
        id: 3,
         image: require('@/assets/distancing.jpg'),
        title: 'Social Distancing',
        note: 'Avoid large events and mass gatherings,Keep distance between yourself and others if COVID-19 is spreading in your community, especially if you have a higher risk of serious illness.'

      },
       {
        id: 4,
         image: require('@/assets/ill_distancing.jpg'),
        title: 'Avoid close contact with sick persons',
        note: 'Avoid close contact (within about 6 feet, or 2 meters) with anyone who is sick or has symptoms.Avoid sharing dishes, glasses, bedding and other household items if you are sick.'

      },
       {
        id: 5,
       image: require('@/assets/cosme.jpg'),
        title: 'Wear face coverings in public places',
        note: 'The CDC recommends wearing cloth face coverings in public places, such as the stores and markets, where it is difficult to avoid close contact with others.It is especially suggested in areas with ongoing community spread.'

      },
        {
        id: 6,
       image: require('@/assets/home.png'),
        title: 'Stay at home',
        note: 'Stay home from work, school and public areas if you are sick, unless you are going to get medical care. Avoid taking public transportation if you are sick'

      },
 
    ],

  }
  },
};
</script>

<style lang="scss" scooped>
#appy {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  
  color: black;
  // background-color: blue;
  margin-bottom: 20px;


}


#nav {
 height: 800px;
 width: 100%;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
