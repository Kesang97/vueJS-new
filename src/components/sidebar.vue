<template>
<div>
    <!-- navbar -->
    <div id="header" style="background: #E1EEDD">
        <div class="container">
            <nav class="navbar navbar-expand">
                <a href="#" class="" @click="drawer = !drawer">
                    <i class="side-icon fas fa-bars"></i>
                </a>

                <ul class="navbar-nav ml-auto">
                    <li class="nav-items">
                        
                    <div class="input-group" >
                        <input type="search" value="search" class="form-control py-2 border-right-0 border" placeholder="search model" style="border-radius: 30px solid #E1EEDD;">
                        <span class="input-group-append">
                            <div class="input-group-text bg-transparent">
                                <i class="fas fa-search"></i>
                            </div>
                           
                        </span>
                      
                    </div>
              
                    </li>
                </ul>
                
            </nav>
        </div>
        

    </div>
    
    <!-- side-bar -->
   
    <b-sidebar  sidebar-class="border-right border-danger" v-model="drawer">
        <div class="header" style="background: #E1EEDD; ">
            <div class="img text-center px-auto">
                <img src="../assets/side_logo.png" class="img-fluid" width="120px" alt="">
            </div>
            

            <div>

    <b-navbar-nav>
      <b-nav-item href="#">Home</b-nav-item>

      <!-- Navbar dropdowns -->
      <b-nav-item-dropdown text="Dashboard" left>
        <b-dropdown-item>Food</b-dropdown-item>
        
      </b-nav-item-dropdown>

      <b-nav-item-dropdown text="Menus" left>
        <b-dropdown-item href="#">Menu Catalogue</b-dropdown-item>
        <b-dropdown-item href="#">Menu List</b-dropdown-item>
        <b-dropdown-item href="#">Menu Grid</b-dropdown-item>
        <b-dropdown-item href="#">Add product</b-dropdown-item>
        <b-dropdown-item href="#">Product detail</b-dropdown-item>
         </b-nav-item-dropdown>
         <b-nav-item href="#">Orders</b-nav-item>
         <b-nav-item href="#">Restaurants List</b-nav-item>
         <b-nav-item-dropdown text="Customers" left>
        <b-dropdown-item href="#">Customers List</b-dropdown-item>
        <b-dropdown-item href="#">Customers Review</b-dropdown-item>
        <b-dropdown-item href="#">Social Activity</b-dropdown-item>
    </b-nav-item-dropdown>

    <b-nav-item href="#">Sales</b-nav-item>
   
    </b-navbar-nav>

</div>

        </div>
    </b-sidebar>

</div>

</template>

<script>
export default{
    name:'sidebar',

    data(){
        return{
            drawer: false,
        }
    }
    
}

</script>

<style>
.side-icon{
    font-size: 20px;
    color: red;
}

</style>