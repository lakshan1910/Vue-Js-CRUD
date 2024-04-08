<template>
  <div>
    <h2>{{ name }}</h2>
    <h1 v-text="name2"></h1>
    <h2 v-bind:id="headingId">this is a heading</h2>
    <p v-bind:class="className">this is class binding</p>

    <h1>{{ computeFunc }}</h1>

    <h2>{{ value }}</h2>
    <button @click="value++">incre</button>
    <button @click="value--">decre</button>
  </div>
  
</template>

<script>
export default{

  data(){
    return{
      name : 'lakshan',
      name2 : 'hello',
      headingId : 'head',
      className : 'cls1',
      firstName : 'kmuara',
      secondName : 'dasa',
      value : 0
    }
  },
  computed: {
    computeFunc(){
      return `${this.firstName} ${this.secondName}`
    }
  },
  watch:{
    value(val){
      if(val > 5){
        alert('done')
      }
    }
  }
}
</script>



<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
