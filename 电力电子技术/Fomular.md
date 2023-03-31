### Chap 2

- 有效值，均方根值

  - $$
    U=\sqrt{\frac{1}{T}\int^{t_0+T}_{t_0}{u^2(t)dt}}
    $$

- 平均值

  - $$
    U_{av}=\frac{1}{T}\int^T_0{u(t)dt}
    $$

- 相控原理

  - $$
    直流输出电压平均值：U_0=0.45U\frac{1+\cos{\alpha}}{2}
    $$

- 斩控原理

  - $$
    U_0=DU_i=\frac{t_{on}}{T}U_i
    $$

### Chap 3 AC-DC

- 单相半波可控整流器
  - 整流输出电压的平均值：$\displaystyle U_0=\frac{1}{2\pi}\int^\pi_\alpha\sqrt{2}U_2\sin{\omega t}d(\omega t)=0.45U_2\frac{1+\cos{\alpha}}{2}$
  - 触发角$\alpha$的移相范围：$0\sim2\pi$
- 单相桥式
  - 整流输出电压的平均值：
    - 电阻负载：$\displaystyle U_0=\frac{1}{\pi}\int^\pi_\alpha\sqrt{2}U_2\sin{\omega t}d(\omega t)=0.9U_2\frac{1+\cos{\alpha}}{2}$
    - 阻感负载：$\displaystyle U_0=\frac{1}{\pi}\int^{\pi+\alpha}_\alpha\sqrt{2}U_2\sin{\omega t}d(\omega t)=0.9U_2\cos{\alpha}$

- 三相半波
  - 整流输出电压的平均值：
    - 电阻负载：$\displaystyle U_0=1.17U_2\cos{\alpha},\alpha\le\frac{\pi}{6},CCM$，移相范围：$0\sim\frac{5\pi}{6}$
    - 阻感负载：$\displaystyle U_0=1.17U_2\cos{\alpha},\alpha\le\frac{\pi}{6},CCM$，移相范围：$0\sim\frac{\pi}{2}$

- 三相桥式
  - 整流输出电压的平均值：
    - 电阻负载：$\displaystyle U_0=2.34U_2\cos{\alpha},\alpha\le\frac{\pi}{3},CCM$，移相范围：$0\sim\frac{2\pi}{3}$
    - 阻感负载：$\displaystyle U_0=2.34U_2\cos{\alpha},\alpha\le\frac{\pi}{3},CCM$，移相范围：$0\sim\frac{\pi}{2}$
  - 阻感负载二次侧电流的有效值：$\displaystyle I_2=\sqrt{\frac{2}{3}}I_o$


### Chap 4 DC-AC

- 电压型逆变器
  - 单相半桥逆变器
    - 输出电压基波幅值：$\displaystyle U_{o1m}=\frac{2U_d}{\pi}\approx 0.637U_d$
    - 输出电压基波有效值：$\displaystyle U_{o1}=\frac{U_{o1m}}{\sqrt{2}}=0.45U_d$
  - 单向全桥逆变器
    - 方波调制
      - 输出电压基波幅值：$\displaystyle U_{o1m}=\frac{4U_d}{\pi}\approx 1.27U_d$
      - 输出电压基波有效值：$\displaystyle U_{o1}=\frac{U_{o1m}}{\sqrt{2}}=0.9U_d$
    - 移相调制
      - $\displaystyle m_a=\frac{U_{rm}}{U_{cm}}=1$时，输出基波电压的幅值最大
      - 基波有效值$\displaystyle U_{o1}=\frac{U_{d}}{\sqrt{2}}=0.707U_d$

### Chap 5 DC-DC

- Buck

  - 输出特性

      - $$
        \frac{U_O}{U_i}=
        \left\{\begin{matrix}
        D,  &K>1-D,  &电感电流连续 \\
        \displaystyle \frac{2}{1+\sqrt{1+4K/D^2}},  &K<1-D,  &电感电流断续
        \end{matrix}\right.
        K=\frac{2L}{RT}
        $$

  - 参数选择

      - 输出电压纹波（CCM）

          - $$
              \Delta u_0=\Delta i_LT/8C=\frac{U_iD(1-D)T^2}{8LC}
              $$

          - 由此得电容取值

- Boost

  - 输出特性

    - $$
      \frac{U_O}{U_i}=
      \left\{\begin{matrix}
      \displaystyle \frac{1}{1-D},  &K>D(1-D)^2,  &电感电流连续 \\
      \displaystyle \frac{1+\sqrt{1+4D^2/K}}{2},  &K<D(1-D)^2,  &电感电流断续
      \end{matrix}\right.
      $$

  - 参数选择

    - 输出电压纹波（CCM）

      - $$
        \Delta u_0=\frac{U_oDT}{RC}
        $$

- Buck-Boost

  - 输出特性

    - $$
      \frac{U_O}{U_i}=
      \left\{\begin{matrix}
      \displaystyle \frac{D}{1-D},  &K>(1-D)^2,  &电感电流连续 \\
      \displaystyle \frac{D}{\sqrt{K}},  &K<(1-D)^2,  &电感电流断续
      \end{matrix}\right.
      $$

  - 参数选择

    - 输出电压纹波（CCM）

      - $$
        \Delta u_0=\frac{U_oDT}{RC}
        $$

#### 隔离型变换器

- 正激变换器
  - 输出电压：$\displaystyle U_o=U_i\frac{N_2}{N_1}D$
  - 占空比：$\displaystyle D=\frac{N_1}{N_1+N_3}$
  - 开关管$S$关断时承受的最大反向电压：$\displaystyle U_{sp}=U_i(1+\frac{N_1}{N_3})$
  - 二极管$VD_1$截止时承受的最大反向电压：$\displaystyle U_{VDmax}=U_i\frac{N_2}{N_3}$
- 反激变换器
  - 输出电压：$\displaystyle U_o=U_i\frac{N_2}{N_1}\frac{D}{1-D}$
  - 开关管$S$关断时承受的最大反向电压：$\displaystyle U_{sp}=U_i\frac{N_2}{N_1}+U_o$
  - 二极管$VD_1$截止时承受的最大反向电压：$\displaystyle U_{VDmax}=U_i+\frac{N_1}{N_2}U_o$



### Chap 6 AC-AC

- 交流调功电路
  - $U_o=\sqrt{D}U_i$
