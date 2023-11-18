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
        <tr v-for="product in apiData" :key="product.id">
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
      apiData: null,
      products: [],
    };
  },
  mounted() {
    this.loadData();
  },
  methods: {
    editProduct(product) {
      console.log('Modifier le produit:', product);
    },
    deleteProduct(productId) {
      console.log('Supprimer le produit avec ID:', productId);

      const requestOptions = {
        method: 'DELETE',
        headers: {
          'Authorization': 'Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiJ9.eyJpYXQiOjE3MDAzMjcxMzUsImV4cCI6MTcwMDMzMDczNSwicm9sZXMiOlsiUk9MRV9BRE1JTiIsIlJPTEVfVVNFUiJdLCJ1c2VybmFtZSI6InRvbW15LmplYW4tamVhbkBlcGl0ZWNoLmRpZ2l0YWwifQ.CXskLNaY4If7GfvFJfqiXCaXTVIfkTWRbayH9jH7mMUZ8mI1DqOO_9dZNuGw0kQhcyMVndVEjjY7C0IPLkNIbuNvNrWaaF9ag7G3fQfYsH7ByDnl1QAS43IaMdLOKc86JH_TKPq_3QGqHZMQv5skFDSKVDvgnMAUD_vnohVamtbfceTJXa0dnsTvrpQiPPQG0jM6Efd20wJTGw895TV9lOb7te44i1oycZUoJJAk4NqqwglWnEngn2Opoauod2IRmE0AnpuTMvcfyRGmDAG_3Yybr_usPGeJFgbpivqPtEc3L36eoXVbLXKZJ6tz2YdVNtchWrTUSmHkNktnffkGUg',
        },
      };

      fetch(`http://localhost/api/products/${productId}`, requestOptions)
        .then(response => {
          if (response.ok) {
            console.log('Produit supprimé avec succès.');
            this.loadData();
          } else {
            console.error('Erreur lors de la suppression du produit.');
          }
        })
        .catch(error => {
          console.error('Erreur lors de la requête de suppression:', error);
        });
    },
    loadData() {
      this.getApiData('http://localhost/api/products/');
    },
    getApiData(apiURL) {
      fetch(apiURL, {
        headers: {
          'Authorization': 'Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiJ9.eyJpYXQiOjE3MDAzMjcxMzUsImV4cCI6MTcwMDMzMDczNSwicm9sZXMiOlsiUk9MRV9BRE1JTiIsIlJPTEVfVVNFUiJdLCJ1c2VybmFtZSI6InRvbW15LmplYW4tamVhbkBlcGl0ZWNoLmRpZ2l0YWwifQ.CXskLNaY4If7GfvFJfqiXCaXTVIfkTWRbayH9jH7mMUZ8mI1DqOO_9dZNuGw0kQhcyMVndVEjjY7C0IPLkNIbuNvNrWaaF9ag7G3fQfYsH7ByDnl1QAS43IaMdLOKc86JH_TKPq_3QGqHZMQv5skFDSKVDvgnMAUD_vnohVamtbfceTJXa0dnsTvrpQiPPQG0jM6Efd20wJTGw895TV9lOb7te44i1oycZUoJJAk4NqqwglWnEngn2Opoauod2IRmE0AnpuTMvcfyRGmDAG_3Yybr_usPGeJFgbpivqPtEc3L36eoXVbLXKZJ6tz2YdVNtchWrTUSmHkNktnffkGUg',
        }
      })
        .then(response => response.json())
        .then(data => {
          this.apiData = data['hydra:member'];
          console.log(this.apiData);
        })
        .catch(error => console.error('Erreur:', error));
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
