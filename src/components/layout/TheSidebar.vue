<template>
        <nav id="sidebarMenu" class="col-md-3 col-lg-2 d-md-block bg-dark sidebar collapse">
            <div class="position-sticky pt-1">
                <ul class="nav flex-column ">
                    <li class="nav-item bg-dark">
                        <router-link class="nav-link active" aria-current="page" :to="{name: 'dashboard'}">
                        <span data-feather="home"></span>
                        <h6 class="list-group-item list-group-item-action list-group-item-dark "><i class="fa-solid fa-gauge"></i> Page d'accueil</h6>
                        </router-link>
                    </li>
                </ul>

                <h6 class="sidebar-heading d-flex justify-content-between align-items-center px-3 mt-4 mb-1 text-muted">
                <span>Utilisateurs</span>
                <a class="link-secondary" href="#" aria-label="Add a new report">
                    <i class="fa fa-user"></i>
                </a>
                </h6>
                <ul class="nav flex-column mb-2 list-group">
                <li class="nav-item rounded-0 list-group-item list-group-item-action bg-dark">
                    <router-link class="nav-link text-orange" :to="{name: 'users'}">
                    <i class="fa fa-users"></i>
                      List des Admins
                    </router-link>
                </li>
                <li class="nav-item rounded-0 list-group-item list-group-item-action bg-dark">
                    <router-link class="nav-link text-orange" :to="{name: 'sellers'}">
                    <i class="fa fa-hand-holding-dollar"></i>
                      Liste des vendeurs
                    </router-link>
                </li>
                <li class="nav-item rounded-0 list-group-item list-group-item-action bg-dark">
                    <router-link class="nav-link text-orange" :to="{name: 'buyers'}">
                    <i class="fa fa-cart-shopping"></i>
                      Liste des acheteurs
                    </router-link>
                </li>

                </ul>

                <h6 class=" sidebar-heading d-flex justify-content-between align-items-center px-3 mt-4 mb-1 text-muted">
                <span>Services</span>
                <a class="link-secondary" href="#" aria-label="Add a new report">
                    <i class="fa fa-shop"></i>
                </a>
                </h6>
                <ul class="nav flex-column mb-2 list-group">
                <li class="nav-item rounded-0 list-group-item list-group-item-action bg-dark">
                    <router-link class="nav-link text-orange" :to="{name: 'services'}">
                    <i class="fa fa-house-laptop"></i>
                      List des services
                    </router-link>
                </li>
                <li class="nav-item rounded-0 list-group-item list-group-item-action bg-dark">
                    <router-link class="nav-link text-orange" :to="{ name: 'categories'}">
                    <i class="fa fa-bars-staggered"></i>
                      Liste des catégories
                    </router-link>
                </li>
                </ul>

                <h6 class=" sidebar-heading d-flex justify-content-between align-items-center px-3 mt-4 mb-1 text-muted">
                <span>Commandes</span>
                <router-link :to="{ name: 'orders' }" class="link-secondary" href="#" aria-label="Add a new report">
                    <i class="fa fa-magnifying-glass-dollar"></i>
                </router-link>
                </h6>
                <ul class="nav flex-column mb-2 list-group">
                <li class="nav-item rounded-0 list-group-item list-group-item-action bg-dark">
                    <router-link class="nav-link text-orange" :to="{name: 'orders'}">
                    <i class="fa fa-comments-dollar"></i>
                      Liste des commandes
                    </router-link>
                </li>
                <li class="nav-item rounded-0 list-group-item list-group-item-action bg-dark">
                    <router-link class="nav-link text-orange" :to="{ name: 'transaction'}">
                    <i class="fa fa-money-bill-transfer"></i>
                      Liste des transactions
                    </router-link>
                </li>
                </ul>

                <h6 class=" sidebar-heading d-flex justify-content-between align-items-center px-3 mt-4 mb-1 text-muted">
                <span>Compte</span>
                <a class="link-secondary" href="#" aria-label="Add a new report">
                    <i class="fa fa-user-gear"></i>
                </a>
                </h6>
                <ul class="nav flex-column mb-2 list-group">
                <li class="nav-item rounded-0 list-group-item list-group-item-action bg-dark">
                    <router-link class="nav-link text-orange" :to="{name: 'profile'}">
                    <i class="fa fa-id-card"></i>
                      Mon profil
                    </router-link>
                </li>
                </ul>

            </div>
        </nav>
</template>

<style scoped>
.sidebar {
    position: fixed;
    top: 0;
    /* rtl:raw:
    right: 0;
    */
    bottom: 0;
    /* rtl:remove */
    left: 0;
    z-index: 100; /* Behind the navbar */
    padding: 48px 0 0; /* Height of navbar */
    box-shadow: inset -1px 0 0 rgba(0, 0, 0, .1);
}

@media (max-width: 767.98px) {
    .sidebar {
        top: 5rem;
    }
}

.sidebar-sticky {
    position: relative;
    top: 0;
    height: calc(100vh - 48px);
    padding-top: .5rem;
    overflow-x: hidden;
    overflow-y: auto; /* Scrollable contents if viewport is shorter than content. */
}

.sidebar .nav-link {
    font-weight: 500;
    color: #333;
    padding: 0px;
}

.sidebar .nav-link .feather {
    margin-right: 4px;
    color: #727272;
}

.sidebar .nav-link.active {
    color: #2470dc;
}

.sidebar .nav-link:hover .feather,
.sidebar .nav-link.active .feather {
    color: inherit;

}

.sidebar-heading {
    font-size: 1rem;
    text-transform: uppercase;
}
.sidebar .nav-item{
    padding: 0px;
}
.sidebar .nav-link{
    padding: .5rem 1rem;
}
.sidebar .nav-item:hover{
    background-color: #ff5b27 !important;
    color: black;

}
.sidebar .nav-link:hover{
    color: black !important;
}

.text-orange{
    color: #ff5b27 !important;
}
</style>
