# Rust의 특별한 함수

러스트는 함수 키워드로 fn을 사용합니다.

## 기본형

```rust
fn main() {
    another_func();
}

fn another_func() {
    println!("AnA moment");
}
```

## 매개변수를 가진 함수

```rust
fn main() {
    another_func(1, "asd");
}

fn another_func(a: usize, b: String) {
    println!("{} {}", a, b);
}
```

## 반환값을 가진 함수

```rust
fn main() {
    let a = factorial(10);
    println!("{}", a);
}

fn factorial(a: u128): u128 {
    (1..=num).product()
    // return (1..=num).product();
}
```
