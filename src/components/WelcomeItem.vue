<template>
  <div class="item">
    <i>
      <slot name="icon"></slot>
    </i>
    <div class="details">
      <h2>
        <slot name="heading"></slot>
      </h2>
      <slot></slot>
    </div>
  </div>
</template>

<style scoped>
.item {
  margin-top: 2rem;
    position: relative;
    display: flex;
    align-items: center;
    color: whitesmoke;
    text-align: center;
    flex-direction: column;
}

.details {
  flex: 1;
  margin-left: 1rem;
}

i {
  display: flex;
  place-items: center;
  place-content: center;
  width: 100px;
  height: 100px;
  color: var(--color-text);
  place-self: center;
}

h3 {
  font-size: 1.2rem;
  font-weight: 500;
  margin-bottom: 0.4rem;
  color: whitesmoke;
}

@media (min-width: 1024px) {
  .item {
    margin-top: 0;
    display: flex;
    position: relative;
    align-items: center;
    flex-direction: column;
    text-align: center;
  }

  i {
    position: relative;
    border: 1px solid var(--color-border);
    background: var(--color-background);
    border-radius: 8px;
    width: auto;
    height: 10rem;
  }

  i img {
    height: 100%;
    object-fit: fill;
  }

  .item:before {
    content: ' ';
    position: absolute;
    left: 0;
    bottom: calc(50% + 25px);
    height: calc(50% - 25px);
  }

  .item:after {
    content: ' ';
    position: absolute;
    left: 0;
    top: calc(50% + 25px);
    height: calc(50% - 25px);
  }

  .item:first-of-type:before {
    display: none;
  }

  .item:last-of-type:after {
    display: none;
  }
}
</style>
