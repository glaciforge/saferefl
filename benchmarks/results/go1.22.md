# Benchmark Results

**Generated:** 2026-08-30 11:21 UTC  
**Go:** 1.22  
**Platform:** linux/amd64  
**CPU:** AMD EPYC 9V45 96-Core Processor                  

## Field Read

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Reflect | 38.4 | 8 | 1 | — |
| ReflectFast | 1.72 | 0 | 0 | 22.3× faster |
| SafeRefl | 24.0 | 0 | 0 | 1.6× faster |
| Offset | 6.95 | 0 | 0 | 5.5× faster |
| Accessor | 0.466 | 0 | 0 | 82.3× faster |
| Native | 0.235 | 0 | 0 | 163.1× faster |

## Slice At

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.682 | 0 | 0 | — |
| Direct | 0.746 | 0 | 0 | 1.1× slower |
| Reflect | 2.01 | 0 | 0 | 2.9× slower |

## Map Len

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.310 | 0 | 0 | — |
| Builtin | 0.232 | 0 | 0 | 1.3× faster |
| Reflect | 2.79 | 0 | 0 | 9.0× slower |

## Kind Of

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.559 | 0 | 0 | — |
| Reflect | 1.28 | 0 | 0 | 2.3× slower |

## Is Nil_ptr

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 1.85 | 0 | 0 | — |
| Reflect | 1.38 | 0 | 0 | 1.3× faster |

## Each Field

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 26.6 | 0 | 0 | — |
| Reflect | 85.5 | 56 | 5 | 3.2× slower |
| ReflectFull | 87.6 | 56 | 5 | 3.3× slower |
| Reflect2 | 14.2 | 0 | 0 | 1.9× faster |

## Copy Fields

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 167 | 0 | 0 | — |
| Manual | 0.231 | 0 | 0 | 721.7× faster |
| Reflect | 341 | 80 | 10 | 2.0× slower |

## To Map

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 118 | 336 | 2 | — |
| Reflect | 269 | 432 | 12 | 2.3× slower |
| JSON | 1394 | 776 | 25 | 11.8× slower |

## Map For Each

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 519 | 0 | 0 | — |
| Range | 555 | 0 | 0 | 1.1× slower |

## Get_int

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 24.3 | 0 | 0 | — |
| Reflect | 39.3 | 8 | 1 | 1.6× slower |
| ReflectFast | 2.06 | 0 | 0 | 11.8× faster |
| Offset | 7.06 | 0 | 0 | 3.4× faster |
| Accessor | 0.466 | 0 | 0 | 52.2× faster |
| AccFrom | 1.65 | 0 | 0 | 14.8× faster |
| Direct | 0.237 | 0 | 0 | 102.6× faster |

## Set_string

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 24.6 | 0 | 0 | — |
| Reflect | 41.6 | 8 | 1 | 1.7× slower |
| ReflectFast | 2.83 | 0 | 0 | 8.7× faster |
| Offset | 8.22 | 0 | 0 | 3.0× faster |
| Accessor | 0.499 | 0 | 0 | 49.4× faster |
| AccOn | 1.64 | 0 | 0 | 15.0× faster |
| Direct | 0.242 | 0 | 0 | 101.9× faster |

## DI Resolve

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 0.349 | 0 | 0 | — |
| SafeRefl | 79.7 | 0 | 0 | 228.0× slower |
| Accessor | 1.73 | 0 | 0 | 4.9× slower |
| Reflect2 | 11.7 | 0 | 0 | 33.4× slower |
| Reflect | 141 | 24 | 3 | 402.1× slower |

## JSON Decode

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| StdlibJSON | 1329 | 392 | 10 | — |
| SafeRefl | 266 | 0 | 0 | 5.0× faster |
| Reflect | 969 | 160 | 20 | 1.4× faster |
| Reflect2 | 42.8 | 0 | 0 | 31.0× faster |
| Accessor | 3.59 | 0 | 0 | 370.0× faster |

## ORM Scan

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 8.32 | 0 | 0 | — |
| SafeRefl | 275 | 0 | 0 | 33.0× slower |
| Accessor | 7.09 | 0 | 0 | 1.2× faster |
| Reflect2 | 47.0 | 0 | 0 | 5.7× slower |
| Reflect | 612 | 80 | 10 | 73.6× slower |
| Copier | 3797 | 880 | 58 | 456.4× slower |

## Struct Copy

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 4.55 | 0 | 0 | — |
| Accessor | 4.77 | 0 | 0 | 1.0× slower |
| Reflect2 | 21.5 | 0 | 0 | 4.7× slower |
| Offset | 99.9 | 0 | 0 | 21.9× slower |
| Reflect | 439 | 80 | 10 | 96.5× slower |
| SafeRefl | 259 | 0 | 0 | 56.8× slower |
| Copier | 1710 | 552 | 32 | 375.5× slower |

