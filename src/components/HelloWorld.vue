<script setup lang="ts">
  defineProps<{ msg: string }>();

  ElMessage({
    message: 'Congrats, this is a success message.',
    type: 'success',
  });
  const components = [
    {
      name: ElInput,
      attrs: {
        placeholder: ' ID',
        clearable: true,
      },
    },
    {
      name: ElTag,
      attrs: {
        type: 'success',
        text: 1023,
      },
    },
  ];
</script>

<template>
  <h1>{{ msg }}</h1>
  <el-button type="primary">66666</el-button>
  <div v-for="(props, i) in components" :key="i">
    <component v-bind="props.attrs" :is="props.name">
      {{ props.attrs.text }}
    </component>
  </div>
</template>
