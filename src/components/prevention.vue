<template>
<div id="app">
 
  <div>

  <b-card class="card-body"> 
    
    <b-card-text>
      <h4>{{ prevent.title }}</h4>
    </b-card-text>

   <div>
  <b-button id="btn" variant="danger" @click="$bvModal.show(prevent.id)">
     See More
     </b-button>
  
 

  <b-modal :id="prevent.id" 
  :title="prevent.title">
       <b-card
    :title="prevent.title"
    :img-src="prevent.image"
    img-alt="Image"
    img-top
    tag="article"
    style="max-width: 20rem;"
    class="mb-2"
  >
   </b-card>
  
    <p class="my-4">{{prevent.note}}</p>
  </b-modal>
</div>

  </b-card>
</div>
</div>
  
</template>
<script>
export default {
    name:"prevention",
    props: ['prevent']
    
}
</script>
<style lang="scss" scoped>
#btn{
  float: right;
  margin-bottom: 20px;
 
}
.card-body{
  height: 130px !important;

}

</style>