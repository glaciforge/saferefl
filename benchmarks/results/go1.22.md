# Benchmark Results

**Generated:** 2026-08-23 06:39 UTC  
**Go:** 1.22  
**Platform:** linux/amd64  
**CPU:** AMD EPYC 7763 64-Core Processor                  

## Field Read

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Reflect | 68.2 | 8 | 1 | — |
| ReflectFast | 3.14 | 0 | 0 | 21.7× faster |
| SafeRefl | 45.1 | 0 | 0 | 1.5× faster |
| Offset | 11.6 | 0 | 0 | 5.9× faster |
| Accessor | 0.940 | 0 | 0 | 72.6× faster |
| Native | 0.313 | 0 | 0 | 218.0× faster |

## Slice At

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 1.01 | 0 | 0 | — |
| Direct | 0.998 | 0 | 0 | 1.0× faster |
| Reflect | 3.74 | 0 | 0 | 3.7× slower |

## Map Len

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.626 | 0 | 0 | — |
| Builtin | 0.312 | 0 | 0 | 2.0× faster |
| Reflect | 4.68 | 0 | 0 | 7.5× slower |

## Kind Of

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.936 | 0 | 0 | — |
| Reflect | 2.18 | 0 | 0 | 2.3× slower |

## Is Nil_ptr

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 3.43 | 0 | 0 | — |
| Reflect | 2.49 | 0 | 0 | 1.4× faster |

## Each Field

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 51.2 | 0 | 0 | — |
| Reflect | 157 | 56 | 5 | 3.1× slower |
| ReflectFull | 161 | 56 | 5 | 3.1× slower |
| Reflect2 | 25.1 | 0 | 0 | 2.0× faster |

## Copy Fields

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 285 | 0 | 0 | — |
| Manual | 0.312 | 0 | 0 | 912.2× faster |
| Reflect | 591 | 80 | 10 | 2.1× slower |

## To Map

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 227 | 336 | 2 | — |
| Reflect | 516 | 432 | 12 | 2.3× slower |
| JSON | 2789 | 776 | 25 | 12.3× slower |

## Map For Each

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 953 | 0 | 0 | — |
| Range | 982 | 0 | 0 | 1.0× slower |

## Get_int

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 45.0 | 0 | 0 | — |
| Reflect | 67.9 | 8 | 1 | 1.5× slower |
| ReflectFast | 3.12 | 0 | 0 | 14.4× faster |
| Offset | 11.7 | 0 | 0 | 3.9× faster |
| Accessor | 0.937 | 0 | 0 | 48.0× faster |
| AccFrom | 3.12 | 0 | 0 | 14.4× faster |
| Direct | 0.315 | 0 | 0 | 142.8× faster |

## Set_string

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 45.9 | 0 | 0 | — |
| Reflect | 72.3 | 8 | 1 | 1.6× slower |
| ReflectFast | 5.02 | 0 | 0 | 9.1× faster |
| Offset | 13.8 | 0 | 0 | 3.3× faster |
| Accessor | 1.25 | 0 | 0 | 36.8× faster |
| AccOn | 3.43 | 0 | 0 | 13.4× faster |
| Direct | 0.627 | 0 | 0 | 73.2× faster |

## DI Resolve

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 0.627 | 0 | 0 | — |
| SafeRefl | 153 | 0 | 0 | 243.1× slower |
| Accessor | 3.13 | 0 | 0 | 5.0× slower |
| Reflect2 | 20.9 | 0 | 0 | 33.3× slower |
| Reflect | 242 | 24 | 3 | 385.4× slower |

## JSON Decode

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| StdlibJSON | 2703 | 392 | 10 | — |
| SafeRefl | 526 | 0 | 0 | 5.1× faster |
| Reflect | 1727 | 160 | 20 | 1.6× faster |
| Reflect2 | 79.8 | 0 | 0 | 33.9× faster |
| Accessor | 9.54 | 0 | 0 | 283.3× faster |

## ORM Scan

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 14.1 | 0 | 0 | — |
| SafeRefl | 540 | 0 | 0 | 38.3× slower |
| Accessor | 12.3 | 0 | 0 | 1.1× faster |
| Reflect2 | 82.8 | 0 | 0 | 5.9× slower |
| Reflect | 981 | 80 | 10 | 69.6× slower |
| Copier | 7233 | 880 | 58 | 513.0× slower |

## Struct Copy

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 9.69 | 0 | 0 | — |
| Accessor | 10.6 | 0 | 0 | 1.1× slower |
| Reflect2 | 40.7 | 0 | 0 | 4.2× slower |
| Offset | 185 | 0 | 0 | 19.1× slower |
| Reflect | 779 | 80 | 10 | 80.4× slower |
| SafeRefl | 520 | 0 | 0 | 53.7× slower |
| Copier | 3250 | 552 | 32 | 335.3× slower |

