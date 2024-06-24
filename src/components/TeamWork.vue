<template>
    <div class="container">
        <div class="row">
            <h2 class="display-2">Team Members</h2>
        </div>

        <div class="row gap-2 justify-content-center" v-if="details.length">

            <Card v-for="detail in details" :key="detail.id" :class="{
            male: detail.gender.toLowerCase() == 'male',
            female: detail.gender.toLowerCase() == 'female'
        }">
                <template #cardHeader>
                    <img :src="detail.profile" :alt="detail.firstName" class="img-fluid" loading="lazy">
                </template>

                <template #cardBody>
                    <p class="lead">{{ detail.firstName }} {{ detail.lastName }}</p>
                    <p> {{ detail.age }} Years Old </p>
                </template>

            </Card>  
        </div>

        <div class="d-flex justify-content-center" v-else>
            <div class="spinner-border" role="status">
            </div>
        </div>

    </div>
</template>

<script>
import Card from '@/components/Card.vue'
export default {
  name: 'TeamWorkComp',

  props: [ 'member1', 'member2'],

  components: {
    Card
  },

  data() {
    return {
        details: [
            {
                id:1,
                firstName: "Jamin",
                lastName: "Langeveldt",
                gender: "Male",
                age:20,
                profile: "https://joshua-langeveldt.github.io/images/images/People/Jamin.jpg"
            },
            {
                id:2,
                firstName: "Leah",
                lastName: "Basson",
                gender: "Female",
                age:19,
                profile: "https://joshua-langeveldt.github.io/images/images/People/leah.png"
            }
        ]
    }
  }

}
</script>

<style scoped>
.male {
    border: 2px solid red;
    box-shadow: .3vw .2vw .5vw black;
}

.female {
    border: 2px solid gold;
    box-shadow: .4vw .4vw .5vw black;
}

img{
    width:30%;
    margin: 10px;
    border-radius: 10px;
    border: 2px solid black;
}

p {
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    font-weight: 200;
    font-style: normal;
}

</style>