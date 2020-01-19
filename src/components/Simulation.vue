<template>
  <div>
    <div class="simulator-title">
      <h1>
        <svg
          height="40px"
          width="40px"
          class="animate"
          viewBox="0 0 512 512"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="m256 426.667969c-94.105469 0-170.667969-76.5625-170.667969-170.667969s76.5625-170.667969 170.667969-170.667969 170.667969 76.5625 170.667969 170.667969-76.5625 170.667969-170.667969 170.667969zm0-324.269531c-84.691406 0-153.601562 68.910156-153.601562 153.601562s68.910156 153.601562 153.601562 153.601562 153.601562-68.910156 153.601562-153.601562-68.910156-153.601562-153.601562-153.601562zm0 0"
          />
          <path
            d="m256 512c-4.710938 0-8.535156-3.824219-8.535156-8.535156v-51.199219c0-4.710937 3.824218-8.53125 8.535156-8.53125s8.535156 3.820313 8.535156 8.53125v51.199219c0 4.710937-3.824218 8.535156-8.535156 8.535156zm0 0"
          />
          <path
            d="m256 68.265625c-4.710938 0-8.535156-3.820313-8.535156-8.53125v-51.199219c0-4.710937 3.824218-8.535156 8.535156-8.535156s8.535156 3.824219 8.535156 8.535156v51.199219c0 4.710937-3.824218 8.53125-8.535156 8.53125zm0 0"
          />
          <path
            d="m59.734375 264.535156h-51.199219c-4.710937 0-8.535156-3.824218-8.535156-8.535156s3.824219-8.535156 8.535156-8.535156h51.199219c4.710937 0 8.53125 3.824218 8.53125 8.535156s-3.820313 8.535156-8.53125 8.535156zm0 0"
          />
          <path
            d="m503.464844 264.535156h-51.199219c-4.710937 0-8.53125-3.824218-8.53125-8.535156s3.820313-8.535156 8.53125-8.535156h51.199219c4.710937 0 8.535156 3.824218 8.535156 8.535156s-3.824219 8.535156-8.535156 8.535156zm0 0"
          />
          <path
            d="m213.332031 384c-1.3125 0-2.636719-.296875-3.863281-.921875-3.492188-1.773437-5.324219-5.707031-4.445312-9.53125l23.183593-100.480469h-40.472656c-3.347656 0-6.375-1.953125-7.765625-4.984375-1.390625-3.035156-.878906-6.605469 1.3125-9.128906l110.933594-128c2.570312-2.96875 6.828125-3.796875 10.316406-2.023437 3.5 1.773437 5.335938 5.710937 4.445312 9.53125l-23.183593 100.472656h40.472656c3.347656 0 6.375 1.953125 7.765625 4.984375 1.390625 3.035156.878906 6.605469-1.3125 9.128906l-110.933594 128c-1.664062 1.929687-4.035156 2.953125-6.453125 2.953125zm-6.910156-128h32.511719c2.601562 0 5.058594 1.1875 6.671875 3.21875 1.621093 2.027344 2.21875 4.691406 1.640625 7.234375l-17.878906 77.484375 76.210937-87.9375h-32.511719c-2.601562 0-5.058594-1.1875-6.679687-3.21875-1.613281-2.027344-2.21875-4.691406-1.640625-7.234375l17.886718-77.484375zm0 0"
          />
          <path
            d="m430.984375 439.519531c-2.183594 0-4.367187-.839843-6.03125-2.5l-36.199219-36.199219c-3.335937-3.335937-3.335937-8.730468 0-12.066406 3.335938-3.335937 8.730469-3.335937 12.066406 0l36.199219 36.199219c3.335938 3.335937 3.335938 8.726563 0 12.066406-1.664062 1.660157-3.851562 2.5-6.035156 2.5zm0 0"
          />
          <path
            d="m117.222656 125.746094c-2.183594 0-4.371094-.835938-6.035156-2.5l-36.207031-36.199219c-3.335938-3.335937-3.335938-8.726563 0-12.066406 3.328125-3.335938 8.730469-3.335938 12.066406 0l36.207031 36.199219c3.339844 3.335937 3.339844 8.730468 0 12.066406-1.664062 1.671875-3.855468 2.5-6.03125 2.5zm0 0"
          />
          <path
            d="m81.015625 439.519531c-2.183594 0-4.371094-.839843-6.035156-2.5-3.335938-3.339843-3.335938-8.730469 0-12.066406l36.207031-36.199219c3.339844-3.335937 8.738281-3.335937 12.066406 0 3.339844 3.335938 3.339844 8.730469 0 12.066406l-36.207031 36.199219c-1.664063 1.660157-3.847656 2.5-6.03125 2.5zm0 0"
          />
          <path
            d="m394.785156 125.746094c-2.183594 0-4.367187-.835938-6.03125-2.5-3.335937-3.335938-3.335937-8.730469 0-12.066406l36.199219-36.199219c3.335937-3.335938 8.726563-3.335938 12.066406 0 3.335938 3.339843 3.335938 8.730469 0 12.066406l-36.199219 36.199219c-1.671874 1.671875-3.851562 2.5-6.035156 2.5zm0 0"
          />
        </svg>
        Power Box
      </h1>
    </div>
    <div class="contact">
      <br />
      <br />
      <a href="https://megatronicspower.com">Our Store</a>
      /
      <a href="mailto:hello@megatronicspower.com">Contact Us</a>
      /
      <a href="mailto:developer@megatronicspower.com">Feedback</a>
    </div>
    <div style="clear:both;"></div>
    <div class="simulator">
      <div class="inner-simulator">
        <div style="padding-bottom: 10px;padding-top: 10px;">
          <h3 style="text-align:center">Simulator Box</h3>
        </div>
        <div class="simulator-box" v-if="appliances.length">
          <div v-for="(appliance, index) of appliances" :key="index">
            <Element :url="appliance.image" />
          </div>
        </div>
      </div>
      <div style="clear:both;width: 20%;margin: 0px auto;text-align:center;">
        <div style="width: 5px;height: 100px;background: orange;float:left">&nbsp;</div>
        <div style="width: 5px;height: 100px;background: orange;float:right">&nbsp;</div>
        <div class="simulator-battery">
          <img src="../assets/inverter.svg" width="100" style="position: relative;bottom: 20px;" />
        </div>
      </div>
      <div class="button-placeholder">
        <button class="refresh" @click="refresh">
          <img src="../assets/refresh.svg" width="13" style="position: relative;top: 3px;" />&nbsp;Refresh
        </button>
        <button
          class="save"
          @click="save"
          :disabled="appliances.length < 1 || isLoading"
        >
          <span v-if="isLoading">please wait...</span>
          <span v-if="!isLoading">
            <img src="../assets/upload.svg" width="13" style="position: relative;top: 3px;" />&nbsp;I want this specification
          </span>
        </button>
      </div>
    </div>
  </div>
