<template>
    <Story title="Button Variants" description="Explore different button variants with customizable text.">
      <Variant title="Primary">
        <Button @click="hstEvent('click', $event)">{{ primaryText }}</Button>
      </Variant>
      <Variant title="Secondary">
        <Button variant="secondary" @click="hstEvent('click', $event)">{{ secondaryText }}</Button>
      </Variant>
  
      <template #controls>
        <HstText title="Primary Button Text" v-model="primaryText" />
        <HstText title="Secondary Button Text" v-model="secondaryText" />
        <HstText title="Large Primary Button Text" v-model="largePrimaryText" />
      </template>
    </Story>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  import { hstEvent } from 'histoire/client';
  import Button from './Button.vue';
  
  // Default texts for each variant
  const primaryText = ref('Primary');
  const secondaryText = ref('Secondary');
  </script>
  
  <docs lang="md">
  # Button Variants
  
  This story demonstrates different button variants, each with customizable text via controls. 
  
  ### Usage
  
  ```vue
  <template>
    <Button variant="primary" @click="onClick">Primary</Button>
  </template>
 ```
  </docs>
  