# Benchmark Results

**Generated:** 2026-09-13 11:10 UTC  
**Go:** 1.22  
**Platform:** linux/amd64  
**CPU:** AMD EPYC 7763 64-Core Processor                  

## Field Read

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Reflect | 68.6 | 8 | 1 | — |
| ReflectFast | 3.19 | 0 | 0 | 21.5× faster |
| SafeRefl | 45.3 | 0 | 0 | 1.5× faster |
| Offset | 11.5 | 0 | 0 | 5.9× faster |
| Accessor | 0.936 | 0 | 0 | 73.3× faster |
| Native | 0.312 | 0 | 0 | 219.7× faster |

## Slice At

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 1.01 | 0 | 0 | — |
| Direct | 0.998 | 0 | 0 | 1.0× faster |
| Reflect | 3.75 | 0 | 0 | 3.7× slower |

## Map Len

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.626 | 0 | 0 | — |
| Builtin | 0.312 | 0 | 0 | 2.0× faster |
| Reflect | 4.68 | 0 | 0 | 7.5× slower |

## Kind Of

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.938 | 0 | 0 | — |
| Reflect | 2.18 | 0 | 0 | 2.3× slower |

## Is Nil_ptr

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 3.44 | 0 | 0 | — |
| Reflect | 2.50 | 0 | 0 | 1.4× faster |

## Each Field

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 51.3 | 0 | 0 | — |
| Reflect | 157 | 56 | 5 | 3.1× slower |
| ReflectFull | 160 | 56 | 5 | 3.1× slower |
| Reflect2 | 24.9 | 0 | 0 | 2.1× faster |

## Copy Fields

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 284 | 0 | 0 | — |
| Manual | 0.312 | 0 | 0 | 911.9× faster |
| Reflect | 592 | 80 | 10 | 2.1× slower |

## To Map

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 229 | 336 | 2 | — |
| Reflect | 522 | 432 | 12 | 2.3× slower |
| JSON | 2785 | 776 | 25 | 12.2× slower |

## Map For Each

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 954 | 0 | 0 | — |
| Range | 979 | 0 | 0 | 1.0× slower |

## Get_int

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 45.2 | 0 | 0 | — |
| Reflect | 68.0 | 8 | 1 | 1.5× slower |
| ReflectFast | 3.13 | 0 | 0 | 14.4× faster |
| Offset | 11.8 | 0 | 0 | 3.8× faster |
| Accessor | 0.937 | 0 | 0 | 48.3× faster |
| AccFrom | 3.34 | 0 | 0 | 13.5× faster |
| Direct | 0.315 | 0 | 0 | 143.7× faster |

## Set_string

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 45.9 | 0 | 0 | — |
| Reflect | 71.7 | 8 | 1 | 1.6× slower |
| ReflectFast | 5.00 | 0 | 0 | 9.2× faster |
| Offset | 13.8 | 0 | 0 | 3.3× faster |
| Accessor | 1.25 | 0 | 0 | 36.7× faster |
| AccOn | 3.54 | 0 | 0 | 13.0× faster |
| Direct | 0.630 | 0 | 0 | 72.8× faster |

## DI Resolve

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 0.627 | 0 | 0 | — |
| SafeRefl | 152 | 0 | 0 | 242.8× slower |
| Accessor | 3.12 | 0 | 0 | 5.0× slower |
| Reflect2 | 20.9 | 0 | 0 | 33.4× slower |
| Reflect | 252 | 24 | 3 | 402.0× slower |

## JSON Decode

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| StdlibJSON | 2707 | 392 | 10 | — |
| SafeRefl | 523 | 0 | 0 | 5.2× faster |
| Reflect | 1734 | 160 | 20 | 1.6× faster |
| Reflect2 | 81.7 | 0 | 0 | 33.1× faster |
| Accessor | 9.55 | 0 | 0 | 283.5× faster |

## ORM Scan

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 14.2 | 0 | 0 | — |
| SafeRefl | 544 | 0 | 0 | 38.5× slower |
| Accessor | 12.4 | 0 | 0 | 1.1× faster |
| Reflect2 | 82.5 | 0 | 0 | 5.8× slower |
| Reflect | 997 | 80 | 10 | 70.5× slower |
| Copier | 7291 | 880 | 58 | 515.3× slower |

## Struct Copy

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 9.67 | 0 | 0 | — |
| Accessor | 10.5 | 0 | 0 | 1.1× slower |
| Reflect2 | 40.9 | 0 | 0 | 4.2× slower |
| Offset | 184 | 0 | 0 | 19.1× slower |
| Reflect | 782 | 80 | 10 | 80.9× slower |
| SafeRefl | 521 | 0 | 0 | 53.9× slower |
| Copier | 3250 | 552 | 32 | 336.0× slower |

