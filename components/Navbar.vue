<template>
  <div>
  <b-navbar toggleable="lg">
    <b-navbar-brand href="#">BimasaktiCooking</b-navbar-brand>

    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

    <b-collapse id="nav-collapse" is-nav>
      <b-navbar-nav>
        <b-nav-item href="#">Home</b-nav-item>
        <b-nav-item href="#">API</b-nav-item>
      </b-navbar-nav>

      <!-- Right aligned nav items -->
      <b-navbar-nav class="ml-auto">
         <b-nav-form>
                  <b-form-input 
                    size="sm" 
                    class="mr-sm-2" 
                    placeholder="Mau makan apa?"
                    v-model="meal"
                    ></b-form-input>
                  <b-button 
                    size="sm" 
                    class="my-2 my-sm-0" 
                    type="submit" 
                    @click.prevent="getMeal"
                    >Cari</b-button>
                </b-nav-form>

        <b-nav-item-dropdown text="Bahasa" right>
          <b-dropdown-item href="#">EN</b-dropdown-item>
          <b-dropdown-item href="#">ES</b-dropdown-item>
          <b-dropdown-item href="#">RU</b-dropdown-item>
          <b-dropdown-item href="#">FA</b-dropdown-item>
        </b-nav-item-dropdown>

        <b-nav-item-dropdown right>
          <!-- Using 'button-content' slot -->
          <template v-slot:button-content>
            <em>User</em>
          </template>
          <b-dropdown-item href="#">Profile</b-dropdown-item>
          <b-dropdown-item href="#">Sign Out</b-dropdown-item>
        </b-nav-item-dropdown>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</div>
</template>
<script>
export default {
    data() {
        return {
            meal: ''
      
        }
    },
  methods: {
    getMeal() {
     
    }
  }
}    
</script>
<style  scoped>
.navbar {
  background-color:cadetblue;
  color: black;
}
  
</style>