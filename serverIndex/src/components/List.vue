<template>
  <el-row :gutter="20" class="list-contain">
    <el-col :span="6" v-for="item in list" :key="item.id">
      <el-tag size="medium" @click="goto(item)">{{ item.name }}</el-tag>
    </el-col>
  </el-row>
</template>

<script setup>
import { defineProps, reactive } from "vue";

defineProps({
  list: Array,
});
const goto = (item) => {
  console.log("item", item);
  console.log("item", item.url);
  window.location.href = item.url;
};
</script>

<style scoped>
.list-contain {
  padding: 10px;
}
</style>
