<script setup>
  import EmployeesItem from './EmployeesItem.vue';

  const props = defineProps({
    data: {
      type: Object,
      required: true
    }
  });

</script>

<template>
  <ul className="app-list list-group">
    <EmployeesItem v-for="(employee, key) in props.data?.employees" :key="key" :name="employee.name" :salary="employee.salary" :isIncrease="employee.increase" :isRise="employee.rise" />
  </ul>
</template>

<style scoped>
.app-list {
  margin-top: 30px;
  background-color: #3d5a80;
  border-radius: 4px;
  box-shadow: 15px 15px 30px rgba(0,0,0, .15);
  color: #fff;
}
</style>