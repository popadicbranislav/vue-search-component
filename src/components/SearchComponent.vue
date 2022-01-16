<script setup>
// your code goes here
</script>

<template>
  <div class="search">
    <input class="search__input" placeholder="search..." />
    <button class="search__btn">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        x="0px"
        y="0px"
        width="24"
        height="24"
        viewBox="0 0 24 24"
        style="fill: currentColor"
      >
        <path
          d="M 9 2 C 5.1458514 2 2 5.1458514 2 9 C 2 12.854149 5.1458514 16 9 16 C 10.747998 16 12.345009 15.348024 13.574219 14.28125 L 14 14.707031 L 14 16 L 20 22 L 22 20 L 16 14 L 14.707031 14 L 14.28125 13.574219 C 15.348024 12.345009 16 10.747998 16 9 C 16 5.1458514 12.854149 2 9 2 z M 9 4 C 11.773268 4 14 6.2267316 14 9 C 14 11.773268 11.773268 14 9 14 C 6.2267316 14 4 11.773268 4 9 C 4 6.2267316 6.2267316 4 9 4 z"
        ></path>
      </svg>
    </button>
  </div>
</template>

<style scoped>
.search {
  --primary: red;
  --size: 50px;

  display: flex;
  position: relative;
  border: 1px solid var(--primary);
  border-radius: 100vh;
  overflow: hidden;
  width: var(--size);
  height: var(--size);

  transition: width 300ms cubic-bezier(0.1, 0.9, 0.3, 1.1);
}

.search:focus-within {
  width: 100%;
}

.search:focus-within .search__input {
  opacity: 1;
  cursor: initial;
}

.search__input {
  font-size: 1.25rem;
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;

  padding: 0 1rem;
  border: 0;

  width: calc(100% - var(--size));

  opacity: 0;
  cursor: pointer;
}

.search__input {
  outline: none;
}

.search__btn {
  background: 0;
  border: 0;

  margin-left: auto;
  width: var(--size);
  height: var(--size);

  cursor: pointer;

  transition: color 300ms ease-in-out;
}

.search__btn:focus,
.search__btn:hover {
  outline: none;
  color: var(--primary);
}
</style>
