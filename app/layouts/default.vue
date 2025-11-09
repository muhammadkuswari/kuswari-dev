<script setup lang="ts">
import type { NavigationMenuItem } from "@nuxt/ui";

const route = useRoute();

const navbarItems = computed<NavigationMenuItem[]>(() => [
  {
    label: "Home",
    to: "/",
    active: route.path.startsWith("/"),
  },
  {
    label: "Projects",
    to: "/projects",
    active: route.path.startsWith("/projects"),
  },
  {
    label: "Blogs",
    to: "/blogs",
    active: route.path.startsWith("/blogs"),
  },
]);
</script>

<template>
  <!-- navbar -->
  <UHeader>
    <template #title>
      <h1 class="text-primary">kuswari.</h1>
    </template>

    <UNavigationMenu :items="navbarItems" :highlight="true" />

    <template #right>
      <UColorModeButton />

      <UTooltip text="Connect at LinkedIn">
        <UButton
          color="info"
          variant="ghost"
          to="https://www.linkedin.com/in/muhammadkuswari/"
          target="_blank"
          icon="i-simple-icons-linkedin"
          aria-label="LinkedIn"
        />
      </UTooltip>
    </template>

    <template #body>
      <UNavigationMenu
        :items="navbarItems"
        orientation="vertical"
        class="-mx-2.5"
      />
    </template>
  </UHeader>

  <!-- attach content here -->
  <slot />

  <USeparator type="dashed" class="h-px" />
  <!-- footer -->
  <UFooter>
    <template #left>
      <p class="text-muted text-sm">
        Copyright © {{ new Date().getFullYear() }} | Muhammad Kuswari
      </p>
    </template>

    <template #right>
      <UButton
        icon="i-simple-icons-instagram"
        color="neutral"
        variant="ghost"
        to="https://go.nuxt.com/discord"
        target="_blank"
        aria-label="Instagram"
      />
      <UButton
        icon="i-simple-icons-facebook"
        color="neutral"
        variant="ghost"
        to="https://www.facebook.com/muh.kuswari/?locale=id_ID"
        target="_blank"
        aria-label="Facebook"
      />
      <UButton
        icon="i-simple-icons-github"
        color="neutral"
        variant="ghost"
        to="https://github.com/muhammadkuswari"
        target="_blank"
        aria-label="GitHub"
      />
    </template>
  </UFooter>
</template>
