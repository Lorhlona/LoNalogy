---
marp: true
theme: default
paginate: true
math: katex
---

# LoNalogy 統一草案（全面改稿版）
## LCMS基礎 + 有効理論 + 分野展開

- 目的: `i`（回転）と `j`（分離）を同格に扱う
- 方針: 基礎理論と有効理論を明確に分離

---

## 0. まず結論

- `i` は位相回転の軸
- `j` は可視/不可視分離の軸
- 実際のセクター移送は `j` 単独ではなく結合項で起こる
- 基礎方程式は LCMS、CGL は粗視化有効方程式

---

## 1. 記号の固定（衝突回避）

- `Xi(x,t)`: セクター分裂係数（`sigma_3` 前）
- `Gamma(x,t)`: セクター混合係数（`sigma_1` 前）
- `Ycal(s)`: 境界アドミタンス演算子
- `Omega_Lambda`: 宇宙定数密度パラメータ

---

## 2. 内部演算子の定義（固定）

$$
i^2=-1,\quad j:=\sigma_3,\quad j^2=I
$$

$$
P_\pm=\frac{I\pm j}{2},\quad
P_\pm^2=P_\pm,\quad
P_+P_-=0,\quad
P_++P_-=I
$$

- 本稿では `j` を「数」ではなく内部2次元空間上の作用素として固定する
- `e_\pm` 記法は直観用の略記とし、厳密式は `P_\pm` で書く

---

## 3. 状態の分解

$$
\psi=P_+\psi+P_-\psi,\quad
\psi_\pm:=P_\pm\psi
$$

二重項表示:

$$
\psi=
\begin{bmatrix}
\psi_+\\
\psi_-
\end{bmatrix}
$$

---

## 4. 双ボルン則と観測写像

$$
p_\pm=\mathrm{Tr}(P_\pm\rho),\quad \rho=|\psi\rangle\langle\psi|
$$

可視射影:

$$
p_{\mathrm{vis}}:=p_+=\mathrm{Tr}(P_+\rho),\quad
p_++p_-=1
$$

---

## 5. LCMS（基礎理論）: 非相対論形

$$
i\hbar\partial_t\psi=
\left[\hat H_0 I+\hbar \Gamma\sigma_1+\hbar \Xi\sigma_3\right]\psi
$$

$$
\hat H_0=
-\frac{\hbar^2}{2m}\left(\nabla-\frac{i q}{\hbar}\mathbf A\right)^2+V
$$

---

## 6. LCMSの数学要件

$$
\mathcal H=L^2(\Omega)\otimes\mathbb C^2,\quad \psi(t)\in D(\hat H)
$$

$$
\hat H=\hat H^\dagger
\Longrightarrow
\psi(t)=e^{-i\hat H t/\hbar}\psi(0)
$$

$$
\|\psi(t)\|^2=\|\psi(0)\|^2
$$

---

## 7. `j` の本質（数理）

- `j=\sigma_3` は `Z_2` 分解の生成子
- `j` は回転ではなく双曲的分離の軸
- `sigma_3` 項（`Xi`）はセクター非対称を定義
- `sigma_1` 項（`Gamma`）がセクターを混ぜる

---

## 8. 連続方程式（厳密）

LCMS から厳密に:

$$
\partial_t p_+ + \nabla\cdot J_+
=
2\Gamma\,\mathrm{Im}(\psi_+^\ast\psi_-)
$$

$$
\partial_t p_- + \nabla\cdot J_-
=
-2\Gamma\,\mathrm{Im}(\psi_+^\ast\psi_-)
$$

---

## 9. 総量保存（厳密）

$$
\partial_t(p_+ + p_-) + \nabla\cdot(J_+ + J_-) = 0
$$

重要:
- 右辺は一般に `p_- - p_+` ではない
- コヒーレンス `Im(psi_+^* psi_-)` が本体

---

## 10. 粗視化有効式（近似）

デコヒーレンス + 時間スケール分離で近似:

$$
\partial_t p_+ + \nabla\cdot J_+ = \Gamma(p_- - p_+)
$$

$$
\partial_t p_- + \nabla\cdot J_- = \Gamma(p_+ - p_-)
$$

---

## 11. CGLの位置づけ

有効方程式（開放系）:

