<script lang="ts">
  export let type = "primary";
  export let size = "medium";
  export let disabled = false;

  export let classList = "";

  $: classes = `btn ${type} ${size} ${disabled ? "disabled" : ""} ${classList}`;
</script>

<button class={classes}>
  <slot />
</button>

<style>
  .btn {
    padding: 10px 20px;
    border: none;
    cursor: pointer;
    border-radius: 100px;
  }

  .primary {
    border: 1px solid #000;
    background-color: #fff;
    color: #000;
  }

  .medium {
    font-size: 14px;
  }
</style>
