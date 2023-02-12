<template>
  <div>
    <div>
      
        <b-navbar toggleable="lg" type="dark" variant="success">
          <b-container>
          <b-navbar-brand href="#">NavBar</b-navbar-brand>

          <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

          <b-collapse id="nav-collapse" is-nav>
            <b-navbar-nav>
              <b-nav-item href="#">About us</b-nav-item>
              <b-nav-item href="#">Contact us</b-nav-item>
              
            </b-navbar-nav>

            <!-- Right aligned nav items -->
            <b-navbar-nav class="ml-auto">
              <b-nav-form>
                <b-form-input
                  size="sm"
                  class="mr-sm-2"
                  placeholder="Search"
                ></b-form-input>
                <b-button variant="dark" size="sm" class="my-2 my-sm-0" type="submit"
                  >Search</b-button
                >
              </b-nav-form>

              <b-nav-item-dropdown text="services" right>
                <b-dropdown-item href="#">EN</b-dropdown-item>
                <b-dropdown-item href="#">ES</b-dropdown-item>
                <b-dropdown-item href="#">RU</b-dropdown-item>
                <b-dropdown-item href="#">FA</b-dropdown-item>
              </b-nav-item-dropdown>

              <b-nav-item-dropdown right>
                <!-- Using 'button-content' slot -->
                <template #button-content>
                  <em>User login</em>
                </template>
                <b-dropdown-item href="#">Profile</b-dropdown-item>
                <b-dropdown-item href="#">Sign Out</b-dropdown-item>
              </b-nav-item-dropdown>
            </b-navbar-nav>
          </b-collapse>
        </b-container>
        </b-navbar>

        <b-button variant="outline-info" class="mt-4 mx-4">Button</b-button>
        
    </div>
<div>
  <b-card  style="max-width: 200px;" class="mt-4 mx-3 img-top text-center" img-src="https://picsum.photos/600/300/?image=25" img-alt="image">
  <b-card-title>My card</b-card-title>
  <b-card-text>this is my first card ever in vuejs and bootstrap vue</b-card-text>
  <b-button  variant="success">Explore here</b-button>
  </b-card>
</div>
    
  </div>
 
  
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,

    data(){
      return{
        
      }
    }
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style></style>
