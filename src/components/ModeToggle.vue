<template>
  <div class="toggle-wrapper">
    <label class="toggle">
      <input
        type="checkbox"
        :checked="isDark === 'dark-theme' ? 'checked' : 'false'"
        @change="$emit('toggle')"
      />
      <span class="toggler round"></span>
    </label>
    <p class="caption" v-if="isDark">sötét</p>
    <p class="caption" v-else>világos</p>
  </div>
</template>

<script>
export default {
  props: ['isDark'],
  data() {
    return {
      isHovered: false,
    };
  },
};
</script>

<style>
.toggle-wrapper {
  display: flex;
  flex-direction: column;
  place-items: center;
}

.toggle {
  display: inline-block;
  width: 46px;
  margin-top: -15px;
  margin-bottom: 4px;
}

.toggle input {
  opacity: 0;
  width: 0;
  height: 0;
}

.toggler {
  cursor: pointer;
  top: 0;
  left: 0;
  display: flex;
  background: var(--color-text);
  outline: 1px solid var(--color-background);
  -webkit-transition: 0.4s ease-in;
  transition: 0.4s ease-in;
  padding: 3px 0;
}

.toggler:before {
  content: '';
  height: 15px;
  width: 15px;
  left: 2px;
  background: var(--color-background);
  border: var(--color-background);
  -webkit-transition: 0.4s;
  transition: 0.4s;
}

input:checked + .toggler {
  background: var(--color-text);
}

input:focus + toggler {
  box-shadow: 0 0 2px var(--sp-black);
}

input:checked + .toggler:before {
  -webkit-transform: translateX(26px);
  -ms-transform: translateX(26px);
  transform: translateX(26px);
}

.toggler.round {
  border-radius: 34px;
}
.toggler.round:before {
  border-radius: 50%;
}
</style>
