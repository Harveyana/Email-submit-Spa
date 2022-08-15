<template>
  <q-page class="flex flex-center">
    <q-card
      class="main-container flex flex-center"
      style="
        width: 70vw;
        height: 50vh;
        border-radius: 15px;
        background: rgba(54, 39, 47, 0.91);
      "
    >
      <q-card
        class="container column no-wrap flex flex-center q-px-md q-pb-md"
        style="
          width: 80%;
          background: rgba(54, 39, 47, 0.91);
          border-radius: 15px;
        "
      >
        <q-card
          class="text-box self-start bg-transparent"
          style="width: 75%; height: fit-content"
        >
          <h3
            class=""
            style="
              font-size: 35px;
              line-height: 1px;
              color: #e6b41d;
              font-family: 'Catellosdemo';
            "
          >
            Enter email address
          </h3>
        </q-card>
        <q-card
          class="input-box row no-wrap self-start justify-between bg-transparent"
          style="width: 90%"
        >
          <q-input
            borderless
            v-model="mailInput"
            color="#27141a"
            class="q-pl-md"
            style="
              width: 75%;
              background: whitesmoke;
              color: #27141a;
              font-size: 20px;
              border-radius: 15px;
            "
          >
          </q-input>
          <!-- <a
            href="mailto:tejiritabor@gmail.com?subject=Your Subject&body="
            style="width: 19%"
          > -->
          <q-btn
            push
            label="Submit"
            style="
              width: 19%;
              background: #e6b41d;
              border-radius: 15px;
              border: 1px solid #27141a;
              color: #27141a;
              font-family: 'Manrope-Medium';
              font-size: medium;
            "
            @click="redir()"
          />
          <!-- </a> -->
        </q-card>
      </q-card>
    </q-card>
  </q-page>
</template>

<script setup>
import { ref } from "vue";
const mailInput = ref("");
const redir = () => {
  window.location.href =
    "mailto:tejiritabor@gmail.com?subject=Your Subject&body=" +
    `${mailInput.value}`;
};
</script>
