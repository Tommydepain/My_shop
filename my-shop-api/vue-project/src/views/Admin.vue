<template>
    <div class="table-container">
      <h2 class="text-center">Liste des Produits</h2>
      <table class="table">
        <thead>
          <tr>
            <th>ID</th>
            <th>Nom du Produit</th>
            <th>Prix</th>
            <th>Modifier</th>
            <th>Supprimer</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="product in products" :key="product.id">
            <td>{{ product.id }}</td>
            <td>{{ product.name }}</td>
            <td>{{ product.price }}</td>
            <td>
              <button @click="editProduct(product)" class="edit-button">Modifier</button>
            </td>
            <td>
              <button @click="deleteProduct(product.id)" class="delete-button">Supprimer</button>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        products: [
          
        ],
      };
    },
    methods: {
      editProduct(product) {
        console.log('Modifier le produit:', product);
      },
      deleteProduct(productId) {
        
        console.log('Supprimer le produit avec ID:', productId);

        const requestOptions = { method: 'DELETE',
         headers : {"Authorization": "eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiJ9.eyJpYXQiOjE3MDAyNTcyMDksImV4cCI6MTcwMDI2MDgwOSwicm9sZXMiOlsiUk9MRV9BRE1JTiIsIlJPTEVfVVNFUiJdLCJ1c2VybmFtZSI6InRvbW15LmplYW4tamVhbkBlcGl0ZWNoLmRpZ2l0YWwifQ.cfoaU106f6biaULmTl6g2IfrqDvP13caj-U0s7xdWHfSnhAUjThOCdBIvwrM4VSIRFZusLJRHqWvQ2IOFZzAA3D3JAuwCyh0CdnmeppRjZ0xhnI_4oeSh7Sg6x8Aw3NKWbi_Ue6pCPxD_fkz7H9URjhoLoeRpafDjg-mJVTcOaMcVG0dlwu9JL1HHdeHMitIJtoEAh4sJgUJGMiwErjGrZqNf3Cz9Q7za-AzyUjuLzzz3PVgBW3I1i1M2nOObay7fl2YaQhf-FIYRRxlRL76MZY1a9Z5GaxU96NL3_X13gkWpNoxh8eFBJJ1UHzfZa_O5_G0loK1uHDpcN_nBfgxgA"} }   

        fetch('http://localhost/api/products/', requestOptions)
      },
    },
  };
  </script>
  
  <style scoped>
  .table-container {
    margin: 20px;
    text-align: center;
  }
  
  .table {
    width: 80%;
    margin: auto;
    border-collapse: collapse;
    margin-top: 10px;
  }
  
  .table th, .table td {
    border: 1px solid #ddd;
    padding: 8px;
    text-align: left;
  }
  
  .table th {
    background-color: #f2f2f2;
  }
  
  .edit-button, .delete-button {
    width: 100%;
    padding: 8px;
    margin-bottom: 5px;
  }
  
  .edit-button {
    background-color: #4CAF50;
    color: white;
  }
  
  .delete-button {
    background-color: #f44336;
    color: white;
  }
  </style>
  