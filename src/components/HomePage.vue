<!-- eslint-disable vue/no-use-v-if-with-v-for -->
<template lang="">
  <div>
    <header class="header">
      <div class="container">
        <div class="row">
          <div class="col-lg-6">
            <div class="header__logo mt-3" style="float: left">
              <a href="/" aria-current="page" class="router-link-exact-active router-link-active"><img style="width: 200px; padding-top: 10px; vertical-align: middle; border-style: none" src="../assets/logo.png" alt="" /></a>
            </div>
          </div>
          <div class="col-lg-6">
            <nav class="header__menu" style="float: right">
              <ul type="none">
                <li class="mt-3">
                  <router-link to="/input" class="headNav">Add New Movie</router-link>
                </li>
              </ul>
            </nav>
          </div>
        </div>
      </div>
    </header>
    <section class="featured">
      <div class="container">
        <div class="row">
          <div class="col-lg-12">
            <div class="section-title"><h2>Movie List</h2></div>
            <div class="featured__controls">
              <ul>
                <li @click="filterCategoryMovie('')">All</li>
                <li @click="filterCategoryMovie('Actions')">Actions</li>
                <li @click="filterCategoryMovie('Science Fiction')">Science Fiction</li>
                <li @click="filterCategoryMovie('Horror')">Horror</li>
                <li @click="filterCategoryMovie('Thriller')">Thriller</li>
                <li @click="filterCategoryMovie('Comedy')">Comedy</li>
                <li @click="filterCategoryMovie('Romance')">Romance</li>
                <li @click="filterCategoryMovie('Adventure')">Adventure</li>
                <li @click="filterCategoryMovie('Fantasy')">Fantasy</li>
              </ul>
            </div>
          </div>
        </div>
        <div>
          <div class="row featured__filter" v-show="filterCategory === 'Actions'">
            <div 
              class="col-lg-3 col-md-4 col-sm-6"
              v-for="(item, index) in movieList" :key="index"
              v-if="item.category === 'Actions'"
            >
              <div class="featured__item">
                <img :src="item.image_url" class="featured__item__pic" />
                <div class="featured__item__text">
                  <router-link  :to="{ name: 'detailPage', params: { id: item.id }, query: { item } }" class=""><h5>{{ item.name }}</h5></router-link>
                </div>
              </div>
            </div>
          </div>
          <div class="row featured__filter" v-show="filterCategory === 'Science Fiction'">
            <div 
              class="col-lg-3 col-md-4 col-sm-6"
              v-for="(item, index) in movieList" :key="index"
              v-if="item.category === 'Science Fiction'"
            >
              <div class="featured__item">
                <img :src="item.image_url" class="featured__item__pic" />
                <div class="featured__item__text">
                  <router-link  :to="{ name: 'detailPage', params: { id: item.id }, query: { item } }" class=""><h5>{{ item.name }}</h5></router-link>
                </div>
              </div>
            </div>
          </div>
          <div class="row featured__filter" v-show="filterCategory === 'Horror'">
            <div 
              class="col-lg-3 col-md-4 col-sm-6"
              v-for="(item, index) in movieList" :key="index"
              v-if="item.category === 'Horror'"
            >
              <div class="featured__item">
                <img :src="item.image_url" class="featured__item__pic" />
                <div class="featured__item__text">
                  <router-link  :to="{ name: 'detailPage', params: { id: item.id }, query: { item } }" class=""><h5>{{ item.name }}</h5></router-link>
                </div>
              </div>
            </div>
          </div>
          <div class="row featured__filter" v-show="filterCategory === 'Thriller'">
            <div 
              class="col-lg-3 col-md-4 col-sm-6"
              v-for="(item, index) in movieList" :key="index"
              v-if="item.category === 'Thriller'"
            >
              <div class="featured__item">
                <img :src="item.image_url" class="featured__item__pic" />
                <div class="featured__item__text">
                  <router-link  :to="{ name: 'detailPage', params: { id: item.id }, query: { item } }" class=""><h5>{{ item.name }}</h5></router-link>
                </div>
              </div>
            </div>
          </div>
          <div class="row featured__filter" v-show="filterCategory === 'Comedy'">
            <div 
              class="col-lg-3 col-md-4 col-sm-6"
              v-for="(item, index) in movieList" :key="index"
              v-if="item.category === 'Comedy'"
            >
              <div class="featured__item">
                <img :src="item.image_url" class="featured__item__pic" />
                <div class="featured__item__text">
                  <router-link  :to="{ name: 'detailPage', params: { id: item.id }, query: { item } }" class=""><h5>{{ item.name }}</h5></router-link>
                </div>
              </div>
            </div>
          </div>
          <div class="row featured__filter" v-show="filterCategory === 'Romance'">
            <div 
              class="col-lg-3 col-md-4 col-sm-6"
              v-for="(item, index) in movieList" :key="index"
              v-if="item.category === 'Romance'"
            >
              <div class="featured__item">
                <img :src="item.image_url" class="featured__item__pic" />
                <div class="featured__item__text">
                  <router-link  :to="{ name: 'detailPage', params: { id: item.id }, query: { item } }" class=""><h5>{{ item.name }}</h5></router-link>
                </div>
              </div>
            </div>
          </div>
          <div class="row featured__filter" v-show="filterCategory === 'Adventure'">
            <div 
              class="col-lg-3 col-md-4 col-sm-6"
              v-for="(item, index) in movieList" :key="index"
              v-if="item.category === 'Adventure'"
            >
              <div class="featured__item">
                <img :src="item.image_url" class="featured__item__pic" />
                <div class="featured__item__text">
                  <router-link  :to="{ name: 'detailPage', params: { id: item.id }, query: { item } }" class=""><h5>{{ item.name }}</h5></router-link>
                </div>
              </div>
            </div>
          </div>
          <div class="row featured__filter" v-show="filterCategory === 'Fantasy'">
            <div 
              class="col-lg-3 col-md-4 col-sm-6"
              v-for="(item, index) in movieList" :key="index"
              v-if="item.category === 'Fantasy'"
            >
              <div class="featured__item">
                <img :src="item.image_url" class="featured__item__pic" />
                <div class="featured__item__text">
                  <router-link  :to="{ name: 'detailPage', params: { id: item.id }, query: { item } }" class=""><h5>{{ item.name }}</h5></router-link>
                </div>
              </div>
            </div>
          </div>
          <div class="row featured__filter" v-show="filterCategory === '' ">
            <div 
              class="col-lg-3 col-md-4 col-sm-6"
              v-for="(item, index) in movieList" :key="index"
            >
              <div class="featured__item">
                <img :src="item.image_url" class="featured__item__pic" />
                <div class="featured__item__text">
                  <router-link  :to="{ name: 'detailPage', params: { id: item.id }, query: { item } }" class=""><h5>{{ item.name }}</h5></router-link>
                </div>
              </div>
            </div>
          </div>
          <!-- <div class="row featured__filter">
            <div 
              class="col-lg-3 col-md-4 col-sm-6"
              v-for="(item, index) in movieList" :key="index"
            >
              <div class="featured__item">
                <img :src="item.image_url" class="featured__item__pic" />
                <div class="featured__item__text">
                  <router-link  :to="{ name: 'detailPage', params: { id: item.id }, query: { item } }" class=""><h5>{{ item.name }}</h5></router-link>
                </div>
              </div>
            </div>
          </div> -->
        </div>
      </div>
    </section>
  </div>
