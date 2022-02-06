<template>
  <div>
    {{ counterContainer.count }}
  </div>
</template>

<script>
export default {
  inject: ['counterContainer'],
};
</script>
