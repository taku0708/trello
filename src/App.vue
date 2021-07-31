<template>
  <div class="app">
    <button v-on:click="postTweet">ツイート</button>
  </div>
</template>

<script>
import firebase from "firebase";

export default {
  methods: {
    postTweet() {
      firebase.firestore().collection("tweets").add({
        text: "こんにちは、ツイートの本文です。",
      });
    },
  },
};
</script>
