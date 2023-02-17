<script>
  import DargAndDrop from "./dargAndDrop.svelte"

  let fileBlobUrl = null
  const handleDrop = (e) => {
    fileBlobUrl = URL.createObjectURL(e.detail.file)
  }
</script>

<DargAndDrop on:onChange={handleDrop} />
<img src={fileBlobUrl} alt="" />

<style lang="postcss" global>
  @tailwind base;
  @tailwind components;
  @tailwind utilities;
</style>
