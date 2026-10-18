# Benchmark Results

**Generated:** 2026-10-18 10:28 UTC  
**Go:** 1.22  
**Platform:** linux/amd64  
**CPU:** AMD EPYC 7763 64-Core Processor                  

## Field Read

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Reflect | 68.8 | 8 | 1 | — |
| ReflectFast | 3.21 | 0 | 0 | 21.4× faster |
| SafeRefl | 44.6 | 0 | 0 | 1.5× faster |
| Offset | 11.4 | 0 | 0 | 6.0× faster |
| Accessor | 0.928 | 0 | 0 | 74.1× faster |
| Native | 0.312 | 0 | 0 | 220.6× faster |

## Slice At

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 1.01 | 0 | 0 | — |
| Direct | 0.995 | 0 | 0 | 1.0× faster |
| Reflect | 3.74 | 0 | 0 | 3.7× slower |

## Map Len

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.625 | 0 | 0 | — |
| Builtin | 0.311 | 0 | 0 | 2.0× faster |
| Reflect | 4.69 | 0 | 0 | 7.5× slower |

## Kind Of

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.935 | 0 | 0 | — |
| Reflect | 2.18 | 0 | 0 | 2.3× slower |

## Is Nil_ptr

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 3.39 | 0 | 0 | — |
| Reflect | 2.46 | 0 | 0 | 1.4× faster |

## Each Field

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 50.4 | 0 | 0 | — |
| Reflect | 154 | 56 | 5 | 3.1× slower |
| ReflectFull | 159 | 56 | 5 | 3.1× slower |
| Reflect2 | 24.7 | 0 | 0 | 2.0× faster |

## Copy Fields

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 282 | 0 | 0 | — |
| Manual | 0.306 | 0 | 0 | 920.3× faster |
| Reflect | 583 | 80 | 10 | 2.1× slower |

## To Map

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 224 | 336 | 2 | — |
| Reflect | 518 | 432 | 12 | 2.3× slower |
| JSON | 2767 | 776 | 25 | 12.3× slower |

## Map For Each

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 961 | 0 | 0 | — |
| Range | 984 | 0 | 0 | 1.0× slower |

## Get_int

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 44.9 | 0 | 0 | — |
| Reflect | 67.8 | 8 | 1 | 1.5× slower |
| ReflectFast | 3.12 | 0 | 0 | 14.4× faster |
| Offset | 11.7 | 0 | 0 | 3.8× faster |
| Accessor | 0.931 | 0 | 0 | 48.2× faster |
| AccFrom | 3.09 | 0 | 0 | 14.5× faster |
| Direct | 0.304 | 0 | 0 | 147.3× faster |

## Set_string

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 45.8 | 0 | 0 | — |
| Reflect | 72.6 | 8 | 1 | 1.6× slower |
| ReflectFast | 4.99 | 0 | 0 | 9.2× faster |
| Offset | 13.8 | 0 | 0 | 3.3× faster |
| Accessor | 1.24 | 0 | 0 | 36.8× faster |
| AccOn | 4.75 | 0 | 0 | 9.6× faster |
| Direct | 0.617 | 0 | 0 | 74.1× faster |

## DI Resolve

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 0.614 | 0 | 0 | — |
| SafeRefl | 150 | 0 | 0 | 244.7× slower |
| Accessor | 3.14 | 0 | 0 | 5.1× slower |
| Reflect2 | 20.9 | 0 | 0 | 34.0× slower |
| Reflect | 239 | 24 | 3 | 389.8× slower |

## JSON Decode

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| StdlibJSON | 2655 | 392 | 10 | — |
| SafeRefl | 512 | 0 | 0 | 5.2× faster |
| Reflect | 1697 | 160 | 20 | 1.6× faster |
| Reflect2 | 77.7 | 0 | 0 | 34.2× faster |
| Accessor | 9.43 | 0 | 0 | 281.5× faster |

## ORM Scan

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 13.8 | 0 | 0 | — |
| SafeRefl | 535 | 0 | 0 | 38.6× slower |
| Accessor | 15.0 | 0 | 0 | 1.1× slower |
| Reflect2 | 82.6 | 0 | 0 | 6.0× slower |
| Reflect | 977 | 80 | 10 | 70.6× slower |
| Copier | 7223 | 880 | 58 | 521.6× slower |

## Struct Copy

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 9.61 | 0 | 0 | — |
| Accessor | 10.6 | 0 | 0 | 1.1× slower |
| Reflect2 | 40.3 | 0 | 0 | 4.2× slower |
| Offset | 185 | 0 | 0 | 19.2× slower |
| Reflect | 780 | 80 | 10 | 81.2× slower |
| SafeRefl | 526 | 0 | 0 | 54.7× slower |
| Copier | 3226 | 552 | 32 | 335.6× slower |

