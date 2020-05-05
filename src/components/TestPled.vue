<template>
  <div>
    <div v-for="(pled, index) in testPled" :key="index" style="border: 1px solid red">
      <div style="display: flex">
        <div>
          <img :src="pled.image" style="height: 300px;">
        </div>
        <div>
          <div v-for="(field, index) in pled.field" :key="index" style="border: 1px solid green">
            {{field._name}}: {{field.__text}}
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import { mapGetters } from 'vuex';

  export default {

    computed: {
    ...mapGetters([
        'testPled',
      ]),
    },
  };
</script>

<style>

</style>