$$
\partial_t\Psi=(\alpha+i\omega+j\kappa+ij\lambda)\Psi
+B\nabla^2\Psi + C|\Psi|^2\Psi
$$

- これは基礎方程式ではなく粗視化表現
- `kappa` は主に対角成長差（分離バイアス）

---

## 12. 分解で見えること

$$
\partial_t\psi_\pm=
\bigl[(\alpha\pm\kappa)+i(\omega\pm\lambda)\bigr]\psi_\pm
+B_\pm\nabla^2\psi_\pm + C_\pm|\psi_\pm|^2\psi_\pm
$$

修正点:
- `kappa` 単独では移送を作らない
- 移送は off-diagonal 結合起源

---

## 13. 標準量子の回収

条件:
1. `Gamma=0`
2. `psi_-(t0)=0`
3. `H0` Hermitian

すると:

$$
i\hbar\partial_t\psi_+=\hat H_0\psi_+,\quad
p=|\psi_+|^2
$$

---

## 14. 測定理論としての厳密化

可視観測は CP 写像（一般には非TP）で定義:

$$
\mathcal E_+(\rho)=P_+\rho P_+
$$

$$
p_{\mathrm{vis}}=\mathrm{Tr}\,\mathcal E_+(\rho)=\mathrm{Tr}(P_+\rho)\le 1
$$

$$
\rho_+^{\mathrm{norm}}=\frac{\mathcal E_+(\rho)}{p_{\mathrm{vis}}}
$$

- 全計測器は `\sum_k \mathcal E_k` が CPTP、可視チャネル `\mathcal E_+` は一般に非TP

---

## 15. 古典力学への接続

$$
\psi_\pm=\sqrt{\rho_\pm}e^{iS_\pm/\hbar}
$$

$$
\hbar\to 0:\ 
\partial_t S_\pm + H(x,\nabla S_\pm,t)=0
$$

- WKB/Hamilton-Jacobi 極限で整合
- `Gamma` は占有再配分として現れる

---

## 16. 熱力学・統計（最小）

空間無視の交換系:

$$
\dot p_+ = \Gamma(p_- - p_+),\quad
\dot p_- = \Gamma(p_+ - p_-)
$$

$$
S=-(p_+\ln p_+ + p_-\ln p_-),\quad \dot S\ge 0
$$

---

## 17. 熱力学の数学条件

- 2状態マルコフ過程（Metzler, 行和0）
- 定常分布 `pi` に対して

$$
D_{\mathrm{KL}}(p\Vert \pi)\ \text{単調減少}
$$

- 詳細釣り合い条件を満たす設計が可能

---

## 18. 電磁気との接続

最小結合:

$$
\nabla\to\nabla-\frac{i}{\hbar}Q\mathbf A,\quad
\partial_t\to\partial_t+\frac{i}{\hbar}Q\phi,\quad
Q=\begin{bmatrix}q_+&0\\0&q_-\end{bmatrix}
$$

- ただし `Gamma sigma_1` 混合と同時に使う場合はゲージ整合条件が必要

---

## 19. 電磁気の設計分岐

直接混合

$$
H_{\mathrm{mix}}=\hbar\Gamma\sigma_1
$$

を採ると、`[Q,\sigma_1]\neq 0` なら U(1) が壊れる。

$$
[Q,\sigma_1]=i(q_+-q_-)\sigma_2
$$

したがって基礎理論での整合条件は次のいずれか:
1. `q_+=q_-`（同電荷で直接混合）
2. 混合を媒介場で実装（下式）
3. `q_-\approx 0` は有効理論近似として扱う

閉体系基本条件:

$$
\partial_\mu J^\mu_{\mathrm{tot}}=0
$$

---

## 20. 相対論版 LCMS

$$
\left(i\hbar c\,\gamma^\mu D_\mu-mc^2\right)\psi
-\hbar c\,\Gamma(\Theta)\sigma_1\psi
-\hbar c\,(\partial_\mu\Theta)\gamma^\mu\sigma_3\psi=0
$$

$$
D_\mu=\partial_\mu+\frac{i}{\hbar}q A_\mu
$$

- 上式は `q_+=q_-=q` を採る基礎形
- 異電荷混合は媒介場実装へ分離する

---

## 21. 相対論の作用原理

