<div align="center">

# ISL81802 48V转12V 20A大功率同步降压电源板





> 基于瑞萨ISL81802交错相位降压，48V输入转12V/20A大功率工业机器人电源板

</div>

## 📖 项目简介
本项目为大功率DC‑DC降压电源板，采用 **Renesas ISL81802** 双相同步降压控制器，采用两相交错并联架构，输入48V直流，输出12V最大20A（240W）功率输出。
适合机器人电控、工业设备供电，可配合前面48V机器人电源板、EtherCAT‑CAN网关板整套机器人电控系统使用。
开源完整Altium Designer原理图、PCB工程与BOM物料清单，可直接打板、二次修改。

## ✨ 核心功能
- 🔌 输入电压：48V直流，最高耐压80V
- ⚡ 输出：12V，最大20A，总功率240W，两相交错并联降低输出纹波
- 🛡️ 芯片自带完整保护：过压OVP、欠压UVP、过流OCP、过热OTP保护
- 📈 可编程软启动，防止上电冲击电流
- 🤖 应用场景：移动机器人、伺服供电、工业设备大功率供电

## 🛠️ 技术方案 & 设计要点
- EDA软件：Altium Designer
- 主控芯片：Renesas ISL81802（80V双相同步Buck控制器）
- 拓扑：两相交错并联同步降压，分担电流，降低发热与纹波
- 开关频率：外部电阻配置
> 💡 设计难点：
大电流电源PCB铺铜处理，功率回路尽量缩短，减小寄生电感；两相功率回路对称布局；功率地与信号地分割处理，降低开关噪声；大电流过孔数量充足，满足20A载流能力。

## 🖼️ 工程预览
<img width="1133" height="718" alt="image" src="https://github.com/user-attachments/assets/a13453a3-aa32-41d9-908a-663426a4e286" />

> 图：ISL81802电源原理图
<img width="1148" height="677" alt="image" src="https://github.com/user-attachments/assets/dcda2f67-3e06-4941-b535-8cab9af8ab99" />

> 图：PCB底层功率布局
<img width="1148" height="673" alt="image" src="https://github.com/user-attachments/assets/ec0cebf1-e082-4531-9010-0f970ff8cb8e" />
[ISL81802-48V-12V20A_Project.pdf](https://github.com/user-attachments/files/33857627/ISL81802-48V-12V20A_Project.pdf)


## 📋 打板说明
1. 使用Altium Designer20及以上版本打开工程
2. 大电流区域铜厚建议≥2oz，功率过孔多打，满足20A载流
3. 注意功率回路走线尽量短，减小开关电源噪声
4. 调试顺序：先低压上电测试，再逐步升高输入电压，测试满载输出

## ⚠️ 调试注意事项
- 本板为大功率电源，满载会产生较高温度，必须配备散热措施
- 上电前确认输入正负极，反接会烧毁功率器件
- 满载测试注意电源、MOS管、电感温度，防止过热损坏

## 📜 开源协议
本项目基于 **MIT License** 开源。
允许查看、修改、复刻、商用，仅需保留原始版权声明。

## 📮 交流反馈
发现bug或优化建议请提交 Issue；
欢迎Fork本项目，提交PR共同完善。

