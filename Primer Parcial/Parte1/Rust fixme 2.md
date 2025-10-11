## Descripción:
The Rust saga continues? I ask you, can I borrow that, pleeeeeaaaasseeeee?Download the Rust code [here](https://challenge-files.picoctf.net/c_verbal_sleep/babfbee79718a6363826ba86300173ffde6d81577e9dd07d4130c53a7eecf6c3/fixme2.tar.gz).

# Solución
1.  **Descomprimir y entrar al directorio:**

    ```bash

    tar -xzf fixme2.tar.gz

    cd fixme2

    nano src/main.rs

    ```

  

2.  **Correcciones Mínimas en `src/main.rs`:**

  

    | **Ubicación** | **CÓDIGO ORIGINAL** | **CAMBIO (Añadir `mut`)** |

    | :--- | :--- | :--- |

    | **Función `decrypt`** | `borrowed_string: &String` | `borrowed_string: &**mut** String` |

    | **Variable `party_foul`** | `let party_foul = String::from(...)` | `let **mut** party_foul = String::from(...)` |

    | **Llamada a `decrypt`** | `decrypt(..., &party_foul)` | `decrypt(..., &**mut** party_foul)` |

  

3.  **Compilación y Ejecución:**

    ```bash

    cargo run

    ```

  

---


  

$$\text{picoCTF\{4r3\_y0u\_h4v1n5\_fun\_y31?\}}$$

## Notas

## Referencias
 