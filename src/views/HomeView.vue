<template>
  <div class="home">
    <h1>This is a home page</h1>
    <UserCard
        name="John Doe"
        email="john-doe@doe.fr"
        @user-welcome="displayWelcome"
    >
      <p>Adresse: 123 Rue de Vue</p>
      <template v-slot:extra>
        <p>Hobbies: Lecture, Randonnée</p>
      </template>
    </UserCard>
    <h4> My products</h4>
    <product
        url="https://picsum.photos/seed/picsum/200/300"
        title="Google"
        price="0"
        description="Le moteur de recherche">
    </product>

  </div>
</template>

<script>
// @ is an alias to /src
import UserCard from '@/components/UserCard.vue'
import Product from '@/components/Product.vue'

export default {
  name: 'HomeView',
  components: [{name : 'UserCard', component: UserCard}, {name : 'productCard', component: Product} ]
  ,
  methods: {
    displayWelcome(message) {
      alert(message);
    }
  }
}
</script>
