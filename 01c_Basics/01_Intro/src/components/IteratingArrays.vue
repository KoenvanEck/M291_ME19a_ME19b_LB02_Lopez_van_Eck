<template>
  <div>
    <h1>Top 3 songs of your favourite artists</h1>
    <h2>We asked you what your favourite artists where and what their 3 best songs were. These are the results:</h2>
    <ul>
      <li id="li-title" v-for="item in interests" :key="item">
        {{ item.title }}
        <ol>
          <li id="li-content" v-for="fav in item.favorite" :key="fav"> {{ fav }}</li>
        </ol>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      interests: [
        {title:"Michael Jackson", favorite:["Thriller", "Billie Jean", "P.Y.T. Pretty Young Thing"]},
        {title:"Billie Eilish", favorite:["Everything I Wanted", "Bad Guy", "Ocean Eyes"]},
        {title:"OBN", favorite:["Roses", "Bad Girl", "Drunk"]}
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
#li-title {
  font-family: 'Gadugi', Helvetica, Arial, sans-serif;
  color: #494949;
  margin-top: 1.5rem;
  font-weight: bold;
}

#li-content {
  font-family: 'Gadugi', Helvetica, Arial, sans-serif;
  color: #494949;
  font-weight: normal;
}

h1 {
  font-family: 'Gadugi', Helvetica, Arial, sans-serif;
  color: #00b4d8;
  margin-top: 60px;
}

h2 {
  font-family: 'Gadugi', Helvetica, Arial, sans-serif;
  color: #494949;
}
</style>
