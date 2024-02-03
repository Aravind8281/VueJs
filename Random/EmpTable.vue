<template>
  <div id="emp-class">
    <table>
      <thead>
        <tr>
          <th>Name</th>
          <th>Email</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(employee, index) in employees" :key="index">
          <td>{{ employee.name }}</td>
          <td>{{ employee.email }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: 'EmployeeCard',
  props: {
    employees: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style scoped>
#emp-class {
  margin: 20px;
}

table {
  width: 100%;
  border-collapse: collapse;
  margin-top: 20px;
}

thead {
  background-color: #f2f2f2;
}

th, td {
  padding: 12px;
  border: 1px solid #ddd;
  text-align: left;
}

tr:hover {
  background-color: #f5f5f5;
}
</style>
