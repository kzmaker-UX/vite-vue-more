<template>
<h2>First Name: {{ firstName }}</h2>
<h2>Last Name: {{ lastName }}</h2>
<h2>Full Name: {{ fullName }}</h2>
<h2>
  Total: {{ items.reduce ((total, curr) => (total = total + curr.price ), 0)}}
</h2>
</template>

<script>
  export default {
    data () {
      return{
        firstName: 'kay',
        lastName: 'Z', 
        items: [
          {id:1, 
          title: 'TV', 
          price: 100
          },
          {id:2, 
          title: 'phone', 
          price: 200
          },
          {id:1, 
          title: 'laptop', 
          price: 300
          }
        ]
      }
    }, 
    computed: {
      fullName(){
        return `${this.firstName}${this.lastName}`
      }
    }
  }
</script>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
