# Palabras clave o `keywords`

**Palabras clave** o `keywords`, El lenguaje Rust tiene un conjunto de palabras clave `keywords` que están reservadas para el uso exclusivo del lenguage, al igual que en otros lenguages. Tenga en cuenta que no puede usar estas palabras como nombres de variables o funciones. La mayoría de las palabras clave tienen significados especiales, y las usarás para realizar diversas tareas en tus programas de Rust; algunos no tienen ninguna funcionalidad actual asociada, pero se han reservado para la funcionalidad que podría agregarse a Rust en el futuro. Veamos una lista de las palabras clave:

## `Keywords` o palabras clave actualmente en uso

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

## `Raw identifiers` (Identificadores sin formato)

Los `Raw identifiers` (identificadores sin formato) es la sintaxis que nos permite usar palabras clave donde normalmente no estarían permitidas. Para usar un identificador sin formato, tenemos que anteper `r#` a una palabra clave.

Por ejemplo, `match` es una palabra clave. Si intenta compilar la siguiente función que usa `match` como nombre:

```rust
fn match(needle: &str, haystack: &str) -> bool {
    haystack.contains(needle)
}
```

obtendremos el siguiente error

```shell
error: expected identifier, found keyword `match`
 --> src/main.rs:4:4
  |
4 | fn match(needle: &str, haystack: &str) -> bool {
  |    ^^^^^ expected identifier, found keyword
```

Podemos verlo en vivo en el [playground](https://play.rust-lang.org/?version=nightly&mode=debug&edition=2024&gist=6d34804c786e312503df1ff0bd2f288e)

El error indica que no se puede utilizar la palabra clave `match` como identificador de función. Para utilizar `match` como nombre de función, es necesario utilizar la sintaxis de `raw identifier` identificador sin formato, como se muestra a continuación:

```rust
fn r#match(needle: &str, haystack: &str) -> bool {
    haystack.contains(needle)
}

fn main() {
    assert!(r#match("foo", "foobar"));
}
```

Nos compilaria con exito

```shell
Compiling playground v0.0.1 (/playground)
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 0.59s
     Running `target/debug/playground`
```

podemos verlo en vivo en el [playground](https://play.rust-lang.org/?version=nightly&mode=debug&edition=2024&gist=904aad65bc0d0eb78d91a6a6c3c51142)

> [!NOTE]
> Ten en cuenta el prefijo `r#` en el nombre de la función en su definición, así como también dónde se llama a la función en main.

Los `raw identifier` (identificadores sin formato) te permiten usar cualquier palabra que elijas como identificador, incluso si esa palabra es una palabra clave reservada. Esto nos da más libertad para elegir los nombres de los identificadores, y nos permite integrarnos con programas escritos en un lenguaje donde estas palabras no son palabras clave. Además, los `raw identifier` (identificadores sin formato) te permiten usar bibliotecas escritas en una edición de Rust diferente a la que usa tu paquete. Por ejemplo, `try` no es una palabra clave en la edición 2015, pero sí en la edición 2018. Si dependes de una biblioteca escrita con la edición 2015 y tiene una función `try`, necesitarás usar la sintaxis de identificador sin formato, `r#try` en este caso, para llamar a esa función desde tu código de la edición 2018.

## Referencias

- [Oficial doc rust - keywords](https://doc.rust-lang.org/book/appendix-01-keywords.html)
