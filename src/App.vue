<template>
  <main>
    <div class="row">
      <div class="col-3">
        <div class="row">
          <Navbar />
        </div>
      </div>
      <div class="col-9">
        <div class="row">
          <div class="col-12 d-flex justify-content-between bg-fb">
            <h1 class="m-3 text-white">Hello World</h1>
            <form
              class="
                form-inline
                d-flex
                justify-content-center
                md-form
                form-sm
                m-3
              "
            >
              <input
                class="form-control form-control-sm mr-3 w-75"
                type="text"
                placeholder="Search"
                aria-label="Search"
              />
              <i class="mdi mdi-magnify" aria-hidden="true"></i>
            </form>
          </div>
          <router-view />
        </div>
      </div>
    </div>
  </main>
  <footer>
    <div class="bg-dark text-light text-center p-4">
      Made with 💖 by CodeWorks
    </div>
  </footer>
</template>

<script>
import { computed } from "vue";
import { AppState } from "./AppState";
export default {
  name: "App",
  setup() {
    return {
      appState: computed(() => AppState),
    };
  },
};
</script>
<style lang="scss">
@import "./assets/scss/main.scss";
.bg-fb {
  background: linear-gradient(90deg, #39c4c6 20.9%, rgba(255, 255, 255, 0) 100%),
    #7edacf;
  box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.25);
}
</style>
