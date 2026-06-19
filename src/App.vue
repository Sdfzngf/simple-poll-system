<template>
  <Form :modelValue="items"></Form>
  <hr />
  <Result :modelValue="items"></Result>
</template>

<script setup lang="ts">
import Form from '@/components/form/Form.vue';
import Result from '@/components/result/Result.vue';
import { ref } from 'vue';
import { IItem } from '@/models/item';

const templateItems: IItem[] = [
  {
    id: 'q1',
    type: 'selection',
    title: 'q1:你对瑞神的评价?',
    options: ['瑞神精彩极了', '瑞神还行', '瑞神糟糕透了'],
    result: {
      type: 'chart',
      chartType: 'doughnut'
    }
  },
  {
    id: 'q2',
    type: 'selection',
    title: 'q2:你对祥神的评价?',
    options: ['祥神夯爆了', '祥神一般', '祥神拉完了'],
    result: {
      type: 'chart',
      chartType: 'doughnut'
    }
  },
  {
    id: 'q3',
    type: 'selection',
    title: 'q3:您今天吃了吗?',
    options: ['吃了', '没有', '不知道'],
    result: {
      type: 'chart',
      chartType: 'doughnut'
    }
  }
];
const items = ref(templateItems);
</script>

<style scoped></style>
