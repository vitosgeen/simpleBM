<template>
  <div class="pads">
    <table>
      <thead></thead>
      <tbody>
        <tr v-for="n in 5" :key="n">
          <td v-for="x in 5" :key="x">
            <button v-on:click="buttonPlayPad" :id="'pad-'+n+'-'+x" class="button-pad">Pad {{ n }} {{ x }}</button>
          </td>
        </tr>
      </tbody>
      <tfoot></tfoot>
    </table>
  </div>
</template>

<script>
export default {
  name: "Pads",
  methods: {
    buttonPlayPad: function(e){
      console.log(e.currentTarget);
    },
  },
};
</script>
<style>
  .button-pad{
    width: 50px;
    height: 50px;
    color: transparent;
    border:1px solid #000;
    border-radius: 3px;
    box-shadow:-1px -1px 2px rgba(255,255,255,0.2) inset,0 -5px 2px 3px rgba(0,0,0,0.6) inset,0 2px 4px rgba(0,0,0,0.5);
    background:linear-gradient(45deg,#222 0%,#555 100%)
  }
  .button-pad:active {
    box-shadow:-1px -1px 2px rgba(255,255,255,0.2) inset,0 -2px 2px 3px rgba(0,0,0,0.6) inset,0 1px 2px rgba(0,0,0,0.5);
    background:linear-gradient(to right,#444 0%,#222 100%)
  }
</style>
