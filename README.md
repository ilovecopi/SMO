## 開発環境
- フロントエンド: Rust(Yew+WebAssembly) 
- バックエンド: Rust (Axum) 
- インフラ: AWS (Amplify, Lambda, API Gateway, RDS for PostgreSQL) 
- CI/CD: AWS Amplify, GitHub Actions

## Yewチュートリアルの注意点
- GitHub の最新版を Cargo.toml に指定する必要あり。'version = "0.21"'では、main.rsでコンパイルエラーが起きる。
```bash
cargo add yew
# 'component'がimportされずコンパイルエラーが起きる
```

```Cargo.toml
[dependencies]
# cargo addを使わずにファイル更新でgitのurlを指定
yew = { git = "https://github.com/yewstack/yew/", features = ["csr"] }
```

- Docker環境でTrunkを使う場合は `trunk serve --address 0.0.0.0` 