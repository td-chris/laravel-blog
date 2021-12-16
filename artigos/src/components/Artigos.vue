<template>
  <div class="hello">
    <div class="card">
      <div class="post" v-for="artigo in artigos" v-bind:key="artigo">
        <h3>{{ artigo.titulo }}</h3>
        <p>{{ artigo.conteudo }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Artigos',
  data() {
    return {
      artigos: [ ]
    }
  },

  methods: {
    fetchArtigos(){
      fetch('http://localhost/artigos/API/public/api/artigos')
      .then(res => res.json())
      .then(res => {
        this.artigos = res.data
      })
      .catch( err => console.log(err))
    }
  },

  created() {
    this.fetchArtigos()
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hello {
  color: #333;
  padding: 20px;
  max-width: 1200px;
  margin: auto;
}

.card {
  background-color: #fff;
  color: #333;
}

.post {
  border: 1px solid silver;
  padding: 10px;
  margin-top: 10px;
  text-align: left;
}
</style>
