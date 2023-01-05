<script setup>
import { computed } from "vue";

const me = {
  firstName: "Romain",
  lastName: "Garcia Rodriguez",
  age: 26,
};
const defaultValue = "Default Value";
const imgGoogle = "https://vuejs.org/images/logo.png";
const rand = () => {
  return Math.random();
};

const fullName = computed(() => {
  return me.firstName + " " + me.lastName;
});

const ageBy7 = computed(() => {
  return me.age * 7;
});
</script>

<template>
  <!-- 1) Afficher votre nom complet (prénom + nom dans 2 variables différentes) en utilsant une computed  -->
  <p>{{ fullName }}</p>
  <!-- 2) Afficher votre age multiplié par 7 -->
  <p>{{ ageBy7 }}</p>
  <!-- 3) Afficher un nombre aléatoire entre 0 et 1 -->
  <p>{{ rand() }}</p>
  <!-- 4) Prendre une image sur Google et l'afficher de manière dynamique avec Vue -->
  <div>
    <img :src="imgGoogle" style="width: 100px; height: 100px" />
  </div>
  <!-- 5) Ajouter une valeur par défaut (stocké dans 1 variable) dans un input via Vue en utilisant les attribute bindings -->
  <div>
    <input type="text" :value="defaultValue" />
  </div>

  <div></div>
</template>

<style></style>
