<template>
    <tr id="Tablazat">
        <td>{{ statue.person }}</td>
        <td>{{ statue.height }}</td>
        <td>{{ statue.price }}</td>
        <td>X</td>
    </tr>
</template>

<script>
export default {
  name: 'Tablazat',
  props: ['statue'],
  data: function() {
    return {
    }
  }
}
</script>

<style>
</style>