</template>

<script>
import Swal from "sweetalert2";
import { EventBus } from "@/event-bus.js";
import Element from "@/components/Element.vue";
import axios from "axios";

export default {
  components: {
    Element
  },
  data() {
    return {
      appliances: [],
      isLoading: false
    };
  },
  mounted() {
    EventBus.$on("ADD", value => {
      this.appliances.push(value);
    });
  },
  methods: {
    async refresh() {
      await Swal.fire({
        title: "Are you sure?",
        text: "You won't be able to revert this!",
        icon: "warning",
        showCancelButton: true,
        confirmButtonColor: "#3085d6",
        cancelButtonColor: "#d33",
        confirmButtonText: "Confirm"
      }).then(result => {
        if (result.value) {
          window.location.reload();
          localStorage.removeItem("_SIMULATION_DATA");
        }
      });
    },
    async save() {
      const { value: formValues } = await Swal.fire({
        title: "Contact Us for the specification",
        html:
          'Name: <input id="swal-input1" class="swal2-input">' +
          'Phone Number: <input id="swal-input2" class="swal2-input">',
        focusConfirm: false,
        preConfirm: () => {
          return [
            document.getElementById("swal-input1").value,
            document.getElementById("swal-input2").value
          ];
        }
      });
      if (formValues) {
        if (formValues[0] == "" || !formValues[0].match(/^[a-zA-Z\s]+$/)) {
          Swal.fire({
            title: "Notification",
            text: "Valid name is required",
            icon: "error"
          });
          return;
        } else if (
          formValues[1] == "" ||
          !formValues[1].match(/^[0-9]+$/) ||
          formValues[1].length < 11 ||
          formValues[1].length > 11
        ) {
          Swal.fire({
            title: "Notification",
            text: "Phone Number is required and must be 11 digit",
            icon: "error"
          });
          return;
        }
        this.isLoading = true;
        this.storeUser(formValues);
      }
    },
    async storeUser(details) {
      const [name, email] = details;
      const activity = localStorage.getItem("_SIMULATION_DATA");
      if (activity == undefined) {
        Swal.fire("Error Occured !");
        return;
      }
      const { data, watt } = JSON.parse(activity);
      const headers = {
        headers: {
          Authorization: "Bearer 4297f44b13955235245b2497399d7a93"
        }
      };
      const that = this;
      const payload = {
        name: name,
        watt: watt,
        recommendation: data,
        email: email
      };
      await axios
        .post(
          "https://api.megatronicspower.com?action=add_user",
          payload,
          headers
        )
        .then(result => {
          if (result.data.status == "success") {
            Swal.fire({
              title: "Notification",
              text:
                "Information sent successfully, our technical department will contact you soon. Thank you",
              icon: "success"
            });
          }
          that.isLoading = false;
          setTimeout(() => {
            window.location.reload();
          }, 10000);
        })
        .catch(err => {
          Swal.fire("Error occured");
        });
    }
  }
};
</script>
<style lang="scss">
.simulator {
  min-height: 420px;
  background: #ffffff;
  border: 5px solid gold;
  .inner-simulator {
    min-height: 200px;
    border-bottom: 3px solid orange;
  }
}

