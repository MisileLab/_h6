# 안전한 변수

## 변할 수 없는 변수

Rust의 변수는 모두 unmutable합니다.

```rust
fn main() {
    let x = 5;
    println!("The value of x is: {x}");
    x = 6;
    println!("The value of x is: {x}");
}
```

JS와 달리 변수에 두 번 할당 할 수 없습니다.  
그 이유는 버그를 줄이기 위해서입니다.

### 변할 수 있는 변수

변할 수 있는(mutable) 변수를 위해서는 `let`을 `let mut`로 바꾸면 됩니다.

## 컴파일타임에 결정되는 상수

상수는 컴파일타임에 결정되는 특별한 수입니다.  
변할 수 없으며, 런타임에 영향받지 않는 타입을 가져야 합니다.

```rs
const MAX_POINTS: u32 = 100_000;
```

## 스코프와 재선언

Rust의 변수는 재선언할 수 있습니다.  
이 때 재선언한 값은 그 스코프(코드블럭) 안에서만 유지됩니다.

```rust
let x = 5;
{ // 스코프 시작

    let x = 20;
    println!("The value of x is: {x}");
    // x = 20

} // 스코프 끝
println!("The value of x is: {x}");

// x = 5
```
