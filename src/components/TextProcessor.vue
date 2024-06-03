<template>
  <div class="container mt-5">
    <div class="row justify-content-center">
      <div class="col-md-8">
        <div class="card">
          <div class="card-body">
            <h1 class="card-title mb-4 text-primary">Procesador de Texto</h1>
            <form @submit.prevent="processText">
              <div class="form-group">
                <label for="inputText" class="mb-2">Ingrese el texto:</label>
                <input 
                  type="text" 
                  id="inputText" 
                  v-model="inputText" 
                  class="form-control mb-3" 
                  @input="updateText"
                />
              </div>
            </form>
            <div class="processed-text">
              <p class="mb-2"><strong>Caracteres ingresados:</strong> <span class="badge badge-secondary">{{ charCount }}</span></p>
              <p class="mb-2"><strong>Codificado:</strong> <span class="badge badge-success">{{ encodedText }}</span></p>
              <p class="mb-2"><strong>Todo en mayúscula:</strong> <span class="badge badge-primary">{{ upperCaseText }}</span></p>
              <p class="mb-2"><strong>Todo en minúscula:</strong> <span class="badge badge-info">{{ lowerCaseText }}</span></p>
              <p class="mb-2"><strong>Intercalado (Mayúscula):</strong> <span class="badge badge-warning">{{ alternatingCaseText }}</span></p>
              <p class="mb-2"><strong>Intercalado (Minúscula):</strong> <span class="badge badge-danger">{{ alternatingCaseTextLower }}</span></p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      inputText: ''
    };
  },
  computed: {
    charCount() {
      return this.inputText.length;
    },
    encodedText() {
      return this.inputText.toLowerCase().replace(/[aeiou]/g, (vowel) => {
        const map = { a: 'u', e: 'o', i: 'i', o: 'e', u: 'a' };
        return map[vowel];
      });
    },
    upperCaseText() {
      return this.inputText.toUpperCase();
    },
    lowerCaseText() {
      return this.inputText.toLowerCase();
    },
    alternatingCaseText() {
      return this.alternateCase(this.inputText, true);
    },
    alternatingCaseTextLower() {
      return this.alternateCase(this.inputText, false);
    }
  },
  methods: {
    updateText() {
      this.$forceUpdate();
    },
    alternateCase(text, startWithUpperCase) {
      return text.split('').map((char, index) => {
        return index % 2 === (startWithUpperCase ? 0 : 1)
          ? char.toUpperCase()
          : char.toLowerCase();
      }).join('');
    }
  }
};
</script>

<style scoped>
.form-group {
  margin-bottom: 15px;
}

.processed-text p {
  margin-bottom: 5px;
}
</style>
