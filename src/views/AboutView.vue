<template>
  <div class="about">
    <h1>This is an about page</h1>
    <h1>{{name}}</h1>
    <h1 v-for="(item, index) in language" :key="index">{{item}}</h1>
    <h1 v-for="(item, index) in students" :key="index">Name:{{item.name}}, Email:{{item.email}}, Mobile: {{item.mobile}}</h1>
  </div>
</template>

<script>
export default {
  name:'AboutView',
  data()
  {
    return{
      name:'Rakesh',
      language:['html', 'css', 'PHP', 'Javascript'],
      students:[
        {'name':'Rakesh', 'email':'rakesh@gmail.com', 'mobile':'0174121412'},
        {'name':'Riya', 'email':'riya@gmail.com', 'mobile':'0187121412'},
        {'name':'Ritesh', 'email':'ritesh@gmail.com', 'mobile':'0161412412'},
      ]
    }
  }
}

</script>

<style scoped>

</style>
