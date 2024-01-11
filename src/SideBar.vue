<template>
    <nav class="flex-column">
        <div class="nav-item px-3">
            <span class="nav-link">
                <a href="#/"> <span class="bi bi-house-door-fill" aria-hidden="true"></span></a>
            </span>
        </div>

        <div class="nav-item px-3">
            <span class="nav-link">
                <a href="#/about"><span class="bi bi-plus-square-fill" aria-hidden="true"></span></a>
            </span>
        </div>

        <div class="nav-item px-3">
            <span class="nav-link">
                <a href="#/non-existent-path"><span class="bi bi-list-nested" aria-hidden="true"></span> </a>
            </span>
        </div>
    </nav>
</template>

<style>
.nav-item {
    font-size: 0.9rem;
    padding-bottom: 0.5rem;
}

.nav-item:first-of-type {
    padding-top: 1rem;
}

.nav-item:last-of-type {
    padding-bottom: 1rem;
}

.nav-item ::deep a {
    color: #d7d7d7;
    border-radius: 4px;
    height: 3rem;
    display: flex;
    align-items: center;
    line-height: 3rem;
}

.nav-item ::deep a.active {
    background-color: rgba(255, 255, 255, 0.37);
    color: white;
}

.nav-item ::deep a:hover {
    background-color: rgba(255, 255, 255, 0.1);
    color: white;
}

.nav-scrollable {
    display: none;
}

.navbar-toggler:checked~.nav-scrollable {
    display: block;
}
</style>