.contact {
  float: right;
  a {
    color: #999;
    text-decoration: none;
    &:hover {
      text-decoration: underline;
    }
  }
}

.simulator-box {
  display: flex;
  flex-wrap: wrap;
  width: 100%;
}

.pole-holder {
  padding-right: 20px;
  padding-left: 20px;
  padding-bottom: 45px;
  border-bottom: 3px solid orange;
  height: 40px;
  margin-bottom: 25px;

  :nth-child(2) {
    height: inherit;
    position: relative;
    bottom: 7px;
  }
}
.pole-wire {
  background: orange !important;
  height: 100%;
  width: 10%;
  margin: auto;
}

.simulator-battery {
  clear: both;
  border-top: 3px solid orange;
  margin-bottom: 5px;
}

.button-placeholder {
  display: flex;
  align-items: center;
  justify-content: center;
  margin: auto;
  text-align: center;
}
button {
  padding: 10px 30px;
  border: transparent;
  margin-bottom: 15px;
  margin-left: 10px;
  margin-right: 10px;
  font-weight: bold;
  font-size: 14px;
  border-radius: 5px;
  cursor: pointer;
  transition: 0.3s all;
  outline: none;
  &:hover {
    opacity: 0.7;
  }
  &.refresh {
    background: #cce5ff;
  }
  &.save {
    background-color: #d4edda;
  }
}

.simulator-title {
  float: left;
}

.simulator-title h1 {
  color: #999;
}

.animate {
  color: #999;
  animation: colorchangesvg 20s infinite;
  -webkit-animation: colorchangesvg 20s infinite;
}

@keyframes colorchangesvg {
  0% {
    fill: #3085d6;
  }

  10% {
    fill: #8e44ad;
  }

  20% {
    fill: #1abc9c;
  }

  30% {
    fill: #d35400;
  }

  40% {
    fill: #3085d6;
  }

  50% {
    fill: #34495e;
  }

  60% {
    fill: #3085d6;
  }

  70% {
    fill: #2980b9;
  }
  80% {
    fill: #f1c40f;
  }

  90% {
    fill: #2980b9;
  }

  100% {
    fill: pink;
  }
}
@-webkit-keyframes colorchangesvg {
  0% {
    fill: #3085d6;
  }

  10% {
    fill: #8e44ad;
  }

  20% {
    fill: #1abc9c;
  }

  30% {
    fill: #d35400;
  }

  40% {
    fill: #3085d6;
  }

  50% {
    fill: #34495e;
  }

  60% {
    fill: #3085d6;
  }

  70% {
    fill: #2980b9;
  }
  80% {
    fill: #f1c40f;
  }

  90% {
    fill: #2980b9;
  }

  100% {
    fill: pink;
  }
}
</style>
