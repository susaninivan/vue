
<template>
    <!-- NAV #1 и HEADER -->
    <div class="top">
        <div class="container-fluid">
            <div class="row">
                <!-- NAV #1 -->
                <nav class="navbar navbar-light bg-light col-md-6 col-xl-12 order-md-1 order-xl-0">
                    <div class="container-fluid">
                        <a class="navbar-brand">Navbar</a>
                        <form class="d-flex">
                            <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
                            <button class="btn btn-outline-success" type="submit">Search</button>
                        </form>
                    </div>
                </nav>
                <!-- HEADER -->
                <header class="col-md-6 col-xl-12 order-md-0 order-xl-1">
                    <h1>Каталог постов</h1>
                </header>
            </div>
        </div>
    </div>
    <!-- ОСНОВНОЙ КОНТЕНТ -->
    <main>
        <div class="container">
            <div class="row">
                <!-- NAV #2 -->
            <!-- <nav class="col-xl-2">
                    <p>NAV #2</p>
                            </nav> -->
                <!-- ARTICLE (основной блок) -->
                <article class="col-md-8 col-xl-10">
                    <div class="col-md-12 col-sm-12 p-4">
                        <div class="form-center">
                            <forms-list @create="createPost" />
                        </div>
                    </div>

                    <div class="col-md-12 col-sm-12 p-4">
                        <cards-list v-bind:posts="posts" />
                    </div>
                    <div class="col-md-12 col-sm-12 p-4">
                        One of three columns
                    </div>
                </article>
                <!-- ASIDE -->
                <aside class="col col__aside">
                    Боковая область
                </aside>




                <div class="container">
                    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Laborum quibusdam natus, nulla delectus
                        velit ipsa
                        voluptate. Dicta neque tenetur sunt deleniti officiis? Atque, ullam quae temporibus rem vitae ipsa
                        tenetur?
                        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Laborum quibusdam natus, nulla delectus
                        velit ipsa
                        voluptate. Dicta neque tenetur sunt deleniti officiis? Atque, ullam quae temporibus rem vitae ipsa
                        tenetur?
                        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Laborum quibusdam natus, nulla delectus
                        velit ipsa
                        voluptate. Dicta neque tenetur sunt deleniti officiis? Atque, ullam quae temporibus rem vitae ipsa
                        tenetur?
                    </p>
                </div>

                <div class="container">
                    <table class="table">
                        <thead>
                            <tr>
                                <th scope="col">#</th>
                                <th scope="col">First</th>
                                <th scope="col">Last</th>
                                <th scope="col">Handle</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <th scope="row">1</th>
                                <td>Mark</td>
                                <td>Otto</td>
                                <td>@mdo</td>
                            </tr>
                            <tr>
                                <th scope="row">2</th>
                                <td>Jacob</td>
                                <td>Thornton</td>
                                <td>@fat</td>
                            </tr>
                            <tr>
                                <th scope="row">3</th>
                                <td colspan="2">Larry the Bird</td>
                                <td>@twitter</td>
                            </tr>
                        </tbody>
                    </table>
                </div>

            </div>
        </div>
    </main>
    <!-- FOOTER -->
    <footer class="container">
        <div class="row">
            <div class="col col__footer">
                Секция футера 1
            </div>
        </div>
        <div class="row">
            <div class="col col__footer">
                Секция футера 2
            </div>
        </div>
        <div class="row">
            <div class="col col__footer">
                Секция футера 3
            </div>
        </div>
        <div class="row">
            <div class="col col__footer">
                Секция футера 4
            </div>
        </div>
    </footer>
</template>

<script>

import CardsList from '@/components/CardsList.vue'
import FormsList from "@/components/FormsList.vue"

export default {
    name: "app",
    components: {
        CardsList, FormsList
    },
    data() {
        return {

            posts: [
                { id: 0, title: "One post", body: "Lorem ipsum dolor, sit amet consectetur adipisicing elit1", img: "200x150.png" },
                { id: 1, title: "Tow post", body: "Lorem ipsum dolor, sit amet consectetur adipisicing elit2", img: "200x250.png" },
                { id: 2, title: "Three post", body: "Lorem ipsum dolor, sit amet consectetur adipisicing elit3", img: "200x350.png" },
                { id: 3, title: "Three post", body: "Lorem ipsum dolor, sit amet consectetur adipisicing elit4", img: "200x350.png" },
            ],


        }
    },
    methods: {

        createPost(post) {
            // console.log(post)
            this.posts.push(post);
        }
    }
}
</script>

<style>
 /* ... */
 .col__other-article {
    -ms-flex: 1 0 0;
    flex: 1 0 0;
    min-width: 300px;
  }

  .col__footer {
    -ms-flex: 1 0 0;
    flex: 1 0 0;
    min-width: 200px;
  }



.form-center {
    max-width: 500px;
    max-height: 500px;
    margin: 0 auto;
    border: 1px solid lightgrey;
}</style>