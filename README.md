# 第二届“湾区杯”网络安全大赛初赛

题目附件前往 [Releases](https://github.com/CTF-Archives/2026-WQB-Quals/releases) 下载

## Crypto

### Cold Forge

> 取证人员从 Cold Forge 的审批节点提取到 `frost_telemetry.json` 与 `sealed_release.json`。恢复正确的阈值私钥并重建发布签名，才能打开该发布包。
> [附件下载](https://github.com/CTF-Archives/2026-WQB-Quals/releases/download/attachments/cold_forge_4b1bc2963947358f4ce48f769581a096.zip)

### TinyNTRU

> A developer implemented a tiny NTRU-like encryption scheme and believed that hiding the private key was enough.
> You are given the source code, the public key and the ciphertext.
> Analyze the parameters, recover the private polynomial and decrypt the flag.
> [附件下载](https://github.com/CTF-Archives/2026-WQB-Quals/releases/download/attachments/TinyNTRU_90da8eacc643a00f6326db3c51039c9e.zip)

### Invalid Echo

> Broken ECDH is still ECDH, right?
> We wrote a tiny elliptic-curve key exchange service. The private key was never printed, and only encrypted oracle responses were recorded.
> You are given the source code and a limited ECDH oracle. Can you recover the server private key and decrypt the flag?
> [附件下载](https://github.com/CTF-Archives/2026-WQB-Quals/releases/download/attachments/InvalidEcho_df98b0a278ffb45541ef8000510dfe53.zip)

环境题，无附件

### mosaic_0rtt_context_collapse

> 附件是一次实验室 mTLS TLS 1.3 握手的事故证据、一个被清零 PSK 的真实 `SSL_SESSION`、另一组完整握手与恢复握手的 binder 校验材料，以及两个普通 OpenSSL 诊断程序。在线服务监听 TCP/9999。
> 请分析 TLS 记录与会话恢复材料，恢复实验室 ticket 的 resumption PSK；随后完成实验室 0-RTT 预检和发布入口确认，取得发布内容。
> [附件下载](https://github.com/CTF-Archives/2026-WQB-Quals/releases/download/attachments/mosaic_0rtt_a57f38959150911c3bfe645d288aaa62.zip)

环境题，无附件

### SlashKEM

> A simplified ML-KEM-like decapsulation implementation was tested on a leaky device.
> The developers claim that no secret key is ever printed, and only public parameters,
> ciphertext samples, power traces and timing samples are released.
> Recover the secret polynomial and decrypt the flag.
> [附件下载](https://github.com/CTF-Archives/2026-WQB-Quals/releases/download/attachments/SlashKEM_d76ffb0d4a434fdec7ef43cc6464f949.zip)


## Misc

### 签到题

> 关注微信公众号“广东省计算机信息网络安全协会”，发送“签到”获取flag字符串。

### SilentConfig

> 安全团队在巡检中发现数据库出现异常查询行为，但线上日志只保留了部分片段。
> 攻击者可能通过 Web 接口读取了某个敏感业务配置。请关联分析附件中的日志，恢复攻击者最终获得的配置值。
> Flag 格式：flag{uuid}
> [附件下载](https://github.com/CTF-Archives/2026-WQB-Quals/releases/download/attachments/silentconfig_3f728698ddce0220f6acd7484e58aece.tar.gz)

### whoami？

> [附件下载](https://github.com/CTF-Archives/2026-WQB-Quals/releases/download/attachments/whoami_7444f331092f76997e2a8944fb2ab8bf.zip)

### 不可信机器

> 某企业服务器数据库被下发勒索信息，并且该服务器疑似被控制，已不可信。现将原服务器硬盘克隆后提供登录访问，选手需在环境内自行搜集线索，固定证据。
> 接入方式示例：
>
> 1) 使用 nc 连接比赛平台分配的目标地址与端口
> 2) 环境启动期间可能出现等待提示，待系统就绪后进入终端
> 3) 在终端内完成相关取证分析
>   请通过证据分析还原攻击链，并按如下格式提交 flag：
>   flag{攻击者IP_释放的第一个恶意文件名_通信salt_网站管理员登录密码hash后6位_攻击者删除的程序名}
>   示例格式（非答案）：
>   flag{1.1.1.1_a.out_abc123_xxxxxx_test}

环境题，无附件

### FractalTrace

> 我们在一次科研数据泄露排查中截获了一张异常实验图像。
> 图像本身看起来正常，但安全团队认为它的像素结构可能被人为处理过。请分析附件，恢复其中隐藏的安全标识。
> [附件下载](https://github.com/CTF-Archives/2026-WQB-Quals/releases/download/attachments/FractalTrace_eaf931e57f5f428d8afa4a57706def67.zip)

### committed

> An internal audit server experienced an abnormal interruption. After the service restarted, investigators discovered that a critical audit record was missing from the audit database.
> Recover the last successfully committed EXPORT operation before 2026-07-18 03:14:00.
> Flag format:flag{actor-action-nonce}，Use lowercase characters.
> [附件下载](https://github.com/CTF-Archives/2026-WQB-Quals/releases/download/attachments/committed_4d17ed71c21733d1f3e6cf3e4421bd95.7z)

### SilentWeights

> Silent Weights 是一起 AI 模型泄露事件的调查样本。
> 某企业安全团队发现，一份内部视觉识别模型的训练结果被上传到了外部网盘。模型所有者确认，本次训练任务没有使用额外适配组件，但泄露文件的体积和训练日志均存在异常。
> 请分析附件中的模型文件和辅助材料，恢复被隐藏的内部资料，并提交最终 flag。
> [附件下载](https://github.com/CTF-Archives/2026-WQB-Quals/releases/download/attachments/SilentWeights_367c1179ccb1339df487d17c0e7242bf.zip)


## PWN

### logd

> [附件下载](https://github.com/CTF-Archives/2026-WQB-Quals/releases/download/attachments/logd_315a6a597e577dbf814caa4a1339dd6f.zip)

环境题

### knote

> [附件下载](https://github.com/CTF-Archives/2026-WQB-Quals/releases/download/attachments/knote_2cf788f32e8f8380bd5097daa717c6f8.zip)

环境题

### gatewayd

> [附件下载](https://github.com/CTF-Archives/2026-WQB-Quals/releases/download/attachments/gatewayd_46f93270f1efcf5ff9710de9d0b8a33c.zip)

环境题

### VaultKeeper

> [附件下载](https://github.com/CTF-Archives/2026-WQB-Quals/releases/download/attachments/VaultKeeper_217f027215c23e54128fcf56b1941a9f.zip)

环境题

### JIT_Sandbox

> 欢迎来到JIT沙盒，你能读取秘密吗？
> [附件下载](https://github.com/CTF-Archives/2026-WQB-Quals/releases/download/attachments/JIT_Sandbox_c76f88b92a71711dd2c2432a9058e7cc.zip)

环境题

### ArchiveFS

> ArchiveFS 是一个轻量级云端文档归档系统。
> 被删除的文档会进入回收站，系统仍会保留最近一次预览缓存，方便用户快速恢复。为了兼容旧版本草稿，开发者还保留了历史草稿修订功能。
> [附件下载](https://github.com/CTF-Archives/2026-WQB-Quals/releases/download/attachments/ArchiveFS_45a760d5f19126b0ee4c54bcbcec78a5.zip)

环境题


## Reverse

### attestjit

> 工业边缘控制面的远程证明验证器在一次崩溃后，只留下了 stripped ELF 验证器、裁剪 ELF Core、COSE_Sign1 证明、请求样本和受保护的发布材料。
> [附件下载](https://github.com/CTF-Archives/2026-WQB-Quals/releases/download/attachments/attestjit_7d6a92e1bbb0c107949c8e209e9fbb69.zip)

### Pixel Oracle

> The flag is not stored as a plaintext string. The verifier checks the move route length, board boundary rules, FNV-1a path hash, score replay, a native gate, and a xorshift32-based encrypted byte array. A simple string search or hardcoded comparison is not enough to solve the challenge.
> [附件下载](https://github.com/CTF-Archives/2026-WQB-Quals/releases/download/attachments/pixel_oracle_478c8182a453fb9562aee4c8238b2662.zip)

### meshgate

> MeshGate 是一个使用 XDP/eBPF 策略的边缘 service-mesh 网关。节点更换后，现场保留了 eBPF 对象、BTF 类型信息、map 快照、loader 状态和历史网络流量。
> [附件下载](https://github.com/CTF-Archives/2026-WQB-Quals/releases/download/attachments/meshgate_fc549d0d36fc289e8079e7424c41d9bb.zip)

### Rift Runner

> The challenge is not a plaintext-string search. The route must reach the goal, collect shards 1-4 in order, satisfy the energy constraint, pass anti-debug telemetry, match route hash and score constants, and pass a native gate from lib/x86/librtrack.so or lib/x86_64/librtrack.so. Only then will the final encrypted flag byte array be checked with a xorshift128 stream.
> [附件下载](https://github.com/CTF-Archives/2026-WQB-Quals/releases/download/attachments/rift_runner_627376ca5ab80d373aedff05c9c83c11.zip)

### passkey_vault

> 某企业在 passkey 迁移事故后留下了虚拟认证器、resident credential vault、浏览器侧 CTAP 探测记录和平台加密恢复数据。
> [附件下载](https://github.com/CTF-Archives/2026-WQB-Quals/releases/download/attachments/passkey_vault_017f4ce57bd5eb2faa2e888aab930e35.zip)
> 提示：
> `release_blob.bin` 是 `PVREL3` AES-256-GCM 密文，格式为 `magic(8)||nonce(12)||明文长度(LE32)||ciphertext||tag`，并令 `auth_base = target_assertion.authenticatorData[:37]`。
> `binding=SHA256("PVREL3"||auth_base||clientDataHash||credential_id)`，`key=HKDF-SHA256(salt=binding, ikm=prf_result, info="PasskeyVault/CTAP/PRF/release-v3", L=32)`，`nonce=SHA256("PVREL3/nonc"||auth_base||prf_result)[:12]`，`aad="PVREL3"||target_user_id||credential_id||clientDataHash`。
> 使用上述 `key`、派生 `nonce`、`aad` 和末尾 GCM tag 解密即可得到 flag；所有字符串均按对应字节拼接。


## Web

### ThemeForge

> ThemeForge 允许设计师通过点路径即时调整个人主题。
> 核心身份字段已经加锁，但管理员的隐藏色仍然有可能被普通设计师看到。
> 找到权限边界中的裂缝，打开 Admin Color Vault。
> [附件下载](https://github.com/CTF-Archives/2026-WQB-Quals/releases/download/attachments/ThemeForge_b6ff996302ecbe6054459caf1b3d331a.zip)

环境题

### SchemaStudio

> 目录团队正在试用新的扩展字段设计流程。
> （本题下发后，请通过http访问相应的ip和port，例如 nc ip port ，改为http://ip:port/）
> [附件下载](https://github.com/CTF-Archives/2026-WQB-Quals/releases/download/attachments/SchemaStudio_b1174301f2cd8567163103f2554180fd.zip)

环境题

### DockRelay

> DockRelay 只允许诊断 approved partner host，但安全团队怀疑校验器和实际 HTTP
> 客户端对同一 URL 的解释不同。审计随题源码，访问队内构建平面，创建符合实验策略的
> 特权容器，并从隔离构建宿主恢复本队 Flag。
> [附件下载](https://github.com/CTF-Archives/2026-WQB-Quals/releases/download/attachments/DockRelay_820132177aaee605dedf7c8129e35acf.zip)

环境题

### one-click-to-build

> Nimbus 是一套新上线的内容管理控制台，运维同学坚信"用了 Go 重写就不会再有 PHP 时代的那些漏洞"。
> 站点开放了游客上报链接的功能，管理员会定时审阅上报的链接。
> 请审计附件源码，找出从访客到服务器控制权的完整路径，取得 /flag 的内容。
> [附件下载](https://github.com/CTF-Archives/2026-WQB-Quals/releases/download/attachments/one-click-to-build_f5b4b956f46656f563e134d3cfe47e06.zip)

环境题

### hanziguard

> 某企业上线了一套新的协同办公平台 CorpFlow OA，支持登录、留言、公告、通讯录、附件与旧系统数据迁移功能，并区分了普通员工与管理员权限。安全团队声称已为 JSON 解析加上了严密的关键词黑名单与 gadget 类黑名单，敏感的数据迁移功能只有管理员才能触达。你作为渗透测试工程师拿到了该系统的访问地址和一个自助注册入口，请深入审计，找到其中隐藏的秘密。
> [附件下载](https://github.com/CTF-Archives/2026-WQB-Quals/releases/download/attachments/hanziguard_6a0e2aae7aa0b08bd1ae5f2c511c437d.zip)

环境题

### 不会建模？让 AI 来

> 无描述

环境题，无附件

### FlowRoot

> FlowRoot 的流程校验服务似乎不只会“校验”代码。
> 完成审计，读取根目录中的 Flag。

环境题，无附件

### ShadowArchive

> Shadow Archive 是一个内部工作区配置归档系统。
> 普通用户可以维护自己的工作区配置并导出归档，管理员可以恢复旧版本归档。
> 系统没有提供 pickle 上传功能，危险关键字也会被过滤。
> 请审计源码，利用业务流程中的漏洞读取服务器端 flag。
> [附件下载](https://github.com/CTF-Archives/2026-WQB-Quals/releases/download/attachments/ShadowArchive_22b5ef049c3cc994a91218701e98a72d.zip)

环境题

### CloudGate

> CloudGate 是一套企业内部云权限管理平台。
> 你获得了 demo workspace 的访问入口。管理员后台使用签名 JWT 认证，并额外检查安全审批会话。
> 请通过平台自身的业务流程进入管理员后台，找到隐藏的 flag。

环境题，无附件

### Ez_web

> 为啥出题人都喜欢题目名称写EASY啊，明明一点都不EASY啊

环境题，无附件
