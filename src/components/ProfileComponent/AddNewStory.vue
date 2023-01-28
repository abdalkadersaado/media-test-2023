<template>
  <button type="button" data-bs-toggle="modal" data-bs-target="#staticBackdropStory">
    <img src="@/assets/images/add_icon.png" alt="" />
    {{ $t("Add Story") }}
  </button>

  <div
    class="modal fade"
    id="staticBackdropStory"
    data-bs-backdrop="static"
    data-bs-keyboard="false"
    tabindex="-1"
    aria-labelledby="staticBackdropLabel"
    aria-hidden="true"
  >
    <div class="modal-dialog modal-dialog-centered">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title" id="staticBackdropLabel">
            {{ $t("Create Story") }}
          </h5>
          <div class="close-dir">
            <button
              type="button"
              class="btn-close"
              data-bs-dismiss="modal"
              aria-label="Close"
            ></button>
          </div>
        </div>
        <div class="modal-body">
          <div class="row justify-content-center">
            <div class="col-3 col-sm-3">
              <div class="card">
                <div
                  class="card-body justify-content-center"
                  data-bs-toggle="modal"
                  data-bs-target="#AddStory"
                >
                  <div class="bo">
                    <font-awesome-icon icon="fa-solid fa-text-width" />
                  </div>
                  <p class="text-center">{{ $t("TEXT") }}</p>
                </div>
              </div>
            </div>
            <div class="col-3 col-sm-3">
              <div class="card">
                <div
                  class="card-body justify-content-center"
                  data-bs-toggle="modal"
                  data-bs-target="#AddStory2"
                >
                  <div class="bo">
                    <font-awesome-icon icon="fa-solid fa-file-image" />
                  </div>
                  <p class="text-center">{{ $t("IMAGE") }}</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <AddStory />
  <AddStoryTow />
</template>
<script>
import AddStory from "@/components/HomeComponent/Story/AddSroryComponent.vue";
import AddStoryTow from "@/components/HomeComponent/Story/AddSroryTowComponent.vue";
import { mapGetters } from "vuex";
export default {
  components: {
    AddStory,
    AddStoryTow,
  },
  computed: {
    ...mapGetters({
      USER: "auth/auth_user_info",
    }),
  },
};
</script>
<style lang="scss" scoped>
.links-urls {
  position: absolute;
  bottom: 0;
  right: 0;
  padding: 10px;
  .link {
    padding: 10px 20px;
    display: block;
    background-color: #eee;
    margin-bottom: 10px;
    text-decoration: none;
    color: #777;
  }
}
.post-col ul li {
  list-style: none;
  font-size: 15px;
  margin: 15px 0;
  align-items: center;
}
.post-col ul li img {
  width: 26px;
  margin-right: 10px;
}
/*  */
/* profile page */
.profile-container {
  padding: 20px 15%;
  background: #ddd;
}

.cover-img {
  width: 100%;
  height: 25rem;
  border-radius: 6px;
  // margin-bottom: 14px;
}
.profile-details {
  background: #fff;
  padding: 20px;
  border-radius: 4px;
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
}

.pd-row {
  display: flex;
  align-items: flex-start;
}

.pd-image {
  width: 70px;
  height: 60px;
  margin-right: 20px;
  border-radius: 6px;
  margin-bottom: 10px;
}

.pd-row div h3 {
  font-size: 25px;
  font-weight: 600;
  margin: 5px;
}

.pd-row div p {
  font-size: 13px;
  margin: 2px;
}

.pd-row div img {
  width: 25px;
  border-radius: 50%;
  margin-top: 12px;
}
.pd-right button {
  background: #1876f2;
  border: 0;
  outline: 0;
  padding: 4px 8px;
  display: inline-flex;
  align-items: center;
  color: #fff;
  border-radius: 15px;
  margin-left: 10px;
  cursor: pointer;
  margin: 2px;
}

.pd-right button img {
  height: 15px;
  margin-right: 10px;
}

.pd-right button:first-child {
  background: #e4e6eb;
  color: #000;
}

.pd-right {
  text-align: right;
}

//create Story
p {
  font-weight: bold;
  font-size: 12px;
  color: white;
  margin-top: 13px;
}

.story {
  height: 170px;
  align-items: center;
  display: flex;

  .story_s {
    position: relative;
    margin-left: 10px;
    height: 170px;
    min-width: 100px;
    max-width: 100px;
    .story_body {
      height: 100%;
      position: relative;
      border-radius: 10px;
      cursor: pointer;
      .user_img {
        border-radius: 100%;
        border: 3px solid white;
        position: absolute;
        width: 40px !important;
        height: 40px !important;
        top: 0.8rem;
        left: 0.5rem;
      }
    }
  }
}
.header_story {
  position: relative;
  height: 65%;
  border-top-right-radius: 10px;
  border-top-left-radius: 10px;
  img {
    border-top-right-radius: 10px;
    border-top-left-radius: 10px;
    position: relative;
    width: 100%;
    height: 100%;
  }
}
.bc1 {
  border: 2px solid #8080804a;
  .story_center {
    position: absolute;
    top: 62%;
    left: 47%;
    transform: translate(-60%, -60%);
    z-index: 1;
  }
  .text_3 {
    position: absolute;
    bottom: 0;
    color: white;
    left: 0.7rem;
  }
  .svg {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
  }
  .story_footer {
    position: relative;
    height: 35%;
    background: #f3f3f3a6;
  }
}

.modal {
  background-color: rgba(255, 255, 255, 0.527) !important;
}
.modal-content {
  border-radius: 20px;
  box-shadow: rgba(50, 50, 93, 0.25) 0px 50px 100px -20px,
    rgba(0, 0, 0, 0.3) 0px 30px 60px -30px, rgba(10, 37, 64, 0.35) 0px -2px 6px 0px inset !important;
}
.modal-body {
  .card {
    background: #00a79d;
    height: 100%;
    .card-body {
      .bo {
        position: relative;
        border-radius: 100%;
        background: white;
        margin-top: 50%;
        padding: 30%;
        display: flex;
        justify-content: center;

        svg {
          font-size: x-large !important;
        }
      }
    }
  }
}
.close-dir:lang(ar) {
  direction: ltr;
}
</style>
