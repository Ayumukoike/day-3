<template>
  <div class="container">
    <div class="container">
      <div class="nav-scroller py-1 mb-2">
        <nav class="nav d-flex justify-content-between">
          <a class="p-2 text-muted" href="#">LA.LIGA</a>
          <a class="p-2 text-muted" href="#">serieA</a>
          <a class="p-2 text-muted" href="#">J1leage</a>
          <a class="p-2 text-muted" href="#">J2</a>
          <a class="p-2 text-muted" href="#">BRAZIL </a>
          <a class="p-2 text-muted" href="#">Liverpool</a>
          <a class="p-2 text-muted" href="#">K-leage</a>
          <a class="p-2 text-muted" href="#">Bundesliga</a>
          <a class="p-2 text-muted" href="#">CL</a>
          <a class="p-2 text-muted" href="#">EL</a>
          <a class="p-2 text-muted" href="#">COPA</a>
          <a class="p-2 text-muted" href="#">FA</a>
        </nav>
      </div>

      <div class="jumbotron p-4 p-md-5 text-white rounded bg-dark">
        <div class="col-md-6 px-0">
          <h1 class="display-4 font-italic">
            nuxt football blog
          </h1>
          <p class="lead my-3"></p>
          <p class="lead mb-0">
            <a href="#" class="text-white font-weight-bold">
              Continue reading...</a
            >
          </p>
        </div>
      </div>

      <div class="row mb-2">
        <div class="col-md-6">
          <div
            class="row no-gutters border rounded overflow-hidden flex-md-row mb-4 shadow-sm h-md-250 position-relative"
          >
            <div class="col p-4 d-flex flex-column position-static">
              <strong class="d-inline-block mb-2 text-primary"
                >Liverpool</strong
              >
              <h3 class="mb-0">transfar market</h3>
              <div class="mb-1 text-muted">Nov 12</div>
              <p class="card-text mb-auto">
                2020-2021
              </p>
              <a href="#" class="stretched-link">Continue reading</a>
            </div>
            <div class="col-auto d-none d-lg-block">
              <svg
                class="bd-placeholder-img"
                width="200"
                height="250"
                xmlns="http://www.w3.org/2000/svg"
                preserveAspectRatio="xMidYMid slice"
                focusable="false"
                role="img"
                aria-label="Placeholder: sample"
              >
                <title>Placeholder</title>
                <rect width="100%" height="100%" fill="#55595c"></rect>
                <text x="50%" y="50%" fill="#eceeef" dy=".3em">foorball</text>
              </svg>
            </div>
          </div>
        </div>
        <div class="col-md-6">
          <div
            class="row no-gutters border rounded overflow-hidden flex-md-row mb-4 shadow-sm h-md-250 position-relative"
          >
            <div class="col p-4 d-flex flex-column position-static">
              <strong class="d-inline-block mb-2 text-success">Design</strong>
              <h3 class="mb-0">Post title</h3>
              <div class="mb-1 text-muted">Nov 11</div>
              <p class="mb-auto">
                This is a wider card with supporting text below as a natural
                lead-in to additional content.
              </p>
              <a href="#" class="stretched-link">Continue reading</a>
            </div>
            <div class="col-auto d-none d-lg-block">
              <svg
                class="bd-placeholder-img"
                width="200"
                height="250"
                xmlns="http://www.w3.org/2000/svg"
                preserveAspectRatio="xMidYMid slice"
                focusable="false"
                role="img"
                aria-label="Placeholder: Thumbnail"
              >
                <title>Placeholder</title>
                <rect width="100%" height="100%" fill="#55595c"></rect>
                <text x="50%" y="50%" fill="#eceeef" dy=".3em">sample</text>
              </svg>
            </div>
          </div>
        </div>
      </div>
    </div>
    <table class="table">
      ​
      <thead>
        ​
        <tr>
          ​
          <th scope="col">バロンドール</th>
          ​
          <th scope="col"></th>
          ​
          <th scope="col">NAME</th>
          ​
          <th scope="col">EMAIL</th>
          ​
        </tr>
        ​
      </thead>
      ​
      <tbody>
        ​
        <tr v-for="(item, i) in items" :key="i">
          ​
          <th scope="row">{{ item.id }}</th>
          ​
          <td>{{ item.naem }}</td>
          ​
          <td>{{ item.username }}</td>
          ​
          <td>{{ item.email }}</td>
          ​
        </tr>
        ​
      </tbody>
      ​
    </table>
  </div>
</template>

<script>
import axios from "axios";
export default {
  async asyncData() {
    const url1 = "https://jsonplaceholder.typicode.com/users";
    const params = {
      id: "11",
      name: "messi",
      username: "CR7",
      email: "waaaaaa@gmail.com"
    };
    const res = await axios.post(url1, params);
    const { data } = await axios.get(url1);
    return {
      items: data,
      item: res.data
    };
  }
};
</script>
