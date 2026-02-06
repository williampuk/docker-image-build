FROM rockylinux:9

# System dependencies for Rust + bindgen
RUN dnf -y install \
    clang \
    clang-devel \
    llvm-devel \
    gcc \
    gcc-c++ \
    make \
    pkg-config \
    ca-certificates \
    curl \
 && dnf clean all

# Install a modern Rust toolchain (Cargo understands lockfile v4)
RUN curl https://sh.rustup.rs -sSf | sh -s -- -y
ENV PATH="/root/.cargo/bin:${PATH}"
