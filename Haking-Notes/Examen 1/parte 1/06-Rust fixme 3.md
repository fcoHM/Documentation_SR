## Descripción 
Have you heard of Rust? Fix the syntax errors in this Rust file to print the flag! Download the Rust code here.
## Solución
Este tenia comentado el inicio y cierre de un metodo
- se descomento el encabezado del metodo
- se descomento el cierre del metodo
```rust

   
    
    unsafe { // <---------este estaba comenatdo 
   
        let decrypted_buffer = xrc.decrypt_vec(encrypted_buffer);
        let decrypted_ptr = decrypted_buffer.as_ptr();
        let decrypted_len = decrypted_buffer.len();
        let decrypted_slice = std::slice::from_raw_parts(decrypted_ptr, decrypted_len);
        borrowed_string.push_str(&String::from_utf8_lossy(decrypted_slice));
    }
    println!("{}", borrowed_string);
} // <--------- este estaba comentado 
```

- se ejecuto y se optuvo
  ```
  picoCTF{n0w_y0uv3_f1x3d_1h3m_411}
  ```


