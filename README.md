# ZFORMULA — Impedance formula reference for TI-84 Plus CE

A menu-driven TI-BASIC cheat sheet: pick series or parallel, pick two of R / L / C, and the calculator shows the impedance formulas for that pair.

一个 TI-84 Plus CE 上的 TI-BASIC 公式速查程序:选择串联或并联,再从 R、L、C 中选两个,计算器就会显示这两个元件组合的阻抗公式。

---

## Features

- Six combinations: R–L, R–C, L–C, each in **series** and **parallel**
- For each one: `Z(s)`, `Z(jw)` (with s = jw), magnitude `|Z|`, phase `∠Z`
- Corner frequency `wc`, `fc` for RL / RC; resonance frequency `w0`, `f0` for LC
- `BACK` option at every level, `QUIT` on the first menu

## 功能

- 共 6 种组合:R–L、R–C、L–C 的**串联**和**并联**
- 每种组合显示:`Z(s)`、`Z(jw)`(令 s = jw)、幅值 `|Z|`、相位 `∠Z`
- RL / RC 显示转折频率 `wc`、`fc`;LC 显示谐振频率 `w0`、`f0`
- 每一级菜单都有 `BACK` 返回,第一级菜单有 `QUIT` 退出

---

## Install

1. Send `ZFORMULA.8xp` to the calculator with TI Connect CE (or paste `ZFORMULA.txt` into a new program in the TI Connect CE editor and send that).
2. `PRGM` → `ZFORMULA` → `ENTER`.

## 安装

1. 用 TI Connect CE 把 `ZFORMULA.8xp` 发送到计算器(或者把 `ZFORMULA.txt` 的内容粘贴到 TI Connect CE 编辑器里新建的程序中,再发送)。
2. 按 `PRGM` → 选 `ZFORMULA` → `ENTER`。

---

## Usage

1. Choose **SERIES** or **PARALLEL**.
2. Pick the first component (R / L / C).
3. Pick the second component from the remaining two.
4. Read the formulas, then press `ENTER` to return to the main menu.

## 使用方法

1. 选择 **SERIES**(串联)或 **PARALLEL**(并联)。
2. 选第一个元件(R / L / C)。
3. 从剩下的两个里选第二个元件。
4. 查看公式,按 `ENTER` 回到主菜单。

---

## Example: R ∥ L

```
R PARALLEL L
Z=R(sL)/(R+sL)
Z=sL/(1+sL/R)
s=jw:
Z=jwL/(1+jwL/R)
|Z|=wL/√(1+(wL/R)²)
∠Z=90°-tan⁻¹(wL/R)
wc=R/L
fc=R/(2πL)
```

## 示例:R ∥ L

屏幕显示内容如上。

---

## Notes

- `w` stands for ω — the calculator has no ω character.
- For pure L–C the phase is only ±90°; the screen notes on which side of the resonance frequency each sign applies.
- Ideal components. The program only uses the variable `S`.

## 注意事项

- `w` 代表 ω,因为计算器没有 ω 字符。
- 纯 L–C 电路的相位只有 ±90°,屏幕上会注明在谐振频率哪一侧取正、哪一侧取负。
- 按理想元件处理。程序只用到变量 `S`。

---

## Files / 文件说明

- `ZFORMULA.8xp` — program for the calculator / 可直接发送到计算器的程序
- `ZFORMULA.txt` — readable source / 可读的源码

## License / 许可证

MIT
