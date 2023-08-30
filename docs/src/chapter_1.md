# Rust는 JS보다 빠릅니다

## Linux && MacOS

```sh
curl --proto '=https' --tlsv1.2 https://sh.rustup.rs -sSf | sh
```

만약에 MacOS에서 링커를 설치할 수 없다는 에러가 뜬다면, 아래의 명령어를 입력해주세요.  
만약 Linux라면 빌드에 필요한 패키지를 설치해주세요. ex) ubuntu라면 `build-essentials`

### MacOS

```sh
xcode-select --install
```

## Windows

Windows는 [이 링크](https://www.rust-lang.org/tools/install)를 참고해주세요.

## 컴파일러 점검

```sh
rustc --version
```

만약 에러가 난다면, `PATH`에 Rust의 경로를 추가해주세요. (Linux 기준)

## 업데이트 및 설치 제거

```sh
rustup update
rustup self uninstall
```
