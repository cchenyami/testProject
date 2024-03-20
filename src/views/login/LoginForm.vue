<template>
    22
  </template>
  <script lang="ts">
  import { defineComponent, reactive, computed } from 'vue';
  interface FormState {
    username: string;
    password: string;
    remember: boolean;
  }
  export default defineComponent({
    components: {
    },
    setup() {
      const formState = reactive<FormState>({
        username: '',
        password: '',
        remember: true,
      });
      const onFinish = (values: any) => {
        console.log('Success:', values);
      };
  
      const onFinishFailed = (errorInfo: any) => {
        console.log('Failed:', errorInfo);
      };
      const disabled = computed(() => {
        return !(formState.username && formState.password);
      });
      return {
        formState,
        onFinish,
        onFinishFailed,
        disabled,
      };
    },
  });
  </script>
  <style>
  </style>
  