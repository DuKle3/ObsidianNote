dislocations by **plastic deformation**

## Frank-Read Source

- dislocation generator

- infinite number of disl loops (材料變硬-> disl line變多)

## Nucleation of Dislocations

### 1. homogeneous

- require extremely high stresse

### 2. heterogeneous

- formed with the help of defects

> 10GPa <--> 0.7Mpa

### observing disl

- an etching reagent : etch pit

- new : 底部是尖的
- old : 較平緩

## Bend Gliding

- Negative edges 聚集 : 累積


- positive edges 到表面 
- screw : leave the crystal

## Rotational Slip

- 產生很多disl line
- slip plane contain more than one possible slip direction
- HCP and FCC are ideal


## Slip planes and Slip directions

- slip occurs most on **high atomic density**

- separation between planes is proportional to the density of the planes
> closed packed plane 密度大, 兩個面之間 : 遠

- 遠 : 鍵結能較小

- slip direction most close packed direction
	- does not disturb th crystal structure
	- smallest strain energy

## Slip Systems

- slip planes + Slip directions --> slip systems

- FCC slip system : 最多

## Critical Resolved Shear Stress

- $\tau_{crss}$ : yield stress 

- 向量分解 -> 分到slip direction 上

#### Resolved shear stress
> shear stress on the slip plane in the slip direction

**Schmid's Law**
$$\tau_R : \sigma \cos(\theta)\cos(\phi)$$

- Tensile axis `perp` slip plane --> $\phi$ = $90^\circ$ --> $\tau_R = 0$  
- Tensile axis lies on the slip plane --> $\theta = 90^\circ$ --> $\tau_R = 0$

> No shear stress --> no slip

- max : $45^\circ$ 

- there may be many available slip systems

- primary slip system : 第一個(最主要的)

### Stress hardening

- impurity $\alpha$ hardness = $\tau$ 
- $\tau$ 越大 : high strength

- FCC 有最多slip system : $\tau_{crss}$ is low
- FCC : high ductilities 

- BCC : high strengths and lower ductilities

## Strengthening of metallic materials : 變硬方法

**Preventing dislocation motion** : 讓disl 固定 <--> hardness

### 1. Work hardening

- ex 打鐵 : introduce dislocations into materials : **yield strengths** 變大
- Dislocations interact with each other : 沒有辦法移動

### 2. Solid Solution Strengthening / Alloying (impurity)

- `substitutional` or `interstitial`
- cause lattice distortions : impede dislocation motion

### 3. Precipitation Hardening (impurity)

- disl interact with the precipitate : **block the motion**

### 4. Grain Boundary (Grain Size) Strengthening

- GB as an impediment to dislocation motion 
	1. disl need change direction of motion
	2. slip plane discontinuity 

> disl 很難過GB --> grain 方向不同

### 5. Transformation Hardening

- **steel**

- 相變態

- heated to the temperature from ferrite into austenite
> changes crystal structure


## Slip On Equivalent Slip Sysems

- slip will start on the system with the **highest resolved shear stress**
> $\tau_{crss}$ --> primary slip system

## Dislocation Density

- disl 很少跑到表面失去掉 (在形成的時候)
	- \# of dislocation : 增加
	- hardness , strength : 增加

- $\rho$ 
	1. estimating th length of the disl line
	2. number of disl etch pits (\#/$cm^2$) : 簡單

## Slip Systems in different crystal forms

### FCC
- closed packed direction : <110>
- closed packed planes : (111),(-111),(1-11),(11-1)
- 每個面有三個direction
- 4 * 3 = 12 slip systems
- $\tau_{crss}$ : 一樣，且low for slip

- multiple glide : 很多slip system 碰在一起
	- **strain hardening**

### BCC

- close packed directions : <111>
- no truly closed packed plane
	- slip plane is not well defined
	- 有<111> 的plane can act as a slip plane
- $\tau_{crss}$ 較高

### HCP

- ${c \over a}$ : 面的距離

- Zn,Cd,Mg : ${c \over a}$ > 1.632
	- 距離遠 : disl 不容易跑
	- $\tau_{crss}$ 小

- Ti,Be,Zr : ${c \over a}$ < 1.632
	- 距離短 : disl跑的範圍大 : ductility
	- $\tau_{crss}$ 大

> **Ductility : FCC > BCC > small${c \over a}$ > big${c \over a}$  > cubic**


## Cross-Slip

- two or more slip planes with a common slip direcion

- screw dislocation : occur
- edge dislocation : move in a single slip plane


- **In many HCP metals, no cross-slip can occur** : 因為the slip plane are parallel 
> not intersecting slip systems
> **No cross slip(brittle)

## Slip Bands

- single large line
	- slip band : 一整條
	- disl line : 點

## Double Cross-Slip

- disl loopo 會變大

## Extended Dislocations and Cross-Slilp

- FCC : b = c + d
- see PDF page 49

> 不會發生(因為複雜)
> b: 1/2[-110] is easier to cross-slip

## Crystal Structure Rotation during Tensile and Compressive Deformation

- In tensile 
	- slip plane 逐漸 `parallel` tensile stress
- In compression
	- slip plane 逐漸 `perp` stress 

- 看ppt

## Work Hardening

- 超過yield stress : plastic deformation : 產生dislocation : 變硬

### True stress and strain

- **instantaneous cross-section area**

- $$\sigma_t = {P \over A_i}$$ 
- $$\varepsilon_t = {\Delta l \over l_i}$$
> 利用體積不變，上下同乘以$l_0$ ,得:
> $$\sigma_t = \sigma_e (1+\varepsilon_e)$$
> $$\varepsilon_t = \ln(1+\varepsilon_e)$$


## Considere's Criterion

- maximum load
	- 右邊 : Reduction of area > strain hardening
	- 左邊 : Strain hardening > reduction of area

- $$\sigma_t = {d\sigma_t \over d\varepsilon_t}$$
- 上式利用 dP = 0 和 體積不變 (dV = d($A_i l_i$)) = 0 )

> 斜率和true stress 相等時, necking should begin

## Relation Between Dislocation density and The stress

- experimentally observed

- stress $\alpha$ $\rho^{1\over2}$ 
 
- if $\rho$ is zero , the metal could not be deformed

## Taylor's relation

- r : flow stress
- r $\alpha$ $\rho^{1\over2}$

## Dislocation velocity

$$v = f(\sigma)e^{-E\over kT}$$
- $25^\circ > T > -50^\circ$

## The Orowan Equation (Strain Rate)

- 看不懂ㄌ


