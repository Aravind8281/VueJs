<template>
    <div class="form">
      <form @submit.prevent="submitForm">
        <label for="name">Name:</label>
        <input type="text" v-model="newEmployee.name" required />
  
        <label for="email">Email:</label>
        <input type="email" v-model="newEmployee.email" required />
  
        <button type="submit">Add Employee</button>
      </form>
    </div>
  </template>
  
  <script>
  export default {
    name: "EmpForm",
    data() {
      return {
        newEmployee: {
          name: "",
          email: "",
        },
      };
    },
    methods: {
      submitForm() {
        this.$emit("addEmployee", { ...this.newEmployee });
        this.newEmployee = { name: "", email: "" };
      },
    },
  };
  </script>
  
  <style scoped>
  .form {
    max-width: 400px;
    margin: auto;
    padding: 20px;
    border: 1px solid #ccc;
    border-radius: 8px;
  }
  
  form {
    display: flex;
    flex-direction: column;
  }
  
  label {
    margin-bottom: 8px;
    font-weight: bold;
  }
  
  input {
    padding: 8px;
    margin-bottom: 16px;
    border: 1px solid #ccc;
    border-radius: 4px;
  }
  
  button {
    background-color: #4caf50;
    color: white;
    padding: 10px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    font-size: 16px;
  }
  
  button:hover {
    background-color: #45a049;
  }
  </style>
  
