<template>
  <div class="container">
    <nav>
      <ul>
        <li>
          <NuxtLink to="/"><strong>Brand</strong></NuxtLink>
        </li>
      </ul>
      <ul>
        <li>
          <NuxtLink to="/"> <IconsHome /> Home </NuxtLink>
        </li>
        <li>
          <NuxtLink to="products">Products</NuxtLink>
        </li>
        <li>
          <NuxtLink to="contact"><IconsContact /> Contact</NuxtLink>
        </li>
        <li><NuxtLink to="about">About</NuxtLink></li>
        <li>
          <a href="#" @click="toggleDark()" role="button"> Dark </a>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script setup>
const isDark = useDark({
  selector: "html",
  attribute: "data-theme",
  valueDark: "dark",
  valueLight: "light",
});

const toggleDark = useToggle(isDark);
</script>
