<template>
    <div class="row">
        <div class="col-sm-4 pt-2" v-bind:key="post.id" v-for="post in posts">
            <div class="card" style="width: 18rem;">
                <img src="https://placehold.jp/200x150.png" class="card-img-top" alt="img200x150">
                <div class="card-body">
                    <h5 class="card-title">{{ post.title }}</h5>
                    <p class="card-text">{{ post.body }}</p>
                    <a href="#" class="btn btn-primary">Go somewhere</a>
                </div>
            </div>
        </div>
        <!-- <div class="col-sm-4">
            <div class="card" style="width: 18rem;">
                <img src="https://placehold.jp/200x150.png" class="card-img-top" alt="img200x150">
                <div class="card-body">
                    <h5 class="card-title">Card title</h5>
                    <p class="card-text">Some quick example text to build on the card title and make up the bulk of the
                        card's
                        content.</p>
                    <a href="#" class="btn btn-primary">Go somewhere</a>
                </div>
            </div>
        </div>
        <div class="col-sm-4">
            <div class="card" style="width: 18rem;">
                <img src="https://placehold.jp/200x150.png" class="card-img-top" alt="img200x150">
                <div class="card-body">
                    <h5 class="card-title">Card title</h5>
                    <p class="card-text">Some quick example text to build on the card title and make up the bulk of the
                        card's
                        content.</p>
                    <a href="#" class="btn btn-primary">Go somewhere</a>
                </div>
            </div>
        </div> -->
    </div>
</template>

<script>
export default {
    name: "cards-list",

    props: {
        posts: {
            type: Array,
            required: true
        }

    }


}
</script>

<style></style>