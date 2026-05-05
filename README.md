# Remember Now Model Artifacts

This repository hosts approved local AI model artifacts for Remember Now as GitHub Release assets.

The model files are downloaded by the Remember Now app, verified by exact byte size and SHA256 fingerprint, stored on the user's device, and then used locally by the app's on-device runtime.

## What this repository is for

- Hosting approved GGUF model files as release assets.
- Providing stable public HTTPS download URLs for the Remember Now app.
- Keeping model artifacts separate from the private app code repository.
- Preserving clear attribution and license notes for downloadable model artifacts.

## What this repository is not for

- It does not contain Remember Now app code.
- It does not receive reminder text or user data.
- It does not run AI inference.
- It does not contain private user information.
- It does not use Git LFS.

## Current model artifact

```txt
Model: Qwen2.5 0.5B Instruct
Format: GGUF
Quantization: Q4_K_M
Runtime target: llama.cpp
Source: Qwen/Qwen2.5-0.5B-Instruct-GGUF
License: Apache-2.0
Filename: qwen2.5-0.5b-instruct-q4_k_m.gguf
Expected bytes: 491400032
Expected SHA256: 74a4da8c9fdbcd15bd1f6d01d621410d31c6fc00986f5eb687824e7b93d7a9db
```

## Verification policy

Every release asset used by Remember Now must be verified before the app catalog points to it.

Required verification:

```txt
1. Download the release asset URL twice.
2. Confirm both downloads have the same exact byte count.
3. Confirm both downloads have the same exact SHA256.
4. Confirm both files are byte-identical with cmp.
5. Record the final URL, exact bytes, and exact SHA256 in the Remember Now app repository approval record.
```

The Remember Now app must reject downloaded model files that do not match the approved byte size and SHA256.

## Privacy note

Model files are public downloadable artifacts.

Reminder content, user data, voice input, imported task content, and local AI prompts are not sent to this repository.

The model runs on the user's device after download and verification.
