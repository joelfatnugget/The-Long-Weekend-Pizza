<template>
    <div class="p-8 max-w-md mx-auto bg-white rounded shadow-md">
      <h1 class="text-2xl font-bold mb-4">Pizza Order Form</h1>
      <div class="mb-4">
        <label for="name" class="block text-sm font-medium text-gray-700">Your Name:</label>
        <input type="text" v-model="name" id="name" required
               class="w-full px-4 py-2 border rounded focus:outline-none focus:border-blue-500"
               placeholder="Enter your name">
      </div>
  
      <form @submit.prevent="submitOrder">
        <!-- Pizza Type -->
        <label for="pizzaType">Select Pizza Type:</label>
        <select v-model="selectedPizzaType" id="pizzaType" required class="w-full px-2 my-2 py-2 border rounded focus:outline-none focus:border-blue-500">
          <option value="margherita">Margherita</option>
          <option value="pepperoni">Pepperoni</option>
          <option value="hamandonion">Ham & Onion</option>
          <option value="ratatouille">Ratatouille</option>
          <option value="hamandonion">Hawaiian</option>
          <option value="mushroomtruffle">Mushroom & Truffle Oil</option>
          <option value="meatmania">Meat Mania</option>
        </select>

        <!-- Phone Number -->
        
        <div class="mb-4">
        <label for="phoneNumber" class="block text-sm font-medium text-gray-700">Phone Number:</label>
        <input type="text" v-model="phoneNumber" id="phoneNumber" required
               class="w-full px-4 py-2 border rounded focus:outline-none focus:border-blue-500"
               placeholder="Enter your phone number">
      </div>
  
    
  
    
  
        <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full mx-auto block" type="submit">Place Order</button>
      </form>
  
      <div v-if="orderPlaced">
        <h2 class="text-lg font-bold">Order Summary:</h2>
        <p>Pizza Type: {{ selectedPizzaType }}</p>
        <p>Pizza Size: {{ phoneNumber }}</p>
        <p>Name: {{ name }}</p>

      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        selectedPizzaType: 'pepperoni',
        phoneNumber: '',
        name: '',
        orderPlaced: false
      };
    },
    methods: {
      submitOrder() {
        // You can implement the logic to send the order to the server here
        // For simplicity, we'll just set orderPlaced to true
        this.orderPlaced = true;
      }
    }
  };
  </script>
  
  <style scoped>
  /* Add your component-specific styles here */
  </style>
  