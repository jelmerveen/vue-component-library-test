<template>
  <div>
    <button class="btn btn-warning" @click="increment">{{ text }}</button>
  </div>
</template>
<script>
export default {
  props: {
    componentClasses: String
  },
  data() {
    return {
      count: 0
    };
  },
  computed: {
    times() {
      return this.count > 1 ? "times" : "time";
    },
    text() {
      return `I have been clicked ${this.count} ${this.times}`;
    }
  },
  methods: {
    increment() {
      this.count += 1;
    }
  }
};
</script>

<docs>
This button is amazing :)

## Examples

A simple counter:

```jsx
<counter />
```

</docs>