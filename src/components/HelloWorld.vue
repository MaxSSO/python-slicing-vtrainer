<template>
  <div class="container vh-100 d-flex flex-column justify-content-center align-items-center">
    <img class="mb-5" src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/c3/Python-logo-notext.svg/1200px-Python-logo-notext.svg.png" alt="Python" style="width: 50px;" />
    <h1 class="h1" style="height: 48px;">
      {{ slicedWord }}
    </h1>
    <p class="text-center text-muted">
      Slice the word with Python slicing notation
    </p>
    <p class="text-center text-monospace text-dark">
      [start:end]
    </p>
    <form>
      <div class="form-row">
        <div class="col">
          <div class="form-group">
            <label class="d-block text-left" for="start">start</label>
            <input type="number" class="form-control" id="start" v-model.number="start">
          </div>
        </div>
        <div class="col">
          <div class="form-group">
            <label class="d-block text-right" for="end">end</label>
            <input type="number" class="form-control" id="end" v-model.number="end">
          </div>
        </div>
      </div>
    </form>
    <p class="text-center text-monospace text-primary">
      [{{ start }}:{{ end }}]
    </p>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      word: 'Hello World!',
      start: '',
      end: ''
    }
  },
  computed: {
    slicedWord () {
      if (!this.start && !this.end) {
        return this.word
      } else if (!this.end) {
        return this.word.slice(this.start)
      } else {
        return this.word.slice(this.start, this.end)
      }
    }
  }
}
</script>
