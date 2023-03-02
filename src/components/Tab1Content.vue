<template>
  <div class="tab-content">
    <form>
      <div class="form-group">
        <label for="name">Name:</label>
        <input class="input-width" type="text" id="name" name="name">
      </div>
      <div class="form-group">
        <label for="age">Age:</label>
        <input class="input-width" type="number" id="age" name="age">
      </div>
      <div class="form-group">
        <label for="sex">Sex:</label>
        <select  id="sex" name="sex">
          <option value="male">Male</option>
          <option value="female">Female</option>
          <option value="other">Other</option>
        </select>
      </div>
      <div class="form-group">
        <label for="birthday">Birthday:</label>
        <input class="input-width" type="date" id="birthday" name="birthday">
      </div>
      <div class="form-group">
        <label for="email">Email:</label>
        <input class="input-width" type="email" id="email" name="email">
      </div>
      <div class="form-group">
        <label for="phone">Phone:</label>
        <input class="input-width" type="tel" id="phone" name="phone">
      </div>
      <div class="form-group">
        <label for="address">Address:</label>
        <input class="input-width" type="text" id="address" name="address">
      </div>
      <div class="form-group">
        <label for="city">City:</label>
        <input class="input-width" type="text" id="city" name="city">
      </div>
      <div class="form-group">
        <label for="state">State:</label>
        <input class="input-width" type="text" id="state" name="state">
      </div>
      <div class="form-group">
        <label for="zip">Zip Code:</label>
        <input class="input-width" type="text" id="zip" name="zip">
      </div>
      <div class="form-group">
        <label for="country">Country:</label>
        <input class="input-width" type="text" id="country" name="country">
      </div>
      <div class="form-group">
        <label for="occupation">Occupation:</label>
        <input class="input-width" type="text" id="occupation" name="occupation">
      </div>
      <div class="form-group">
        <label for="interests">Interests:</label>
        <textarea class="input-width" id="interests" name="interests"></textarea>
      </div>
    </form>
   <div class="button-container">
      <button class="save-button" @click="saveForm">Save</button>
      <button class="reset-button" @click="resetForm">Reset</button>
    </div>
  </div>
</template>
<script>
export default {
  name: 'Tab1Content',
  methods: {
    saveForm() {
      // handle form saving here
      console.log("Save")
    },
    resetForm() {
      // handle form resetting here
      console.log("Reset")
    }
  }
}
</script>
<style scoped>
.input-width {
  width: 400px; /* Set the width you want */
  border: 1px solid black;
}
.form-group {
  display: flex;
  align-items: center;
  margin-bottom: 1rem;
}

label {
  width: 8rem;
  margin-right: 1rem;
  text-align: right;
}

input [type="text"],
input [type="number"],
input [type="email"],
input [type="tel"],
input [type="date"],
textarea,
select {
  flex: 1;
}

button {
  padding: 0.5rem;
  margin-right: 1rem;
}

.save-button {
  background-color: #007bff;
  color: #fff;
  border: none;
}

.reset-button {
  background-color: #f8f9fa;
  color: #212529;
border: 1px solid #ced4da;
}
.save-button:active,
.reset-button:active {
  background-color: #0069d9;
  box-shadow: 0 0 0 rgba(0, 0, 0, 0.2);
}
.button-container {
display: flex;
justify-content: flex-end;
margin-top: 2rem;
}

.tab-content {
text-align: left;
margin-top: 2rem;
}

@media (max-width: 768px) {
label {
display: block;
width: 100%;
margin-right: 0;
margin-bottom: 0.5rem;
text-align: left;
}
}
</style>