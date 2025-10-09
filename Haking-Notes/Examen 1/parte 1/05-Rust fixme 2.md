## Descripción 
The Rust saga continues? I ask you, can I borrow that, pleeeeeaaaasseeeee? Download the Rust code here. 
## Solución
- ejecutamos el programa y vemos que hay errores
- reparamos los errores:  falto mut que es un tipo de objeto, un return mal escrito un & que no va y falto mut en el objeto del final
- se aplican las siguietes correccciones

```rust
use xor_cryptor::XORCryptor;

fn decrypt(encrypted_buffer: Vec<u8>, borrowed_string: &mut String) { // <---- aquí faltó 'mut' en el parámetro
    // Key for decryption
    let key = String::from("CSUCKS");

    // Editing our borrowed value
    borrowed_string.push_str("PARTY FOUL! Here is your flag: ");

    // Create decryption object
    let res = XORCryptor::new(&key);
    if res.is_err() {
        return; // <---- esta es la forma correcta de retornar en Rust
    }
    let xrc = res.unwrap();

    // Decrypt flag and print it out
    let decrypted_buffer = xrc.decrypt_vec(encrypted_buffer); // <---- aquí sobra '&', debe ser sin referencia
    borrowed_string.push_str(&String::from_utf8_lossy(&decrypted_buffer));
    println!("{}", borrowed_string);
}

fn main() {
    // Encrypted flag values
    let hex_values = ["41", "30", "20", "63", "4a", "45", "54", "76", "01", "1c", "7e", "59", "63", "e1", "61", "25", "0d", "c4", "60", "f2", "12", "a0", "18", "03", "51", "03", "36", "05", "0e", "f9", "42", "5b"];

    // Convert the hexadecimal strings to bytes and collect them into a vector
    let encrypted_buffer: Vec<u8> = hex_values.iter()
        .map(|&hex| u8::from_str_radix(hex, 16).unwrap())
        .collect();

    let mut party_foul = String::from("Using memory unsafe languages is a: "); // <---- aquí faltó 'mut' para hacerla mutable
    decrypt(encrypted_buffer, &mut party_foul); // <---- aquí faltó 'mut' en la referencia
}
```

- se ejecuta y da:
solucion:
```
picoCTF{4r3_y0u_h4v1n5_fun_y31?}
```


