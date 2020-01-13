# Rust
[Homepage](https://www.rust-lang.org/)

## Concurrency

### With Rayon

#### par_iter examples

```
use rayon::prelude::*;
fn sum_of_squares(input: &[i32]) -> i32 {
    input.par_iter()
         .map(|i| i * i)
         .sum()
}
```

```
use rayon::prelude::*;

(0..100).into_par_iter().for_each(|x| println!("{:?}", x));
```



*With channels (using mpsc):*
```
use std::sync::mpsc::channel;
use rayon::prelude::*;

let (sender, receiver) = channel();

(0..5).into_par_iter().for_each_with(sender, |s, x| s.send(x).unwrap());

let mut res: Vec<_> = receiver.iter().collect();

res.sort();

assert_eq!(&res[..], &[0, 1, 2, 3, 4])
```

There are a bunch of useful methods in here:
[Docs](https://docs.rs/rayon/1.0.3/rayon/iter/index.html)
```


## SSH? - Not tested yet
[libmush](https://docs.rs/libmussh/1.0.1/libmussh/)
