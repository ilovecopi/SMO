FROM rust:1.89

WORKDIR /usr/src/app

RUN cargo install --locked trunk

RUN rustup target add wasm32-unknown-unknown

EXPOSE 8080

CMD ["bash"]
