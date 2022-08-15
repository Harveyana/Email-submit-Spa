<template>
  <q-page class="flex flex-center" style="background: rgba(222, 233, 236, 0.8)">
    <q-card class="main-container flex flex-center" style="">
      <q-card
        class="container column no-wrap flex flex-center q-px-md q-pb-md"
        style=""
      >
        <q-card
          class="text-box self-start bg-transparent"
          style="width: 75%; height: fit-content"
        >
          <h3 class="heading" style="">Enter email address</h3>
        </q-card>
        <q-card
          class="input-box row no-wrap self-start justify-between bg-transparent"
          style=""
        >
          <q-input
            borderless
            v-model="mailInput"
            color="#27141a"
            class="q-pl-md input"
            style=""
          >
          </q-input>

          <q-btn push class="btn" label="Submit" style="" @click="redir()" />
        </q-card>
      </q-card>
    </q-card>
  </q-page>
</template>

<script setup>
import { useQuasar } from "quasar";
import { ref } from "vue";
const mailInput = ref("");
const $q = useQuasar();
const redir = () => {
  $q.notify("Redirecting to mailbox");
  window.location.href =
    "mailto:harveyana3@gmail.com?subject=Email Submission&body=" +
    `${mailInput.value}`;
};
</script>
<style scoped lang="sass">
.heading
  font-size: 170%
  line-height: 1px
  color: #e6b41d
  font-family: 'Catellosdemo'
  body.screen--xs &
    font-size: 160%
    line-height: normal
.text-box
  width: 75%
  height: fit-content
  body.screen--xs &
    font-size: 80%
    width:100%
.main-container
  width: 70vw
  height: 50vh
  border-radius: 15px
  background: rgba(54, 39, 47, 0.91)
  body.screen--xs &
    width: 90vw
.container
  width: 80%
  background: rgba(54, 39, 47, 0.91)
  border-radius: 15px
  body.screen--xs &
    width: 90%
.input-box
  width: 90%
  body.screen--xs &
    flex-direction: column
    width: 100%

.input
  width: 75%
  background: whitesmoke
  color: #27141a
  font-size: 20px
  border-radius: 15px
  body.screen--xs &
    font-size: 16px
    width: 100%
    height: 45px

.btn
  width: 19%
  background: #e6b41d
  border-radius: 15px
  border: 1px solid #27141a
  color: #27141a
  font-family: 'Manrope-Medium'
  font-size: medium
  body.screen--xs &
    margin-top: 10%
    width: 50%
</style>