$$
\mathcal L=
\bar\psi(i\hbar c\gamma^\mu D_\mu-mc^2)\psi
-\hbar c\,\Gamma\,\bar\psi\sigma_1\psi
-\hbar c\,(\partial_\mu\Theta)\bar\psi\gamma^\mu\sigma_3\psi
+\frac{f^2}{2}\partial_\mu\Theta\partial^\mu\Theta-U(\Theta)
$$

異電荷混合の代表:

$$
\mathcal L_{\mathrm{mix}}=y\,S\,\bar\psi_+\psi_-+\mathrm{h.c.},\quad
q_S=q_+-q_-
$$

---

## 22. 相対論での実務条件

- Lorentz 共変
- 因果性
- 有効化時の完全正値（GKSL）
- 局所性条件（超光速信号回避）

---

## 23. 宇宙論（背景）

$$
3M_{\mathrm{Pl}}^2H^2=
\rho_r+\rho_\Lambda+\rho_+ + \rho_- + \rho_\Theta
$$

$$
\dot\rho_+ + 3H(1+w_+)\rho_+ = +Q,\quad
\dot\rho_- + 3H(1+w_-)\rho_- = -Q
$$

---

## 24. 宇宙論（共変保存）

$$
\nabla_\mu T^{\mu\nu}_{(+)}=Q^\nu,\quad
\nabla_\mu T^{\mu\nu}_{(-)}=-Q^\nu
$$

$$
\nabla_\mu(T^{\mu\nu}_{(+)}+T^{\mu\nu}_{(-)})=0
$$

FRW では通常 `Q^\nu = Q u^\nu` を採用。

---

## 25. 宇宙論（摂動）

最小拡張:

$$
\dot\delta_i+(1+w_i)(\theta_i-3\dot\Phi)
+3H(c_{s,i}^2-w_i)\delta_i
=
\frac{\delta Q_i}{\rho_i}-\frac{Q_i}{\rho_i}\delta_i
$$

`H(z)` と `f\sigma_8` 同時適合には `Q` と `delta Q` の整合実装が必須。

---

## 26. 素粒子論（最小）

$$
\mathcal L=
\mathcal L_{\mathrm{SM}}
+\bar\psi(i\gamma^\mu\partial_\mu-M)\psi
-\Gamma\,\bar\psi\sigma_1\psi
+\mathcal L_{\mathrm{portal}}^{\mathrm{baseline}}
$$

---

## 27. 素粒子論（ベースライン固定）

自由度過多を避けるため、まず1本に固定:

$$
\mathcal L_{\mathrm{portal}}^{\mathrm{baseline}}
=
\lambda_{HS}|H|^2|S|^2
$$

拡張（別解析）:
- kinetic mixing
- neutrino portal

---

## 28. 素粒子論（制約）

- anomaly cancellation（ベクトルライク配置）
- collider / direct / indirect constraints
- 暗黒安定性（対称性 or 凍結機構）

---

## 29. 弦理論接続（条件付き）

$$
N_{\mathrm{gen}}=|I_{ab}|,\quad
I_{ab}=\prod_i(n_a^i m_b^i-m_a^i n_b^i)
$$

$$
\sum_x x_xN_xB_x^I=0\ (\forall I)
$$

---

## 30. 弦理論接続（整合制約）

