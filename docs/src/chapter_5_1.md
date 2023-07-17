# loop 반복문의 특별한 기능

loop반복문은 다른 반복문과 다르게 break를 좀더 특별하게 사용할수있습니다.

## break n

loop문을 나가면서 n을 반환합니다.

```rust
fn main(){
    let mut i = 2;
    let a = loop  {
        i *= i;
        if i > 1000{
            break i;
        }
    };
    println!("{a}")
}

```

이 코드는 i가 1000보다 클시 a에값에 들어갑니다.

## break 'name

'name: loop{...}이런식으로 할수있으며 break 'name을 사용해 name이라는 이름을 가진 반복문을 중단시킬수 있습니다.

```rust
fn main(){
    'name: loop{
        for i in 0..10{
            if i == 9{
                break 'name
            }
        }
    }
}
```

이 코드는 i가 9보다 클시 name반복문을 중단합니다.
