# 🧪 Soundness Testnet Registration Guide

## 🌐 Official Website

🔗 [https://soundness.xyz/](https://soundness.xyz/)

➡️ **Step 0:** Submit your email on the website to get started.

---

## ✅ Step 1: Install Dependencies & Generate Your Key

### 🔧 System Update

```bash
sudo apt update && sudo apt upgrade -y
```

### ⚙️ Install Soundness CLI Installer

```bash
curl -sSL https://raw.githubusercontent.com/WibuCryptoPY/Soundness-Cli/refs/heads/master/install.sh | bash
```

### 🦀 Install Rust

```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs/ | sh
```

Nhập `1` rồi nhấn **Enter** nếu được nhắc.

### 🔄 Load Environment (for Bash)

```bash
source ~/.bashrc
```

### 🔧 Install & Update Soundness CLI

```bash
soundnessup install
soundnessup update
```

### 🔑 Generate Key

```bash
soundness-cli generate-key --name my-key
```

Lưu lại**public key** và **mnemonic phrase** 

### 🔍 Check Key & Seedphrase

```bash
soundness-cli list-keys
```

---

## 🎮 Step 2: Play the Game

1. Mở **Discord Soundness**: [https://discord.gg/soundnesslabs](https://discord.gg/soundnesslabs)
2. Truy cập kênh `#game-arena`
3. Nhập một trong các lệnh trò chơi như sau:

   ```
   /8queens
   /tictactoe
   ```

76 / 5.000
4. Chơi cho đến khi **thắng**
5. Bạn sẽ nhận được **bằng chứng** dưới dạng:

   * File proof (proof file)
   * Or **Walrus Blob ID**

---

## 🚀 Step 3: Submit Your Proof to Soundness

Sử dụng lệnh này để gửi:

```bash
soundness-cli send \
--proof-file <your-proof-blob-id> \
--game <game-name> \
--key-name <your-key-name> \
--proving-system ligetron \
--payload '<json-payload>'
```

### 📝 Giải thích:

* `--proof-file`: ID của bằng chứng hoặc đường dẫn đến tệp bằng chứng của bạn
* `--game`: Tên của trò chơi (ví dụ: `8queens` hoặc `tictactoe`)
* `--key-name`: Tên của khóa bạn đã tạo
* `--proving-system`: Sử dụng `ligetron` cho trò chơi hiện tại
* `--payload`: Chuỗi JSON chứa dữ liệu bằng chứng của trò chơi (thu được khi thắng)
---

## 🧰 Bổ Sung: Gửi Proof bằng Nhiều Cách Khác Nhau

### 1. 🔄 Gửi Proof từ Tệp Cục Bộ

```bash
soundness-cli send --proof-file path/to/proof.proof --elf-file path/to/program.elf --key-name my-key
```

### 2. ☁️ Gửi Proof từ Walrus Storage

```bash
soundness-cli send --proof-file <proof-walrus-blob-id> --elf-file <elf-walrus-blob-id> --key-name my-key
```

### 3. 🔀 Kết Hợp Giữa File Cục Bộ & Walrus Blob

```bash
# Proof từ file cục bộ, ELF từ Walrus
soundness-cli send --proof-file path/to/proof.proof --elf-file <walrus-blob-id> --key-name my-key

# Proof từ Walrus, ELF từ file cục bộ
soundness-cli send --proof-file <walrus-blob-id> --elf-file path/to/program.elf --key-name my-key
```

### 4. 🧠 Thay Đổi Hệ Thống Proving (Tuỳ Chọn)

```bash
soundness-cli send \
--proof-file <path-or-blob-id> \
--elf-file <path-or-blob-id> \
--key-name my-key \
--proving-system <sp1 | ligetron | risc0>
```

> ✅ Các hệ thống proving hiện có: `sp1`, `ligetron`, `risc0`
> Mọi yêu cầu sẽ được ký bằng key pair bạn đã tạo.

---

## 📌 Bước Cuối Cùng

* 💾 Lưu lại **seed phrase** và **public key** của bạn một cách an toàn!
* 💬 Tham gia Discord: [https://discord.gg/soundnesslabs](https://discord.gg/soundnesslabs)
* 🚀 Truy cập cockpit tại kênh 🐬│soundness-cockpit, sau đó dùng lệnh:

  ```
  /access
  ```

  để gửi **public key** của bạn.

✅ **Hoàn tất! Bạn đã sẵn sàng khám phá testnet của Soundness.**

---

## 📚 Tài Liệu Tham Khảo

📄 [Tweet Thông Báo Chính Thức](https://x.com/SoundnessLabs/status/1902389758527152586)

---
