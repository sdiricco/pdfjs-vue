<template>
  <div ref="viewerContainer" class="pdf-viewer"></div>
</template>

<script>
export default {
  mounted() {
    // Carica viewer.html
    const viewerHtmlPath = 'pdfjs-4.0.379-legacy-dist/web/viewer.html'; // Assicurati di specificare il percorso corretto
    const iframe = document.createElement('iframe');
    iframe.src = viewerHtmlPath;
    iframe.style.width = '100%';
    iframe.style.height = '100%'; 
    iframe.style.borderWidth = '0px';
    this.$refs.viewerContainer.appendChild(iframe);
  }
};
</script>

<style scoped>
.pdf-viewer {
  width: 100vw;
  height: 100vh;
  overflow: hidden;
}
</style>