</template>
<script>
export default {
  name: "HomePage",
  data() {
    return {
      movieList: [],
      filterCategory: ""
    };
  },
  methods: {
    filterCategoryMovie(category){
      this.filterCategory = category
    }
  },
  created() {
    this.$http
      .get("https://vue-js-project-e25b9-default-rtdb.firebaseio.com/movielist.json")
      .then((response) => {
        return response.json();
      })
      .then((data) => {
        const resultArray = [];
        for (let key in data) {
          resultArray.push(data[key]);
        }
        this.movieList = resultArray;
      });
  },
};
</script>
<style>
.headNav {
  text-decoration: none;
  font-size: 14px;
  color: #252525;
  text-transform: uppercase;
  font-weight: 700;
  letter-spacing: 2px;
  transition: all, 0.3s;
  padding: 5px 0;
  display: block;
}
</style>
<style type="text/css">
body,
html {
  height: 100%;
}
body,
h2,
h5,
h6,
html {
  font-family: Cairo, sans-serif;
}
h2,
h5,
h6 {
  margin: 0;
  color: #111;
  font-weight: 400;
}
h2 {
  font-size: 36px;
}
h5 {
  font-size: 18px;
}
h6,
p {
  font-size: 16px;
}
p {
  font-family: Cairo, sans-serif;
  color: #6f6f6f;
  font-weight: 400;
  line-height: 26px;
  margin: 0 0 15px;
}
img {
  max-width: 100%;
}
button:focus,
input:focus,
select:focus,
textarea:focus {
  outline: none;
}
a:focus,
a:hover {
  text-decoration: none;
  outline: none;
  color: #fff;
}
ol,
ul {
  padding: 0;
  margin: 0;
}
</style>
<style type="text/css">
.featured {
  padding-top: 30px;
  padding-bottom: 40px;
}
.section-title {
  margin-bottom: 20px;
  text-align: center;
}
.section-title h2 {
  color: #1c1c1c;
  font-weight: 700;
  position: relative;
}
</style>
<style type="text/css">
.header__logo[data-v-394207fb] {
  padding: 15px 0;
}
.header__logo img[data-v-394207fb] {
  width: 200px;
  padding-top: 10px;
}
.header__logo a[data-v-394207fb] {
  display: inline-block;
}
.header__menu[data-v-394207fb] {
  padding: 24px 0;
}
.header__menu ul li[data-v-394207fb] {
  list-style: none;
  margin-right: 50px;
  position: relative;
  text-align: right;
}
.header__menu ul li:hover > a[data-v-394207fb] {
  color: #7fad39;
}
.header__menu ul li[data-v-394207fb]:last-child {
  margin-right: 0;
}
.header__menu ul li a[data-v-394207fb] {
  font-size: 14px;
  color: #252525;
  text-transform: uppercase;
  font-weight: 700;
  letter-spacing: 2px;
  transition: all, 0.3s;
  padding: 5px 0;
  display: block;
}
</style>
<style type="text/css">
.featured__controls {
  text-align: center;
  margin-bottom: 50px;
}
.featured__controls ul li {
  list-style: none;
  font-size: 18px;
  color: #1c1c1c;
  display: inline-block;
  margin-right: 25px;
  position: relative;
  cursor: pointer;
}
.featured__controls ul li.active:after {
  opacity: 1;
}
.featured__controls ul li:after {
  position: absolute;
  left: 0;
  bottom: -2px;
  width: 100%;
  height: 2px;
  background: #7fad39;
  content: "";
  opacity: 0;
}
.featured__controls ul li:last-child {
  margin-right: 0;
}
</style>
