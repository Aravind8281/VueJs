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
                <tr>
                    <td>John doe</td>
                    <td>john@email.com</td>
                </tr>
            </tbody>
        </table>
    </div>
  </template>
  
  <script>
  export default {
    name: 'Employee-Card' 
  }
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
