# 소유권 개념

소유권은 한개의 값은 한개의 변수에서만 가질수 있다는 개념입니다.

## 소유권 규칙

1. 데이타(값)은 항상 하나의 변수를 갖는다.(2개 이상의 다른 변수에 있을수 없다.)
2. 변수가 스코프(scope)를 벗어나면, 데이타(값)이 해제된다.

## 예시(규칙1)

```rust
fn main() {
    let a = "asdf".to_string(); // "asdf"라는 값을 a에 넣음
    println!("{a}");
    let b = a; // "asdf"라는 값을 b한테줌
    println!("{b}");
    println!("{a}"); // b한테 "asdf"라는 값을 줬기때문에 오류남
}
```

## 예시(규칙2)

```rust
fn main() {
    { // 스코프(scope) 시작
        let a = "asdf".to_string();
        println!("{a}");
    } // 스코프(scope) 끝나면서 a변수가 해제됨 
    println!("{a}") // 오류!!
}
```
