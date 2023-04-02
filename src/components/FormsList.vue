<template>
  <div class="row align-items-start">
    <div class="col-12 col-sm-12 p-4">
      <form @submit.prevent>
        <h4>Создание поста</h4>
        <div class="row mb-3">
          <label for="inputEmail3" class="col-sm-2 col-form-label">Название</label>
          <div class="col-sm-10">
            <input type="text" v-model="post.title" class="form-control" id="inputEmail3"
              placeholder="Введите название">
          </div>
        </div>
        <div class="row mb-3">
          <label for="inputPassword3" class="col-sm-2 col-form-label">Описание</label>
          <div class="col-sm-10">
            <input type="text" v-model="post.body" class="form-control" id="inputPassword3"
              placeholder="Введите описание">
          </div>
        </div>
        <button type="submit" class="btn btn-primary" @click="createPost">Создать</button>
      </form>

    </div>
  </div>
</template>

<script>
export default {
  name: "forms-list",

  data() {
    return {
      post: {
        title: "",
        body: ""
      }

    }
  },
  methods: {
    createPost() {
      this.post.id = Date.now(),
        this.$emit('create', this.post)
      this.post = {
        title: "",
        body: ""
      }

    },

    // полная запись на JS
        // < input type="text" id="myInput" >
        // const inputField = document.getElementById('myInput')
        // inputField.addEventListener('input', function (event) {
        // console.log('Input changed:', event.target.value) })

        // inputTitle(event) {
        //     this.title = event.target.value
        // },

        // //короткая запись в html
        // //@input="body = $event.target.value"

        // inputBody(event) {
        //   this.body = event.target.value
        // },
  }
}
</script>

<style></style>