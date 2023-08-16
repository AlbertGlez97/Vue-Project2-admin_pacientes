# La directiva v-model 

Es una directiva específica de Vue que crea una asociación bidireccional entre un elemento del DOM y una propiedad de un objeto de datos. Esto significa que cuando el usuario cambia el valor del elemento del DOM, la propiedad del objeto de datos se actualizará y viceversa.

Por ejemplo, el siguiente código creará una asociación bidireccional entre el campo de entrada nombre y la propiedad nombre del objeto de datos usuario:

```
<script setup>
import { reactive } from "vue";

const paciente = reactive({
nombre : ''
});
</script>

<template>
{{ paciente.nombre }}
      <div class="mb-5">
        <label for="mascota" class="block text-gray-700 uppercase font-bold"
          >Nombre de la mascota</label
        >
        <input
          id="mascota"
          type="text"
          placeholder="Nombre de la mascota"
          class="border-2 w-full p-2 mt-2 placeholder-gray-400 rounded-md"
          v-model="paciente.nombre"
        />
      </div>
</template>
```

Cuando el usuario escriba algo en el campo de entrada nombre, el valor de la propiedad nombre del objeto de datos usuario se actualizará. Y viceversa, cuando el valor de la propiedad nombre del objeto de datos usuario se actualice, el campo de entrada nombre se actualizará con el nuevo valor.

La directiva v-model se puede usar con cualquier elemento del DOM que admita la entrada de usuario, como campos de entrada, casillas de verificación y botones. También se puede usar con componentes de Vue.

La directiva v-model es una herramienta poderosa que puede simplificar la escritura de código de interfaz de usuario. Al usar v-model, puede crear interfaces de usuario que son receptivas y fáciles de usar.