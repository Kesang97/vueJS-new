<template>
    <div>
        <!-- navbar -->
        <div id="header" class="shadow-sm" style="background: #FFFFFF">
            <div class="container">
                <nav class="navbar navbar-expand py-2">
                    <button class="btn btn-lg" @click="drawer = !drawer">
                        <i class="fas fa-bars"></i>
                    </button>

                    <ul class="navbar-nav ml-auto">
                        <li class="nav-items">
                            <div class="input-group">
                                <input type="search" value="search" class="form-control py-2 border-right-0 border"
                                    placeholder="search model" style="background: #f0f0f7" />
                                <span class="input-group-append">
                                    <div class="input-group-text">
                                        <i class="search-icon fas fa-search"></i>
                                    </div>
                                </span>
                            </div>
                        </li>
                        <li class="nav-items">
                            <a href="#" class="nav-link pl-5 my-auto">
                                <i class="far fa-envelope"></i>



                            </a>
                        </li>
                        <li class="nav-items">
                            <a href="#" class="nav-link pl-5 my-auto">
                                <i class="far fa-bell"></i>
                            </a>
                        </li>
                        <li class="nav-items">
                            <div class="my-auto pl-5" style="cursor: pointer">
                                <img class="rounded-circle img-fluid" width="40px"
                                    src="https://mdbcdn.b-cdn.net/img/new/avatars/9.webp" />
                            </div>

                        </li>
                    </ul>
                </nav>
            </div>
        </div>
        <!-- side-bar -->
        <b-sidebar v-model="drawer">

            <div class="sidebar">
                <a href="#" class="active" v-for="(data, index) in dashItems" :key="index">
                    <span>
                        <font-awesome-icon :icon="data.icons" />
                        {{ data.title }}
                    </span>
                </a>
            </div>
        </b-sidebar>
    </div>
  
</template>

<script>
export default {
    name: "sidebar",

    data() {
        return {
            drawer: false,
            dashItems:[
                {
                    icons: 'fal fa-envelope', title:'Dashboard'
                },
                {
                    icons: 'fal fa-envelope', title:'Home'
                },
                {
                    icons: 'fal fa-envelope', title:'Categories'
                },
                {
                    icons: 'fal fa-envelope', title:'MenuItems'
                },
                {
                    icons: 'fal fa-envelope', title:'Orders'
                },
                {
                    icons: 'fal fa-envelope', title:'News'
                },
                {
                    icons: 'fal fa-envelope', title:'Settings'
                },

            ]
        };
    },
};
</script>

<style>
.search-icon {
    font-size: 20px;
    color: grey;
    cursor: pointer;
}

.navbar .btn i {
    font-size: 20px;
    color: #F94A29;
}

.nav-items a i {
    font-size: 22px;
    color: #B2B2B2;
}

.nav-items a i:hover {
    color: #F94A29;
}

/* sidebar */
.sidebar {
    position: fixed;
    height: 100%;
    width: 100%;
    margin: 0;
    padding: 0;
    overflow: auto;

}

.sidebar a {
    display: block;
    padding: 16px;
    text-decoration: none;
}

/* .sidebar a.active {
    background-color: #6096B4;
    color: white;
}

.sidebar a:hover:not(.active) {
    background-color: #93BFCF;
    color: white;
} */

@media screen and (max-width: 768px) {
    .sidebar {
        width: 100%;
        text-align: center;
        height: auto;
        position: relative;
    }

    .sidebar a {
        float: left;
    }
}
</style>