$$
\sum_a N_a([\Pi_a]+[\Pi_{a'}])-4[\Pi_{O6}]=0
$$

$$
\sum_a N_a[\Pi_a]\cdot[\Pi_{\mathrm{probe}}]\equiv 0\pmod 2
$$

---

## 31. 弦理論主張のスコープ

- 一般定理を主張しない
- 特定コンパクト化クラスでの実現可能性を主張
- 「3世代必然化」は条件付き命題として扱う

---

## 32. 逆問題・境界理論

$$
I(s)=\mathcal Y(s)V(s)+I_0(s)
$$

$$
Z_{\mathrm{th}}(s)=\mathcal Y(s)^{-1},\quad
V_{\mathrm{th}}(s)=\mathcal Y(s)^{-1}I_0(s)
$$

---

## 33. 二層境界演算子

$$
\begin{bmatrix}I_+\\I_-\end{bmatrix}
=
\begin{bmatrix}
\mathcal Y_{++} & \mathcal Y_{+-}\\
\mathcal Y_{-+} & \mathcal Y_{--}
\end{bmatrix}
\begin{bmatrix}V_+\\V_-\end{bmatrix}
+
\begin{bmatrix}I_{0+}\\I_{0-}\end{bmatrix}
$$

---

## 34. 可視有効応答

$$
\mathcal Y_{\mathrm{eff}}
=
\mathcal Y_{++}
-\mathcal Y_{+-}\mathcal Y_{--}^{-1}\mathcal Y_{-+}
$$

- 不可視情報は可視応答へ混入
- 逆散乱で推定可能

---

## 35. 逆問題の数学条件

- 正実性（受動性）
- 解析性（因果性, Kramers-Kronig）
- 一意性・安定性（測定配置依存）

---

## 36. どこまで確立したか

確立寄り:
- 二重項 + 射影 + 交換の骨格
- LCMS（基礎）/ CGL（有効）の分離
- 分野展開テンプレの統一

---

## 37. 未完の核心

1. `Q, delta Q` を含む宇宙論同時フィット  
2. 3世代必然化の完全証明（`g=1,2` 排除）  
3. 境界逆問題の実験プロトタイプ

---

## 38. 分野展開テンプレ（実装規約）

1. 状態空間  
2. 閉体系力学  
3. 観測写像  
4. 有効化（必要時）  
5. 検証量

この順で書けば、分野間で式の互換性を維持できる。

---

## 39. 研究計画

Phase A: 厳密化（well-posedness, 近似条件）  
Phase B: 分野別拘束（宇宙論, QFT, 逆問題）  
Phase C: 外挿予言で検証

---

## 40. 抽象 Thevenin 定理（演算子版）

境界状態空間を $\mathcal U$ とし、入出力を
$V,I\in\mathcal U$ とする。  
自然界の等価関係:

$$
I=\mathcal Y(s)V+I_0(s)
$$

ここで $\mathcal Y(s):\mathcal U\to\mathcal U$ が可逆なら

$$
V=V_{\mathrm{th}}(s)-Z_{\mathrm{th}}(s)I
$$

$$
Z_{\mathrm{th}}(s)=\mathcal Y(s)^{-1},\quad
V_{\mathrm{th}}(s)=\mathcal Y(s)^{-1}I_0(s)
$$

これは有限次元回路の Thevenin/Norton を
無限次元境界演算子へ拡張した形。

---

## 41. ラプラス変換の意味（抽象系）

状態空間表現:

$$
\dot x=Ax+Bu,\quad y=Cx+Du
$$

ラプラス像:

$$
Y(s)=H(s)U(s),\quad
H(s)=C(sI-A)^{-1}B+D
$$

意義:
- 時間領域の畳み込みを代数積へ変換
- 極/零点で安定性・共振・減衰を分類
- 逆問題で同定対象を `H(s)` / `Ycal(s)` に圧縮

---

## 42. 受動性・因果性（境界理論）

受動系の要件（周波数応答）:

$$
\mathrm{Re}\,\langle V,\mathcal Y(i\omega)V\rangle \ge 0
$$

解析性:
- $\mathcal Y(s)$ は $\mathrm{Re}(s)>0$ で解析
- Kramers-Kronig により実部/虚部が結合

これを満たすと、抽象回路としての物理整合が取れる。

---

## 43. 古典力学（詳細）

WKB だけでなく、正準構造で書く:

$$
\dot q_\pm=\frac{\partial H_\pm}{\partial p_\pm},\quad
\dot p_\pm=-\frac{\partial H_\pm}{\partial q_\pm}
$$

交換を加えた有効力学:

$$
\dot n_\pm = \pm\Gamma(n_\mp-n_\pm)
$$

ここで $n_\pm$ はセクター占有。  
軌道（力学）と占有（可視性）を分離記述できる。

---

## 44. 熱力学・統計（詳細）

局所平衡近似では、自由エネルギー汎関数
$\mathcal F[p_+,p_-]$ を導入して

$$
\partial_t p_i = \nabla\!\cdot\!\left(M_i\nabla\frac{\delta\mathcal F}{\delta p_i}\right)+R_i
$$

$$
R_+=\Gamma(p_--p_+),\quad R_-=-R_+
$$

すると

$$
\frac{d\mathcal F}{dt}\le 0
$$

を構成しやすく、散逸系として厳密化できる。

---

## 45. 量子（詳細）

可視は部分トレースではなく可視操作で定義:

$$
\rho_+^{u}:=\mathcal E_+(\rho)=P_+\rho P_+
$$

$$
p_{\mathrm{vis}}=\mathrm{Tr}\,\rho_+^{u},\quad
\rho_+^{\mathrm{norm}}=\rho_+^{u}/p_{\mathrm{vis}}
$$

有効時間発展は（条件付きで）GKSL:

$$
\dot\rho_{\mathrm{vis}}
=-\frac{i}{\hbar}[H_{\mathrm{eff}},\rho_{\mathrm{vis}}]
+\sum_k\left(L_k\rho_{\mathrm{vis}}L_k^\dagger-\frac12\{L_k^\dagger L_k,\rho_{\mathrm{vis}}\}\right)
$$

---

## 46. 電磁気（詳細）

Maxwell の境界写像（DtN）として:

$$
I_t = \mathcal Y_{\mathrm{EM}}(s)V_t
$$

LoNalogy 二層化:

$$
\mathcal Y_{\mathrm{EM}}
=
\begin{bmatrix}
\mathcal Y_{++}&\mathcal Y_{+-}\\
\mathcal Y_{-+}&\mathcal Y_{--}
\end{bmatrix}
$$

測定は $I_+,V_+$ のみでも
$\mathcal Y_{+-}\mathcal Y_{--}^{-1}\mathcal Y_{-+}$ を通じて
不可視構造が推定できる。

---

## 47. 相対論（詳細）

重力を含めると

$$
G_{\mu\nu}=8\pi G\left(T_{\mu\nu}^{(+)}+T_{\mu\nu}^{(-)}+T_{\mu\nu}^{(\Theta)}\right)
$$

交換は共変に

$$
\nabla_\mu T^{\mu\nu}_{(\pm)}=\pm Q^\nu
$$

で与える。  
背景だけでなく摂動でも同じ $Q^\nu$ 分解を使うのが一貫的。

---

## 48. 宇宙論（詳細）

線形成長の代表形:

$$
\ddot\delta_m + 2H\dot\delta_m - 4\pi G_{\mathrm{eff}}\rho_m\delta_m = S_Q
$$

観測量:
- 背景: $H(z)$
- 成長: $f\sigma_8(z)$
- 弱レンズ: $S_8$

要件:
- 同一パラメータで3系統同時に再現
- 片方だけ合わせる自由度は許容しない

---

## 49. 素粒子論（詳細）

基礎検証フロー:
1. ポータルを1本固定  
2. RG で摂動論的一貫性確認  
3. 真空安定性・ユニタリティ境界を確認  
4. 実験拘束（LHC/直接検出/間接検出）と同時評価

理論の強さは「最小自由度で生き残るか」で決まる。

---

## 50. 弦理論（詳細）

実装手順:
1. コンパクト化クラス固定  
2. 交差数で世代を計算  
3. タドポール/K理論/Yukawa選択則を同時適用  
4. 余剰U(1)の質量化を確認

最終的には、整数制約問題として
`g=1,2` が排除されるかを機械的に判定する。

---

## 51. 逆問題工学（詳細）

multi-static データ:

$$
d(r,s,\omega)\ \longrightarrow\ \mathcal Y_{\mathrm{eff}}(i\omega)
$$

推定対象:
- 混合項 $\mathcal Y_{+-},\mathcal Y_{-+}$
- 不可視側 $\mathcal Y_{--}$ の有効寄与

これが「見えない自由度を設計変数にする」核心。

---

## 52. どこまでが理論、どこからが仮説か

理論コア（高信頼）:
- LCMS 閉体系
- 射影観測
- 有効化（GKSL）
- 境界演算子同定

仮説コア（要検証）:
- 具体的な $Q^\nu$ 形
- 弦埋め込みでの 3世代必然化
- 宇宙データ同時適合の優位性

---

## 53. プラトン・イデア論の数式対応

LoNalogy の対応は次で固定できる:

- イデア界（全体）: 全状態 $\rho\in\mathcal B(\mathcal H)$
- 現象界（可視）: 可視操作 $\mathcal E_+$
- 洞窟の壁: 情報圧縮写像 $\rho\mapsto \rho_+^{u}$

数式的には

$$
\rho_+^{u}=\mathcal E_+(\rho)=P_+\rho P_+,\quad
\rho_+^{\mathrm{norm}}=\rho_+^{u}/\mathrm{Tr}(\rho_+^{u})
$$

で「全体」と「見える像」を分離できる。

---

## 54. 哲学対応の物理的意味

- 全体保存はイデア側で成立
- 観測欠損は現象側で発生
- $\Sigma p_{\mathrm{visible}}<1$ は矛盾ではなく射影効果

$$
\mathrm{Tr}(\rho)=1,\quad
p_{\mathrm{vis}}=\mathrm{Tr}(P_+\rho)\le 1
$$

ここでの差分は「未観測自由度の重み」。

---

## 55. 木村理論との接続（逆散乱）

狙い:
- 可視の境界散乱データから
- 不可視セクターの有効寄与を推定

観測データ（multi-static）:

$$
d(r,s,\omega)
\ \longrightarrow\
\mathcal Y_{\mathrm{eff}}(i\omega)
$$

これを逆問題として解き、内部の有効媒質/散乱核を復元する。

---

## 56. `p-` 推定の数理フロー

可視-不可視の消去で自己エネルギー核が出る:

$$
\Sigma(E)=H_{+-}(E-H_{--})^{-1}H_{-+}
$$

可視側有効演算子:

$$
\mathcal Y_{\mathrm{eff}}
=
\mathcal Y_{++}
-\mathcal Y_{+-}\mathcal Y_{--}^{-1}\mathcal Y_{-+}
$$

つまり、`p-` 世界は直接観測不能でも
$\Sigma(E)$ / $\mathcal Y_{\mathrm{eff}}$ を通して間接推定できる。

---

## 57. `p-` で何が復元できるか

直接復元が難しいもの:
- 全位相情報（ゲージ不定性）

比較的復元しやすいもの:
- スペクトル密度
- 有効結合強度分布
- 占有重み（低次モーメント）

実務上は「完全再構成」より
「識別可能な統計量の推定」が現実的。

---

## 58. 木村理論を使うと何が進むか

1. 境界データから不可視寄与を定量化  
2. `p-` を“ノイズ”でなく推定対象に昇格  
3. LoNalogy の射影構造に実験接点を作る

これにより、
「イデア界は数式だけの仮定」から
「境界データで拘束可能な仮説」へ進む。

---

## 59. 哲学命題の科学化条件

古典哲学の論点を工学的に言い換えると:

- 直接認知不能でも
- 観測可能量に一意な痕跡を残すなら
- 反証可能な科学命題にできる

LoNalogy ではその痕跡が
$\mathcal Y_{\mathrm{eff}}$ や $\Sigma(E)$ に対応する。

---

## 60. 位置づけ（哲学と科学の接続）

- 哲学: 「見える世界は全体の像にすぎない」
- 科学: 像から逆写像を推定して全体を拘束する

したがって本理論の主張は:

$$
\text{不可視} \not\Rightarrow \text{不可知}
$$

条件はただ一つ:
\[
\text{境界データから識別可能であること}
\]

---

## 61. GPT-5.2 グルーオン結果との接続（2026-02）

- 対象: [arXiv:2602.12176](https://arxiv.org/abs/2602.12176)
- 主張（論文側）: half-collinear 領域で single-minus tree amplitude が非零
- 値域: 
$$
A_n(1^-,2^+,\dots,n^+)\big|_{\mathrm{half\text{-}coll}} \in \{0,+1,-1\}
$$
- 本節の立場: LoNalogy からの「再解釈」と「適用条件の整理」

---

## 62. 散乱振幅の最小比較

既知（MHV, 2 minus）:

$$
A_n^{\mathrm{MHV}}=\frac{\langle ij\rangle^4}{\langle12\rangle\langle23\rangle\cdots\langle n1\rangle}
$$

今回（single-minus, half-collinear）:

$$
A_n \in \{0,+1,-1\},\quad \text{piecewise constant}
$$

- 同じ Yang-Mills 内で「連続有理関数」型と「離散符号」型が共存

---

## 63. 接続1: `j=\sigma_3` と離散値

既存定義:

$$
j:=\sigma_3,\quad j^2=I,\quad
P_\pm=\frac{I\pm j}{2}
$$

固有値:

$$
\mathrm{spec}(j)=\{+1,-1\}
$$

可視射影での離散化:

$$
\langle j\rangle_\rho=\mathrm{Tr}(j\rho)=p_+-p_- \in [-1,1]
$$

- 極限チャネルでは $\langle j\rangle_\rho\to \pm1$、完全抑制で $0$
- よって $\{0,\pm1\}$ は `P_\pm` 構造と整合

---

## 64. 接続2: half-collinear を射影縮退として見る

通常:

$$
P_+P_-=0
$$

half-collinear の整列（例: $|i\rangle\propto|j\rangle$）では、
有効理論側で射影の分離が弱まり、可視側に混合漏れが出る:

$$
\rho_+^{u}=P_+\rho P_+,\quad
\delta\rho_+^{u}\sim P_+\rho P_- + P_-\rho P_+
$$

連続方程式のコヒーレンス項:

$$
\partial_t p_+ + \nabla\!\cdot J_+
=2\Gamma\,\mathrm{Im}(\psi_+^\ast\psi_-)
$$

- 非零 single-minus はこの混合寄与が可視化されたケースとして解釈可能

---

## 65. 接続3: CGL での位相凍結と `j` 支配

有効式:

$$
\partial_t\Psi=(\alpha+i\omega+j\kappa+ij\lambda)\Psi+B\nabla^2\Psi+C|\Psi|^2\Psi
$$

half-collinear を
「回転自由度の凍結（$i\omega$ 有効低下）+ 分離軸の顕在化（$j\kappa$ 優勢）」とみなすと、
振幅は区分定数化しやすい:

$$
\Psi \ \xrightarrow[\omega_{\mathrm{eff}}\to 0]{}\ 
\exp\!\bigl((\alpha+j\kappa)t\bigr)\Psi_0
$$

- 連続位相干渉より、セクター選択の離散性が前面化

---

## 66. 接続4: 伝搬 (`i`) / 選択 (`j`) の二重性

- `i`-主導領域: 波動的伝搬・干渉（連続）
- `j`-主導領域: セクター選択・符号化（離散）

概念図式:

$$
\text{MHV} \leftrightarrow i\text{-dominant},\qquad
\text{single-minus (half-coll)} \leftrightarrow j\text{-dominant}
$$

- 新しい相互作用を追加せず、同一理論内の有効支配軸の違いとして整理

---

## 67. 接続5: Burgers 示唆と Madelung 経路

既存経路:

$$
\psi_\pm=\sqrt{\rho_\pm}e^{iS_\pm/\hbar}
\ \Longrightarrow\
\text{流体型方程式}
$$

1次元・粘性近似で:

$$
\partial_t u + u\,\partial_x u=\nu\,\partial_x^2 u
$$

- 論文の Burgers 関連示唆は、
LoNalogy の「振幅方程式 $\to$ Madelung $\to$ 流体」連結と整合

---

## 68. 接続6: 重力子拡張との整合的見取り図

既存重力側:

$$
G_{\mu\nu}=8\pi G\left(T_{\mu\nu}^{(+)}+T_{\mu\nu}^{(-)}+T_{\mu\nu}^{(\Theta)}\right)
$$

振幅側での期待:

$$
\mathcal M_n \sim (A_n)^2 \quad \text{(KLT 型関係の文脈)}
$$

- グルーオン側の half-collinear 非零が重力側へ写る可能性は自然
- ただしここは「作業仮説」。実際のヘリシティ・境界条件で要検証

---

## 69. 方法論的位置づけと検証項目

方法論の相補性:

- GPT-5.2: 帰納（小$n$計算から一般式の発見）
- LoNalogy: 演繹（`j=\sigma_3`, `P_\pm`, 混合項から構造説明）

検証可能な作業項目:

1. half-collinear 条件のもとで $\Gamma$ と符号領域（chamber）の対応を明示化  
2. $\mathcal Y_{\mathrm{eff}}$ 側に符号関数積の痕跡が出るかを逆問題で検定  
3. 重力子拡張で $\{0,\pm1\}$ 構造がどこまで保持されるかを確認

- 立場: 「予言」ではなく「既報結果を統一枠で説明する再記述」

---

# End
## 改稿版の原理

> `i` は位相の言語、`j` は可視性分離の言語  
> その両立を、基礎理論と有効理論の分離で実装する
