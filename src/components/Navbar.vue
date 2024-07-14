<template>
    <nav class="navbar navbar-expand-lg">
        <div class="container-fluid">
            <a class="navbar-brand" href="#">
                <img src="../assets/images/iFlowspace-Logo.png" alt="">
            </a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
                aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon custom-toggler"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav">
                    <li class="nav-item">
                        <a class="nav-link" href="#">about</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">what we do</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">residential</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link">commercial</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link">calculator</a>
                    </li>
                    <li class="nav-item last-item">
                        <a class="nav-itam-button">request a quote</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
</template>

<script>
export default {
    data() { },
};
</script>

<style>
.navbar {
    padding: 0 40px;
    background-color: #0E2442;
}

.navbar-nav {
    margin-left: auto;
    width: 95%;
    display: flex;
    justify-content: space-between;
}

.navbar-nav .nav-link {
    text-transform: uppercase;
    font-size: 16px;
    color: #fff;
    border-bottom: 1px solid transparent;
}

.navbar-nav .nav-link:hover {
    color: #EAC7A7;
    border-bottom: 1px solid #EAC7A7;
}

.last-item {
    width: 200px;
}

.nav-itam-button {
    display: inline-block;
    width: 100%;
    height: 100%;
    padding: 8px 10px;
    text-align: center;
    text-decoration: none;
    text-transform: uppercase;
    font-size: 16px;
    color: #fff;
    background-color: #E57661;
    border-radius: 5px;
    cursor: pointer;
}

@media (max-width:991px) {
    .navbar {
        padding: 10px;
    }

    .navbar-nav {
        margin-left: 0;
        padding-left: 10px;
        width: 100%;
        row-gap: 10px;
    }

    .navbar-toggler {
        border-color: #EAC7A7 !important;
    }

    .navbar-toggler-icon.custom-toggler {
  background-image: url("data:image/svg+xml;charset=UTF8,%3csvg viewBox='0 0 30 30' xmlns='http://www.w3.org/2000/svg'%3e%3cpath stroke='rgba(234,199,167,1)' stroke-width='2' d='M4 7h22M4 15h22M4 23h22'/%3e%3c/svg%3e");
}
}
</style>
