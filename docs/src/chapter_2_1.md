# C보다 쉬운 라이브러리 정리

지금 프로젝트와 다른 곳에

```sh
cargo new hello_rust
```

를 치고 hello_rust 폴더로 들어가보세요.

## 의존성 관리 파일 Cargo.toml

Cargo.toml은 [toml](https://toml.io) 포맷을 사용한 의존성 관리 파일입니다.  
Cargo.toml은 다음과 같은 구조를 가지고 있습니다.

```toml
[package]
name = "hello_rust"
version = "0.1.0"
edition = "2021"

# See more keys and their definitions at https://doc.rust-lang.org/cargo/reference/manifest.html

[dependencies]
```

1. name은 패키지의 이름입니다.
2. version은 패키지의 버전입니다.
3. edition은 Rust의 표준 버전입니다. ex) C99 = C의 표준 버전

Cargo는 src 폴더에 모든 코드가 있다고 가정합니다.

## 빠른 의존성 관리를 위한 캐시 파일 Cargo.lock

Cargo.lock은 캐시 파일입니다.  
**절대** 건들지 마세요. (건들 시 책임 안 짐)

## Cargo를 이용한 컴파일

```sh
cargo build # debug mode
cargo build --release # release mode
```

이 컴파일의 결과물은 ./target/{build_target}/{package_name}입니다.

## Cargo를 이용한 실행

```sh
cargo run
cargo run --release
```

## 컴파일 없이, 체크

```sh
cargo check
```
