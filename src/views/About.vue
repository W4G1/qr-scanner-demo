<template>
  <div class="about">
    <h1>This is an about page</h1>
    <button v-on:click="openScanner">Open scanner</button>
  </div>
</template>

<script>
import { BarcodeScanner } from "@ionic-native/barcode-scanner";

export default {
  methods: {
    openScanner() {
      BarcodeScanner.scan({
        // preferFrontCamera: true, // iOS and Android
        showFlipCameraButton: false, // iOS and Android
        showTorchButton: false,
        prompt: "",
        formats: "QR_CODE",
        resultDisplayDuration: 0
      })
        .then(({ text, cancelled }) => alert(text))
        .catch(err => alert(err));
    }
  }
};
</script>
