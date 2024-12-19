<template>
    <header class="header">
        <span>{{ headerText }}</span>
        <div class="button-container">
            <BaseButton
                v-for="(button, index) in buttons"
                :key="index"
                :color="button.color"
                :size="button.size"
                :label="button.label"
                :href="button.href"
                :target="button.target"
                :icon="button.icon"
                :onClick="button.onClick"
            />
        </div>
    </header>
</template>

<script>
import BaseButton from './Button.vue';

export default {
  name: 'Header',
  components: {
    BaseButton, 
  },
  props: {
    headerText: {
      type: String,
      required: true, // This will be passed dynamically
    },
    buttons: {
      type: Array,
    },
  },
};
</script>


<style lang="scss" >
    .header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin: 0 auto;
        padding-top: 100px;
        padding-bottom: 50px;
        width: 92%;
        span {
            font-size: 24px;
            font-weight: 500;
            letter-spacing: -.5px;
        }
        .button-container {
            display: flex;
            flex-direction: row;
            gap: 25px;
            align-items: center;
        }
    }
</style>