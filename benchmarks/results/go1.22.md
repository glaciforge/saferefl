# Benchmark Results

**Generated:** 2026-07-26 08:26 UTC  
**Go:** 1.22  
**Platform:** linux/amd64  
**CPU:** AMD EPYC 7763 64-Core Processor                  

## Field Read

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Reflect | 68.4 | 8 | 1 | — |
| ReflectFast | 3.18 | 0 | 0 | 21.5× faster |
| SafeRefl | 45.2 | 0 | 0 | 1.5× faster |
| Offset | 11.6 | 0 | 0 | 5.9× faster |
| Accessor | 0.938 | 0 | 0 | 72.9× faster |
| Native | 0.312 | 0 | 0 | 219.1× faster |

## Slice At

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 1.01 | 0 | 0 | — |
| Direct | 0.997 | 0 | 0 | 1.0× faster |
| Reflect | 3.74 | 0 | 0 | 3.7× slower |

## Map Len

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.625 | 0 | 0 | — |
| Builtin | 0.313 | 0 | 0 | 2.0× faster |
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
| Manual | 0.312 | 0 | 0 | 911.0× faster |
| Reflect | 592 | 80 | 10 | 2.1× slower |

## To Map

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 226 | 336 | 2 | — |
| Reflect | 516 | 432 | 12 | 2.3× slower |
| JSON | 2802 | 776 | 25 | 12.4× slower |

## Map For Each

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 951 | 0 | 0 | — |
| Range | 983 | 0 | 0 | 1.0× slower |

## Get_int

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 45.3 | 0 | 0 | — |
| Reflect | 67.8 | 8 | 1 | 1.5× slower |
| ReflectFast | 3.12 | 0 | 0 | 14.5× faster |
| Offset | 11.6 | 0 | 0 | 3.9× faster |
| Accessor | 0.936 | 0 | 0 | 48.4× faster |
| AccFrom | 3.12 | 0 | 0 | 14.5× faster |
| Direct | 0.312 | 0 | 0 | 145.0× faster |

## Set_string

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 45.9 | 0 | 0 | — |
| Reflect | 71.8 | 8 | 1 | 1.6× slower |
| ReflectFast | 4.99 | 0 | 0 | 9.2× faster |
| Offset | 13.7 | 0 | 0 | 3.3× faster |
| Accessor | 1.25 | 0 | 0 | 36.8× faster |
| AccOn | 3.43 | 0 | 0 | 13.4× faster |
| Direct | 0.624 | 0 | 0 | 73.6× faster |

## DI Resolve

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 0.633 | 0 | 0 | — |
| SafeRefl | 155 | 0 | 0 | 244.4× slower |
| Accessor | 3.14 | 0 | 0 | 5.0× slower |
| Reflect2 | 21.5 | 0 | 0 | 34.0× slower |
| Reflect | 242 | 24 | 3 | 383.3× slower |

## JSON Decode

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| StdlibJSON | 2680 | 392 | 10 | — |
| SafeRefl | 527 | 0 | 0 | 5.1× faster |
| Reflect | 1732 | 160 | 20 | 1.5× faster |
| Reflect2 | 79.5 | 0 | 0 | 33.7× faster |
| Accessor | 9.55 | 0 | 0 | 280.7× faster |

## ORM Scan

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 14.1 | 0 | 0 | — |
| SafeRefl | 539 | 0 | 0 | 38.3× slower |
| Accessor | 12.3 | 0 | 0 | 1.1× faster |
| Reflect2 | 83.6 | 0 | 0 | 5.9× slower |
| Reflect | 986 | 80 | 10 | 69.9× slower |
| Copier | 7261 | 880 | 58 | 514.9× slower |

## Struct Copy

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 9.67 | 0 | 0 | — |
| Accessor | 10.5 | 0 | 0 | 1.1× slower |
| Reflect2 | 41.0 | 0 | 0 | 4.2× slower |
| Offset | 185 | 0 | 0 | 19.2× slower |
| Reflect | 781 | 80 | 10 | 80.8× slower |
| SafeRefl | 519 | 0 | 0 | 53.7× slower |
| Copier | 3246 | 552 | 32 | 335.8× slower |

