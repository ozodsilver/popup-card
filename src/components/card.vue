<template>
  <div id="card-one">
    <div class="card-1 d-flex">
      <div
        class="card  m-auto text-center bg-light justify-content-center align-items-center p-5 m-3"
        v-if="show"
        style="width:500px"
      >
        <h1>New Book Subscription</h1>
        <p>
          Lorem, ipsum dolor sit amet consectetur adipisicing elit. Doloribus
          placeat aspernatur perferendis tempore excepturi corrupti provident
          laboriosam aut, libero omnis veniam,
        </p>

        <button
          class="btn btn-primary d-block m-auto w-50"
          @click="showSecondCard"
        >
          click Here
        </button>
      </div>
    </div>

    <br />
    <div class="w-100" style="position:absolute; left:0; top:10%">
      <transition name="bounce">
        <div
          class="card-1 d-flex card  m-auto p-4 text-center"
          id="card-two"
          v-if="!show"
          style="width:400px;"
        >
          <i
            class="fa fa-close text-danger"
            style="position:absolute; right:10px; top:3px; cursor:pointer;"
            @click="showfirstCard"
          ></i>
          <img
            src="https://f.vividscreen.info/soft/5759d199d44d8efbc4baf625282421a7/Program-Code-2880x1920.jpg"
            class="img img-fluid"
            alt=""
          />
          <div class="card-title">
            <h3>New books</h3>
            <p>
              Lorem, ipsum dolor sit amet consectetur adipisicing elit. Alias
              odit expedita laboriosam quo
            </p>
            <div class="wrapper w-100 m-auto">
              <div class="btn bg-light border w-50" @click="showfirstCard">
                cancel
              </div>

              <div class="btn btn-success w-50">
                go
              </div>
            </div>
          </div>
        </div>
      </transition>
    </div>
  </div>
</template>

<script>
export default {
  el: "#card-one",
  data() {
    return {
      show: true,
    };
  },

  methods: {
    showSecondCard() {
      this.show = !this.show;
    },
    showfirstCard() {
      this.show = !this.show;
    },
  },
};
</script>

<style scoped>
.bounce-enter-active {
  animation: bounce-in 0.5s;
}
.bounce-leave-active {
  animation: bounce-in 0.5s reverse;
}
@keyframes bounce-in {
  0% {
    transform: scale(0);
  }
  50% {
    transform: scale(1.5) rotate(10deg);
  }
  100% {
    transform: scale(1) rotate(0deg);
  }
}
</style>
