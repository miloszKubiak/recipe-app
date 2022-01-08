<template>
  <div class="home">
    <h1><i class="fas fa-cookie-bite"></i> My Recipes</h1>
    <button>Add new Recipe</button>
    <div class="recipes">
      <div class="card">
        <h2>title1</h2>
        <p>description</p>
        <button>View Recipe</button>
      </div>
    </div>
  </div>

  <div class="add-recipe-popup">
    <div class="popup-content">
      <h2>Add new Recipe</h2>

      <form @submit.prevent="addNewRecipe">
        <div class="group">
          <label>Title</label>
          <input type="text">
        </div>

        <div class="group">
          <label>Description</label>
          <textarea></textarea>
        </div>

        <div class="group">
          <label>Ingredients</label>
          <div class="ingredient">
            <input type="text">
          </div>
          <button type="button">Add Ingredient</button>
        </div>

        <div class="group">
          <label>Method</label>
          <div class="method">
            <textarea></textarea>
          </div>
          <button>Add Step</button>
        </div>

        <button type="submit">Add Recipe</button>
        <button type="button">Close</button>
      </form>
    </div>
  </div>
</template>

<script>

export default {
  name: 'Home',
}
</script>

<style>
.home {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 1rem;
}

h1 {
  font-size: 3rem;
  margin-bottom: 3rem;
}

.recipes {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.recipes .card {
  padding: 1.5rem;
  background-color: #97BFB4;
  border-radius: 5px;
  margin: 1rem;
}

.recipes .card h2 {
  font-size: 2.5rem;
  margin-bottom: 1rem;
}

.recipes .card p {
  font-size: 1.1rem;
  line-height: 2;
  margin-bottom: 1rem;
}

.add-recipe-popup {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 2rem;
  background-color: rgba(0, 0, 0, 0.5);
}

.add-recipe-popup .popup-content {
  background-color: #F5EEDC;
  padding: 2rem;
  border-radius: 1rem;
  border: 5px solid #DD4A48;
  width: 100%;
  max-width: 768px;
}

.popup-content h2 {
  font-size: 2rem;
  margin-bottom: 1rem;
}

.popup-content .group {
  margin-bottom: 1rem;
}

.popup-content .group label {
  display: block;
  margin-bottom: .5rem;
}

.popup-content .group input,
.popup-content .group textarea {
  display: block;
  width: 100%;
  padding: .5rem;
  border: 1px solid #4F091D;
  border-radius: 5px;
  margin-bottom: 1rem;
}

.popup-content .group textarea {
  height: 100px;
  resize: none;
}

.popup-content button[type="submit"] {
  margin-right: 1rem;
}
</style>