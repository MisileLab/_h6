# 간단한 프로그래밍

## Hello, world

```rust
fn main() {
    println!("Hello, world!");
}
```

## 컴파일 하는 방법

```sh
rustc main.rs
./main # windows is .\main.exe
```

## 코드 뜯어보기

```rs
fn main() {

}
```

이 부분은 main 함수입니다.  

```rs
println!("Hello, world!");
```

1. println은 함수의 이름입니다.
2. !는 rust만의 특별한 macro라는 기능입니다. (나중에 배움)
3. "Hello, world!"는 함수의 인자입니다.
4. Rust는 거의 모든 경우에 세미콜론을 사용합니다.
