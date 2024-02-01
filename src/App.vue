<script setup>
  import AppInfo from './components/AppInfo.vue';
  import SearchPanel from './components/SearchPanel.vue';
  import EmployeesFilter from './components/EmployeesFilter.vue';
  import EmployeesList from './components/EmployeesList.vue';
  import EmployeesAddForm from './components/EmployeesAddForm.vue';
</script>

<template>
  <div className="app">
    <AppInfo :employeesInfo="employeesInfo" />

    <div className="search-panel">
        <SearchPanel />
        <EmployeesFilter />
    </div>
    
    <EmployeesList />
    <EmployeesAddForm />
  </div>
</template>

<style scoped>
  .app {
    margin: 0 auto;
    max-width: 1000px;
  }

  .search-panel {
    margin-top: 30px;
    padding: 25px;
    background-color: #3d5a80;
    border-radius: 4px;
    box-shadow: 15px 15px 30px rgba(0,0,0, .15);
    color: #fff;
  }
</style>
