<script setup>
defineProps({
  msg: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <main>
    <header>
      <h1 class="site-title no-interact">SaveYourRecipes</h1>
      <div class="header-content">
        <img
          alt="Vue logo"
          class="logo no-interact"
          src="@/assets/logo.svg"
          width="125"
          height="125"
        />
        <div class="wrapper">
          <nav>
            <a
              class="no-select"
              href="https://docs.saveyour.recipes"
              target="_blank"
            >
              Docs
            </a>
            <a
              class="no-select"
              href="https://github.com/EleanorPrins/saveyourrecipes"
              target="_blank"
            >
              Github
            </a>
          </nav>
        </div>
      </div>
    </header>
    <div class="greetings">
      <h1 class="no-interact">Login</h1>
      <h5></h5>
      <div class="form">
        <input v-model="username" placeholder="Username" />
        <input type="password" v-model="password" placeholder="Password" />
        <button>Submit</button>
      </div>
    </div>
  </main>
</template>

<style>
body > div#app {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  min-height: 100vh;
}
</style>

<style scoped>
main {
  display: flex;
  flex-direction: column;
  gap: 3rem;
}

h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}
.site-title {
  font-family: "Vujahday Script";
  text-align: center;
  color: var(--color-text);
}

header {
  display: flex;
  flex-direction: column;
  max-height: 100vh;
}

.header-content {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.logo {
  display: block;
  margin: 0 auto 1rem;
}

nav {
  width: 100%;
  font-size: 12px;
  display: flex;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  width: 100%;
  padding: 0.2rem 1rem;
  margin: 0.5rem;
  color: var(--color-text);
  text-decoration: none;
  text-align: center;
}

nav a:hover {
  color: black;
  background-color: var(--color-text);
  border-radius: 4px;
  transition: all 0.3s ease;
}

button {
  display: block;
  width: 100%;
  max-width: 300px;
  margin: 1rem 0;
  padding: 0.5rem;
  font-size: 1rem;
  font-weight: 600;
  color: var(--color-background);
  background-color: var(--color-text);
  border: none;
  border-radius: 4px;
  cursor: pointer;
  user-select: none;
}

button:hover {
  background-color: var(--color-text-accent);
  transition: background-color 0.3s ease;
}

input:first {
  margin-top: 0;
}

input {
  display: block;
  width: 100%;
  max-width: 300px;
  margin: 1rem 0;
  padding: 0.5rem;
  font-size: 1rem;
  border: 1px solid var(--color-text-accent);
  border-radius: 4px;
  color: var(--color-background-opposite);

  background-color: var(--color-background-soft);
}

input:focus {
  background-color: var(--color-background-mute);
  outline: none;
}

input::placeholder {
  color: var(--color-text-accent);
  user-select: none;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h5 {
  text-align: center;
}

.greetings h5 {
  color: red;
  margin-top: -10px;
}

.greetings .form {
  display: flex;
  flex-direction: column;
  align-items: center;
}

@media (min-width: 1024px) {
  main {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    min-height: 80vh;
  }

  .greetings h1,
  .greetings h5 {
    text-align: left;
  }

  .greetings .form {
    align-items: flex-start;
  }

  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  .header-content {
    flex-direction: row;
    align-items: center;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    justify-content: center;
    flex-direction: column;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 2rem;
  }
}
</style>
