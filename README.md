# BreakInfinity.cs
A C# port of [break_infinity.js](https://github.com/Patashu/break_infinity.js) - a solution for incremental games which want to deal with very large numbers (bigger in magnitude than 1e308, up to as much as 1e(9e15) ) and want to prioritize speed over accuracy.

## Installation

### In the form of a unity module

Installation as a unity module via a git link in the PackageManager or direct editing of `Packages/manifest.json` is supported:

```
"com.portaldweller.breakinfinity": "https://github.com/PortalDweller/BreakInfinity.cs.git",
```

### As source

The code can also be cloned or obtained as an archive from the releases page.

Alternatively, just drop [BigDouble.cs](https://github.com/PortalDweller/BreakInfinity.cs/blob/master/BreakInfinity/BigDouble.cs) file into your `Scripts` folder and use `BigDouble` type instead of `double` in your scripts

## BigDouble
`BigDouble` is a `double` replacement for very large numbers.

### ToString() Formats

- General
```csharp
new BigDouble(105203122911321275.6).ToString() == "1.05203122911321E+17"
new BigDouble(105203122911321275.6).ToString("G") == "1.05203122911321E+17"
new BigDouble(105203122911321275.6).ToString("G0") == "1.05203122911321E+17"
new BigDouble(105203122911321275.6).ToString("G1") == "1E+17"
new BigDouble(105203122911321275.6).ToString("G4") == "1.052E+17"
```
- Exponential
```csharp
new BigDouble(105203122911321275.6).ToString("E") == "1.052031E+017"
new BigDouble(105203122911321275.6).ToString("E0") == "1E+017"
new BigDouble(105203122911321275.6).ToString("E4") == "1.0520E+017"
```
- Fixed
```csharp
new BigDouble(105203122911321275.6).ToString("F") == "105203122911321000.00"
new BigDouble(105203122911321275.6).ToString("F0") == "105203122911321000"
new BigDouble(105203122911321275.6).ToString("F4") == "105203122911321000.0000"
```

# Credits
[Patashu](https://github.com/Patashu) - for amazing library and major effort in porting to C#
