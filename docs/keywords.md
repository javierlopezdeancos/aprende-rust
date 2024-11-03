# Palabras clave o `keywords`

**Palabras clave** o `keywords`, El lenguaje Rust tiene un conjunto de palabras clave `keywords` que están reservadas para el uso exclusivo del lenguage, al igual que en otros lenguages. Tenga en cuenta que no puede usar estas palabras como nombres de variables o funciones. La mayoría de las palabras clave tienen significados especiales, y las usarás para realizar diversas tareas en tus programas de Rust; algunos no tienen ninguna funcionalidad actual asociada, pero se han reservado para la funcionalidad que podría agregarse a Rust en el futuro. Veamos una lista de las palabras clave:

## `Keywords` actualmente en uso

The following is a list of keywords currently in use, with their functionality described.

- `as` - Realizar la conversión a una primitiva, eliminar la ambigüedad del rasgo específico que contiene un elemento o cambiar el nombre de los elementos en las instrucciones de uso.
- `async` - Devuelve un `Future` en lugar de bloquear el hilo actual.
- `await` - Suspende la ejecución hasta que el resultado de un `Future` esté listo.
- `break` - Salir del loop inmediatamente.
- `const` - Define elementos constantes o `raw pointers` (punteros sin formato) constantes.
- `continue` - Continua con la siguiente iteración del bucle.
- `crate` - En un `path` de un módulo, se refiere a la raíz del `crate`.
- `dyn` - Envío dinámico a un objeto de `trait` (de caracteristica).
- `else` - Respaldo para flujos de control `if` y `if let`.
- `enum` - Define un enum (enumercion).
- `extern` - Enlazar una funcion o variable externa.
- `false` - Literal booleano falso.
- `fn` - Definir una función o el tipo de puntero de función.
- `for` - Recorrer elementos de un iterador, implementar un `trait` (característica) o especificar un tiempo de vida `higher-ranked` (de mayor rango).
- `if` - Rama basada en el resultado de una expresión condicional.
- `impl` - Implementar funcionalidad inherente o `trait` (característica).
- `in` - Parte de la sintaxis del bucle `for`.
- `let` - Vincular una variable.
- `loop` - Bucle incondicional
- `match` - Hacer coincidir un valor con patrones.
- `mod` - Define un modulo.
- `move` - Hacer que un `closure` se apropie de todas sus `captures` (capturas).
- `mut` - Denota mutabilidad en referencias, `raw pointers` (punteros sin formato) o `pattern bindings` (enlaces de patrones).
- `pub` - Denota visibilidad pública en `struct fields` (campos de estructura), `impl blocks` (bloques de implementación) o módulos.
- `ref` - Vincular por referencia.
- `return` - Retorno de una funcion.
- `Self` - Un `type alias` para el tipo que estamos definiendo o implementando.
- `self` - `Subject method` (método sujeto) o módulo actual.
- `static` - Variable global o `lifetime` (duración de vida) que dura toda la ejecución del programa.
- `struct` - Define una `structure` (estructura).
- `super` - Modulo padre del modulo actual.
- `trait` - Define una `trait` (característica).
- `true` - Literal booleano verdadero.
- `type` - Define un `type alias` (alias de un tipo) o asocia un tipo.
- `union` - Define una union; es solo una `keyword` (palabra clave) cuando se usa en una `union declaration`.
- `unsafe` - Denota código, funciones, características o implementaciones inseguras
- `use` - Traer símbolos al `scope` (ámbito de aplicació).
- `where` - Denotan cláusulas que restringen un tipo.
- `while` - Bucle condicional basado en el resultado de una expresión

## `Keywords` o palabras clave reservadas para su uso

Las siguientes palabras no tienen aun una funcionalidad establecida pero estan reservadas por Rust para un potensial futuro uso.

- `abstract`
- `become`
- `box`
- `do`
- `final`
- `macro`
- `override`
- `priv`
- `try`
- `typeof`
- `unsized`
- `virtual`
- `yield`

## Referencias

- [Oficial doc rust - keywords](https://doc.rust-lang.org/book/appendix-01-keywords.html)
