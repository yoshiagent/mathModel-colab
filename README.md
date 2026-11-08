# 數學建模：原課程 MATLAB 程式的 Python 筆記本

「[數學建模 Mathematical Modeling](https://yoshiagent.github.io/mathModel/)」課程原本以 MATLAB／Simulink 示範。這裡把原課程的 MATLAB 程式與 Simulink 模型改寫成 Python 筆記本，可以直接在 Google Colab 執行，不需要安裝任何軟體。

| 筆記本 | 內容（原課程的檔案） | 對照的網頁 | 開啟 |
|---|---|---|---|
| [一階系統](notebooks/O1_FirstOrder.ipynb) | order1.m／order1a.m／Order1Sybolic.m（步階與自然響應、符號解）、order1b.m／order1c.m（低通與高通的 Bode 圖、步階響應）、order1Bode_01.mdl（正弦輸入的穩態響應）、order1Filter.mdl（低通濾波）、FreqResp_01.m、Bode 漸近線與積分器 | [網頁](https://yoshiagent.github.io/mathModel/O1.html) | [![在 Colab 開啟](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/yoshiagent/mathModel-colab/blob/main/notebooks/O1_FirstOrder.ipynb) |
| [二階系統](notebooks/O2_SecondOrder.ipynb) | ord2／damp、齊次解三種情況、步階響應規格（tr、tp、Mp、ts）、StandardOrder2.m、MpZeta.m／TrZeta.m／TrZeta1.m、zetaConstant.m／wdConstant.m、pzmap＋sgrid、共振頻率／共振峰／頻寬 | [網頁](https://yoshiagent.github.io/mathModel/O2.html) | [![在 Colab 開啟](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/yoshiagent/mathModel-colab/blob/main/notebooks/O2_SecondOrder.ipynb) |
| [機械與電路系統](notebooks/Mech_Elec_Systems.ipynb) | 轉動慣量公式（積分驗證）、齒輪與直線運動的等效慣量、RCData.m／RC.mdl、RC／RL 高通與低通、mck.mdl、mckss.m／ssmodel.mdl、MCKTFM.m／MCKTf.mdl、RCLData.m／RCL.mdl | [網頁](https://yoshiagent.github.io/mathModel/MCK.html) | [![在 Colab 開啟](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/yoshiagent/mathModel-colab/blob/main/notebooks/Mech_Elec_Systems.ipynb) |
| [直流馬達](notebooks/DC_Motor.ipynb) | DCMotorData.m／DCMotorTf.mdl／DCMotorTf1.mdl／DCMotorSS.mdl、方塊圖化簡、DCMotorDataMaxon.m／DCMotorMaxon1.mdl（時間常數）、DCMotorTfTL.mdl（負載轉矩）、DCMotorTfTLRotD.m／DCMotorTfTLRot.mdl／DCMotorTfTLRot1.mdl（齒輪負載）、伺服馬達選用 | [網頁](https://yoshiagent.github.io/mathModel/DCM.html) | [![在 Colab 開啟](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/yoshiagent/mathModel-colab/blob/main/notebooks/DC_Motor.ipynb) |
| [倒單擺與汽車懸吊](notebooks/InvertPole_Suspension.ipynb) | 倒單擺運動方程式（Lagrange 驗證）、InvertPole.zip 的 slcp.mdl（Cart & Pole Dynamics）與 slcp.fis 模糊控制、線性化；汽車懸吊半車模型的矩陣推導與凸塊響應 | [網頁](https://yoshiagent.github.io/mathModel/IP.html) | [![在 Colab 開啟](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/yoshiagent/mathModel-colab/blob/main/notebooks/InvertPole_Suspension.ipynb) |

* 每本筆記本都先列出原本的 MATLAB 程式，再給逐段對應的 Python 版本，並已實際執行（存有輸出與圖）。
* 只用 Colab 內建的 numpy、scipy、sympy 與 plotly。
* Simulink 模型以 `scipy.signal`（轉移函數）或 `scipy.integrate.solve_ivp`（微分方程式）重現，參數取自原 .mdl 檔。
