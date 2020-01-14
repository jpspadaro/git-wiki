# SSH in Rust

## libssh2
[Crate](https://crates.io/crates/ssh2)
[Docs](https://docs.rs/ssh2/)

```
use std::io::prelude::*;
use std::net::{TcpStream};
use ssh2::Session;

// Connect to the local SSH server
let tcp = TcpStream::connect("127.0.0.1:22").unwrap();
let mut sess = Session::new().unwrap();
sess.set_tcp_stream(tcp);
sess.handshake().unwrap();
sess.userauth_agent("username").unwrap();

let mut channel = sess.channel_session().unwrap();
channel.exec("ls").unwrap();
let mut s = String::new();
channel.read_to_string(&mut s).unwrap();
println!("{}", s);
channel.wait_close();
println!("{}", channel.exit_status().unwrap());
```

## libmussh
[Crate](https://crates.io/crates/libmussh)
[Docs](https://docs.rs/libmussh/1.0.1/libmussh/)

