# 참조타입(reference type)
참조는 값을 빌린것입니다.

## 참조타입 종류
잠조타입은  수정이 불가능한 참조타입(&T)과 수정가능한 참조타입(&mut T)이 있습니다.

## 예시1
```rust
fn main(){
    let mut a: isize = 1;
    println!("변경전: {a}");
    let b: &mut isize = &mut a; // 1
    *b = 2; // 2
    println!("변경후: {a}");
}
```
1. 앰퍼샌드(&)를 붙임여서 b의값을 참조하였습니다.
2. 에스터리스크(*)를 붙여 값을 변경하였습니다.


## 예시2
```rust
fn main(){
    let mut a: isize = 1;
    println!("변경전: {a}");
    change(&mut a, 2);
    println!("변경후: {a}");
}
fn change(a: &mut isize, b: isize){
    *a = b
}
```
함수에서도 이런식으로 활용할수있습니다.
