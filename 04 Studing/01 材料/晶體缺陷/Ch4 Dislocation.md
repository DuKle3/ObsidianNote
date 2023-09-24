
## Edge dislocation

`b` perp `ED`
`b` parallel `ED move`

## Screw dislocation

`b` parallel `SD`
`b` perp `SD move`

## Slip plane

- contain the [[#Edge dislocation]] and `b`
- Edge
	- uniquely defined  (`b` perp `ED`)
- Screw
	- can be any plane  (`b` parallel `SD`)

- most happens **close-packed plane**
	- energetically favored

## Disl in FCC

### partial (extended disloction)

- b = c + d

- when $b^2 > c^2 + d^2$ (因為能量 $\alpha$ 平方 )

### stacking faults

- Discontinuity : ABCA""CABC 
- additional planes of atoms (移動中)

#### 1. Shockley type

- `b,c,d` is **lying** in the plane of the fault

#### 2. Frank type

- `b` is **normal** to the stacking fault

### Stacking Fault Energy (SFE)

1. 相斥 (反比於d)
2. area不能太大塊 (E高) (正比於d)

> 有equilibrium position d

- SFE is high
	- separation small
- SFE is low
	- wider stacking faults

## Intrinsic and Extrinsic Stacking Faults 

### Frank partial dislocations : intrinsic(single)

- ABCA""C
- Difficult to move (Sessile) along `b` (`b` prep disl line)
> climb only

### Extrinsic(double)

- ABCA""C""BC
- much less probable
- by the precipitation of interstitial atoms on the octahedral plane

## Extended Dislocations in Hexagonal Metals (HCP)

---

## Climb of Edge Dislocations

### Edge

- slip plane : only one plane
- slip in its **single slip plane**

### Screw

- slip plane : contains both the disl line and `b` (many)
- slip in any direction 

### Climb 

different from slip , edge dislocation can move

- motion in the direction `perp` slip plane
- 因為vacancy ，disl 往上移動 

#### 1. Positive climb

- extra plane 減少
- 因為跑到空位

#### 2. Negative climb

- extra plane 增加
- 因為空位跑過來

> 都需要vacancy,都跟溫度有關

> climb : 不是整個一起移動
> slip  : 整個一起移動

### in edge dislocations

- shear stress --> slip 
- normal stress --> climb

## Dislocation Intersections

- disl 遇到 disl : **require works** to cut through other disl

1. jogs : `perp` slip plane
2. kinks : `parallel` slip plane

### kinks

`b` 在 slip plane 上

#### edge-edge intersection - screw type
#### screw-screw intersection - edge type
- both of steps can be eliminated easily
- the step tends to disappear

### jogs

`b` `perp` to slip plane

- `b1` `perp` `b2`
- immobile (不容易動) versus kinks 
- and require **climb** 


## The stress field of a Screw Dislocation

### Map


``` mermaid
graph LR;
Displacement-->Strain;
Strain-->Stress;
Stress-->Strain-Energy;

```

### Strain Energy
#### Screw

$$ W_s = \quad {\mu b^2 \over 4 \pi} \ln({r^\prime \over r_0}) $$

#### Edge 

$$ W_s = \quad {\mu b^2 \over 4 \pi(1-\nu)} \ln ({r^\prime \over r_0}) $$

$\upsilon$ : Poisson's ratio : ${1 \over (1-\nu)}$ 

> edge dislocation is about 50% larger than screw dislocation

(大部分金屬 $\nu$ = ${1 \over 3}$)

