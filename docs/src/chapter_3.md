# Chapter 3 - JS 프로그래머를 위한 Rust

Rust의 변수는 모두 unmutable합니다.

```rs
fn main() {
    let x = 5;
    println!("The value of x is: {x}");
    x = 6;
    println!("The value of x is: {x}");
}
```

JS와 달리 변수에 두 번 할당 할 수 없습니다.  
그 이유는 버그를 줄이기 위해서입니다.

## 재할당 가능한 변수

재할당 가능한 변수를 위해서는 `let`을 `let mut`로 바꾸면 됩니다.
