<template>
  <div id="content">
    <div class="editor">
      <h3 class="title">Markdown Editor</h3>
      <textarea rows="20" v-model="markdownText"></textarea>
    </div>
    <div class="preview">
      <h3 class="title">Markdown Preview</h3>
      <div v-html="previewText"></div>
    </div>
  </div>
</template>

<script>
import marked from 'marked'

export default {
  data() {
    return {
      markdownText: `An h1 header
============

Paragraphs are separated by a blank line.

2nd paragraph. *Italic*, **bold**, and \`monospace\`.

Itemized lists look like:
  * this one
  * that one
  * the other one`
    }
  },
  computed: {
    previewText() {
      marked.setOptions({
        render: new marked.Renderer(),
        gfm: true,
        tables: true,
        breaks: true,
        pedantic: false,
        sanitize: true,
        smartLists: true,
        smartypants: false
      })
      return marked(this.markdownText)
    }
  }
}
</script>

<style scoped>
#content {
  width: 90%;
  margin: 0 auto;
  padding-bottom: 60px;
}
.editor,
.preview {
  flex-basis: 46%;
  margin-bottom: 40px;
}
.editor {
  display: flex;
  flex-direction: column;
}
.editor > textarea {
  flex: 1;
}
.title {
  padding: 10px 0;
  text-align: center;
  margin-bottom: 30px;
  color: #32673f;
}

@media (min-width: 900px) {
  #content {
    display: flex;
    justify-content: space-between;
  }
  .title {
    text-align: start;
  }
  .editor {
    display: flex;
    flex-direction: column;
  }
  .editor > textarea {
    flex: 1;
  }
}
</style>
