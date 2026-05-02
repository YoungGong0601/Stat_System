# Stat_System
> Unity Stat/Buff Management System

- Observer
- Dirty Flag

- no Linq
- no Garbage

## 계산방식
```
Result = ((Value + Flat) + (Value * PercentAdd)) * Multiplier
```
- 가중치 Type : Flat, PercentAdd, Multiple

## 기능
- modifier
- dynamic modifier : 타 Stat과 값 연동

## Example
```
Speed.AddModifier(new StatModifier(-1f, ModifierType.Flat, "Death"), (int)StatLayerType.FinalCalculation);
```
```
PLAYER.Stat.FinalDamage.AddModifier(new StatModifier(0.3f, ModifierType.PercentAdd, "UpgradeTile"));
```
```
Damage_Dash.AddModifier(
  new DynamicModifier(FinalDamage, 1f, ModifierType.Multiplier, "FinalDamage_Dash"),
  (int)StatLayerType.FinalCalculation);
```
