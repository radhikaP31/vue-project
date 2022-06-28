<template>
  <div>
    Hello {{ greet }}, You are viewing {{ name }},Here is some example of
    Computed Properties
  </div>
  <p></p>
  <hr />
  <h2>Fullname - {{ firstname }} {{ lastname }}</h2>
  <h2>Computed Fullname - {{ fullName }}</h2>
  <button @click="changeFullname"> Change Fullname</button>

  <h2>Total - {{ items.reduce((total,curr) => ( total = total + curr.price), 0) }}</h2>
  <h2>Computed Total - {{ total }}</h2>
  <h2>Method Total - {{ getTotal() }}</h2>
  <button @click="items.push({ id: 4, title: 'remote', price: 500})">Add Item</button>

  <hr>
  <h2>With v-if: </h2>
  <template v-for="item in items" :key="item.id">
    <h6 v-if=" item.price > 100"> {{item.title}} {{item.price}}</h6>
  </template>

  <hr>
  <h2>With Computed v-if: </h2>
  <template v-for="item in expensiveItems" :key="item.id">
    <h6 v-if=" item.price > 100"> {{item.title}} {{item.price}}</h6>
  </template>
  <hr>
  
  <input type="text" v-model="country"> 


</template>

<script>
export default {
  name: 'App',
  data() {    
    return {
      'greet': 'Good Afternoon',
      name:' Vue App',
      firstname: 'Spiderman',
      lastname: 'Harry',
      items:[
        {
          id: 1,
          title: 'TV',
          price: 100,
        },
        {
          id: 2,
          title: 'Mobile',
          price: 200,
        },
        {
          id: 3,
          title: 'Laptop',
          price: 300,
        },
      ],
      country: '',
    };
  },
  methods: {
    getTotal() {
      console.log('Total Method')
      return this.items.reduce((total,curr) => ( total = total + curr.price), 0)
    },
    changeFullname() {
      this.fullName = 'Tony Stark'
    }
  },
  computed: {
    fullName: {
      get() {
        return `${this.firstname} ${this.lastname}`
      },
      set(value) {
        const names = value.split(' ')
        this.firstname = names[0]
        this.lastname = names[1]
      }
    },
    total() {
      console.log('Total computed properties')
      return this.items.reduce((total,curr) => ( total = total + curr.price), 0)
    },
    expensiveItems() {
      return this.items.filter(item => item.price > 100)
    },
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

hr {
  border: 2px solid #035891;
}
</style>
