<template>
    <div class="top-row ps-3 navbar navbar-dark">
        <div class="container-fluid">
            <a class="navbar-brand" href="">Avalon</a>
        </div>
    </div>

    <input type="checkbox" title="Navigation menu" class="navbar-toggler" />

    <div class="nav-scrollable" onclick="document.querySelector('.navbar-toggler').click()">
        <nav class="flex-column">
            <div class="nav-item px-3">
                <span class="nav-link">
                    <span class="bi bi-house-door-fill" aria-hidden="true"></span> <a href="#/">Home</a>
                </span>
            </div>

            <div class="nav-item px-3">
                <span class="nav-link">
                    <span class="bi bi-plus-square-fill" aria-hidden="true"></span> <a href="#/about">About</a>
                </span>
            </div>

            <div class="nav-item px-3">
                <span class="nav-link">
                    <span class="bi bi-list-nested" aria-hidden="true"></span> <a href="#/non-existent-path">Broken Link</a>
                </span>
            </div>
        </nav>
    </div>
</template>

<script>
export default {

}
</script>

<style></style>