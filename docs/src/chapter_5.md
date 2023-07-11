# if와 반복문

## if

js와 다르게 조건에 괄호를 쓸 필요 없습니다.  
조건은 무조건 bool이어야 합니다.

```rust
let a = 0;
if a > 0 {println!("asd")} else {println!("132")}
```

### let if

let if는 if문의 조건에 따라 변수를 선언합니다.  
이 때 두 결과물 (또는 else if를 사용할 시 여러 개)의 결과물의 타입은 무조건 똑같아야 합니다.

```rust
let a = 2;
let number = if a == 2 {2} else {1};
println!("{}", number);
```

## no while true

while true는 조건을 검사해야 하는 오버헤드가 존재하기 때문에, rust에서는 loop 키워드를 제공합니다.

```rust
let mut a = 20;
loop {
    if a == 0 {break;}
    println!("{}", a);
    a -= 1;
}
```
