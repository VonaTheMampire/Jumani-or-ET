<template>
  <div class="page">
    <div class="search">
      <h1><span class="jumanji">JUMANJI</span> <span class="or">or</span><span class="ET">E.T.</span></h1>
      <input v-model="film" placeholder="ET and Jumanji are basically the only 2 films" @keydown.enter="search(film)" />

       <div class="images">
        <img class="et" src="../assets/images/et.png" />
        <img class="jumanji" src="../assets/images/jumanji.png" />
      </div>
    </div>
  </div>
</template>   

<script>
export default {
  data () {
    return {
      film: ''
    }
  },
  methods: {
    search (film) {
      alert(film)
    }
  }
}
</script>

<style lang="scss" scoped>
// style for the OR in the title
.or {
  display: inline-block;
  font-size: 16px;
  padding: 12px;
}

.page {
  height: 100%; width: 100%;
  display: flex;
  justify-content: space-around;
  align-items: center;
  .search {
    max-width: 550px;
    margin-top: -70px;
    text-align: center;

    // title
    h1 {
      margin-bottom: 0;
      font-size: 80px;
    }

    // search box to enter film title in
    input {
      width: 100%; height: 50px;
      padding-left: 20px; padding-right: 20px;
      font-size: 16px; font-family: 'Indie Flower';
      border: 2px solid #222;
      box-sizing: border-box;
      transition: all .25s;
      text-align: center;

      &:focus {
        outline: none;
        border: 2px solid red;
      }
    }
  }
}

.images {
  img {
    opacity: 0.8;
    position: fixed;
    bottom: 0;
  }
  .et { left: 0; }
  .jumanji { right: 0; }
}
</style>
