# Rescue Notice — 故事神谕 (Story Oracle)

> **This is an unofficial rescue mirror. It is not an official fork, not an official
> continuation, and not maintained by the original author.**
> **本仓库是非官方抢救镜像，不是官方分支、不是官方延续，也不由原作者维护。**

| | |
|---|---|
| Original author | `namelessone88` |
| Original repository | `https://github.com/namelessone88/story-oracle` — no longer available |
| Current repository | `https://github.com/BakaronLab/story-oracle-Fork` |
| Plugin version recovered | `1.84.0` (`manifest.json` version, matching `SO_VERSION` in `index.js`) |
| Rescue date | 2026-09-29 |
| License status | **UNCLEAR — see [License status](#license-status)** |

---

## English

### What this repository is

A preservation copy of the SillyTavern extension **Story Oracle** (故事神谕), recovered from
a local installation after the original GitHub repository and the original author's account
became unavailable (both return HTTP 404 as of 2026-09-29).

It exists for two reasons:

1. **Preservation** — to keep the source, its Git history, and its metadata from being lost.
2. **Temporary continuity** — so that existing users can still install and update the plugin.

### What this repository is not

- It is **not** an official fork, official continuation, or a new maintainer.
- It does **not** claim authorship of any original work.
- It does **not** relicense the project. No license file has been added, and none was present
  in the original.
- It is **not** endorsed by, affiliated with, or approved by the original author.

### Install

Install as a SillyTavern third-party extension:

- **Newer SillyTavern**: *Extensions* (🧩) → **Install extension** → paste the Git URL below.
- **Manual / older SillyTavern**: copy this folder into the third-party extensions directory
  (`SillyTavern/data/<user>/extensions/story-oracle/` on newer builds, or
  `SillyTavern/public/scripts/extensions/third-party/story-oracle/` on older ones).

Git URL:

```
https://github.com/BakaronLab/story-oracle-Fork
```

### Provenance

The source was a local installation created by SillyTavern's extension installer, i.e. a
**shallow clone (depth 1)** of the original repository.

| Item | Value |
|---|---|
| Recovered HEAD (original commit) | `8d311e9f4e8f5634af57687b85276901e0c30119` |
| Recovered HEAD tree | `170efb7ddd05547fdfb3efe77c0f897b65aba28f` |
| Original commit author | `namelessone88 <91587289+namelessone88@users.noreply.github.com>` |
| Original commit date | 2026-09-17 21:39:21 -0400 |
| Original commit subject | `Add files via upload` |
| Missing parent commit | `7715fe729e7591415536e02221b81d9aef89fc2f` (not on disk, upstream gone) |
| Published root commit | `95bf4cc0d30b8a97caa9f74402b4595b5f1bb071` |

**Why the published root commit has a different SHA.** The shallow clone did not contain the
original commit's parent, and Git rejects pushing a shallow history
(`shallow update not allowed`). The import commit was therefore re-rooted: the published commit
keeps the **identical tree**, **identical author**, **identical author date** and **identical
subject**; only the parent link and the GitHub web-flow signature differ. The commit's tree is the
original tree object `170efb7ddd05547fdfb3efe77c0f897b65aba28f`, so the imported content is
identical.

Canonical content checksums (SHA-256) of the recovered snapshot, taken from the original commit's
Git objects. All four files are stored with **LF** line endings, exactly as the author committed
them; a Windows checkout with `core.autocrlf=true` renders CRLF locally, which does not change
repository content. `README.md` has since had the rescue notice prepended, so its current
checksum differs (see [Changes](#changes)).

```
README.md     5182ee7c76f519292e6cdf28ba447eafcd3eca58eada55c71f0b863a2a97cf6f
index.js      fc7eea93c2475a7da82836bf49345f0f1fdcab82f90f3de06d793b1a0fe37d3e
manifest.json f10b309413d1104a517b504ce3172c3686f475eecc8b276e9d701fc083758b69
style.css     26c79699a27f33086e13e1351d94ea9889fca9ceca3753b5bd84c166f9d31295
```

### History recovery status

| | |
|---|---|
| History before 2026-09-17 | **NOT RECOVERED** |
| Reason | The only local copy was a shallow clone; the original repository and account are gone |
| Checked and unavailable in | Software Heritage archive, GitHub code/repository search, surviving community derivative repositories |

Community derivative projects (for example, a Vietnamese localisation and several *outline* /
*patch* variants) re-uploaded the source rather than forking it, so they carry no upstream
history. They were used only as corroboration that the recovered `style.css` matches the
project's published content.

Git history note: the original repository had at least one earlier commit (the missing parent),
whose content could not be recovered. Users should assume the recovered snapshot is the **last
version that was locally installed**, which is very likely but not provably the last version the
author ever published.

### Changes

Only these changes were made on top of the recovered snapshot:

| Commit | File(s) | Reason |
|---|---|---|
| `docs(rescue): document upstream repository recovery` | `README.md`, `RESCUE_NOTICE.md` | Mark the project as an unofficial rescue mirror and record provenance |
| `fix(rescue): repoint unavailable upstream update URL` | `index.js` | The built-in update check pointed at the now-unavailable upstream; repointed at this repository |

No other behaviour was changed. No version number was changed: the plugin remains `1.84.0`.
The original upstream URL is still named in the code comment next to the update sources.

### License status

**LICENSE_STATUS=UNCLEAR**

The recovered project contains **no license file** (`LICENSE`, `LICENSE.md`, `COPYING`) and no
license or copyright statement in `README.md`, `manifest.json`, `index.js` or `style.css`.
It carries no SPDX identifier and no terms of use.

What is known from the project's own documentation and from public community repositories:

- The author is on record granting **case-by-case** permission to at least one derivative
  project, together with a **non-commercial** restriction. That is a specific grant to a
  specific person, **not** a general redistribution license.
- The plugin exposes a documented Hook API intended for community derivative works, which shows
  a community-friendly stance but is not a licence grant.

Because no redistribution licence is established:

- **No licence file has been added** to this repository, and none should be added without the
  author's decision.
- Until the original author's permission is established, this repository is kept as a
  **preservation and continuity copy** rather than an authorised redistribution.
- Anyone who needs certainty about redistribution rights should seek the original author's
  permission.

### Privacy

This repository contains **only the plugin's own source and the original author's public Git
metadata**. It contains no API keys, tokens, cookies, passwords, chat logs, SillyTavern user
configuration, or user data. The extension stores endpoint credentials in the browser's local
storage and never shipped credentials in the source.

### Deference to the original upstream

If the original author restores the official project, or asks for this copy to be archived,
moved, or removed, this rescue repository should defer to the official upstream, subject to
applicable licence terms and to preservation needs.

---

## 中文

### 这是什么

这是 SillyTavern 扩展**故事神谕（Story Oracle）**的保存副本。原作者仓库与原作者账号均已无法
访问（截至 2026-09-29 均返回 HTTP 404），本副本是从**本地已安装的插件目录**抢救出来的。

存在的目的只有两个：

1. **保存**——让源码、Git 历史与项目元数据不至于失传。
2. **临时接续**——让既有用户仍能安装与更新这个插件。

### 这不是什么

- **不是**官方分支、**不是**官方延续，也**不代表**出现了新的维护者。
- **不主张**任何原创署名。
- **不重新授权**：仓库里**没有添加任何许可证文件**，原项目本身也从未附带过。
- **未经**原作者认可、授权或背书。

### 安装

按 SillyTavern 第三方扩展安装：

- **较新版酒馆**：*扩展*（🧩）→ **安装扩展** → 填入下面的 Git 地址。
- **手动 / 较旧版酒馆**：把本文件夹放进第三方扩展目录（较新版为
  `SillyTavern/data/<用户名>/extensions/story-oracle/`，较旧版为
  `SillyTavern/public/scripts/extensions/third-party/story-oracle/`）。

Git 地址：

```
https://github.com/BakaronLab/story-oracle-Fork
```

### 来源与取证

来源是酒馆扩展安装器创建的本地目录，即原仓库的**浅克隆（depth 1）**。

| 项目 | 值 |
|---|---|
| 抢救到的 HEAD（原提交） | `8d311e9f4e8f5634af57687b85276901e0c30119` |
| 该提交的 tree | `170efb7ddd05547fdfb3efe77c0f897b65aba28f` |
| 原提交作者 | `namelessone88 <91587289+namelessone88@users.noreply.github.com>` |
| 原提交时间 | 2026-09-17 21:39:21 -0400 |
| 原提交标题 | `Add files via upload` |
| 缺失的父提交 | `7715fe729e7591415536e02221b81d9aef89fc2f`（本地与线上均不存在） |
| 本仓库的根提交 | `95bf4cc0d30b8a97caa9f74402b4595b5f1bb071` |

**为什么发布出来的根提交 SHA 与原来不同。** 浅克隆里没有原提交的父提交，而 Git 拒绝推送浅
历史（`shallow update not allowed`）。因此导入提交被**重新扎根**：发布出来的提交保持**完全相同的
tree、相同的作者、相同的作者时间、相同的标题**，只有父链接与 GitHub 的 web-flow 签名不同。
导入提交的 tree 就是原 tree 对象 `170efb7ddd05547fdfb3efe77c0f897b65aba28f`，内容一致。

四个文件在 Git 中均为 **LF** 换行（与作者提交时一致）；Windows 上 `core.autocrlf=true` 的检出会
显示成 CRLF，这不会改变仓库内容。快照的 SHA-256（取自原提交的 Git 对象）见英文一节；
`README.md` 之后被加上了抢救声明，因此它现在的校验和已经不同（见「改动清单」）。

### 历史恢复状态

- **2026-09-17 之前的历史：未能恢复。**
- 原因：本地只有浅克隆，原仓库与账号都已消失。已尝试且当时无存档可取的渠道：Software
  Heritage 存档、GitHub 代码/仓库搜索、网上现存的二创/衍生仓库。
- 网上的社区二创（例如越南语化版本、若干「大纲版 / patch」变体）是**重新上传**而非 fork，
  因此不含上游历史；它们只被用来交叉验证抢救出的 `style.css` 与项目公开内容一致。
- 原仓库至少还有一个更早的提交（父提交），其内容无法取回。用户可以认为：抢救到的是
  **本地最后安装过的版本**——这极可能、但无法证明就是作者发布过的最后一个版本。

### 改动清单

在抢救快照之上只做了这两处改动：

| 提交 | 文件 | 原因 |
|---|---|---|
| `docs(rescue): document upstream repository recovery` | `README.md`、`RESCUE_NOTICE.md` | 标注为非官方抢救镜像并记录来源 |
| `fix(rescue): repoint unavailable upstream update URL` | `index.js` | 内置更新检查指向已失效的原仓库，改为指向本仓库 |

没有其它行为改动，**版本号未改**（仍为 `1.84.0`）。更新地址旁的代码注释里仍然写明原 upstream。

### 许可证状态

**LICENSE_STATUS=UNCLEAR（未确认）**

抢救到的项目**没有任何许可证文件**（`LICENSE`、`LICENSE.md`、`COPYING`），`README.md`、
`manifest.json`、`index.js`、`style.css` 里也**没有任何版权或许可声明**，没有 SPDX 标识、
没有使用条款。

目前已知的旁证：

- 作者曾**逐案**授权至少一个二创项目，并附带**禁止商业化**的要求。那是对特定个人的特定授权，
  **不是**面向公众的再分发许可。
- 插件公开了面向二创的 Hook API，态度友好，但这不构成许可授权。

因为再分发许可并不成立：

- 本仓库**没有添加任何许可证文件**，也不应在未经作者决定的情况下添加。
- 在获得原作者授权之前，本仓库按**保存与接续副本**对待，而不是「已授权的再分发」。
- 需要明确权利的人，请向原作者取得许可。

### 隐私

本仓库只包含**插件自身源码**与**原作者的公开 Git 元数据**：不含任何 API Key、token、cookie、
密码、聊天记录、酒馆用户配置或其它用户数据。插件把端点凭据保存在浏览器本地存储里，源码中
从未包含过凭据。

### 让位于官方上游

如果原作者恢复官方项目，或要求归档、迁移、下架本副本，本抢救仓库应让位于官方上游——具体以
适用许可条款与保存需要为准。
