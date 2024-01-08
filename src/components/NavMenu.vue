<script setup>
import { ref } from "vue";
import { invoke } from "@tauri-apps/api/tauri";
import "../css/menu.css";

const greetMsg = ref("");
const name = ref("");

async function greet() {
    // Learn more about Tauri commands at https://tauri.app/v1/guides/features/command
    greetMsg.value = await invoke("greet", { name: name.value });
}
</script>

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
                <NavLink class="nav-link">
                    <span class="bi bi-house-door-fill" aria-hidden="true"></span> Home
                </NavLink>
            </div>

            <div class="nav-item px-3">
                <NavLink class="nav-link">
                    <span class="bi bi-plus-square-fill" aria-hidden="true"></span> Counter
                </NavLink>
            </div>

            <div class="nav-item px-3">
                <NavLink class="nav-link">
                    <span class="bi bi-list-nested" aria-hidden="true"></span> Weather
                </NavLink>
            </div>
        </nav>
    </div>
</template>
