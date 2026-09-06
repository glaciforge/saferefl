# Benchmark Results

**Generated:** 2026-09-06 10:21 UTC  
**Go:** 1.22  
**Platform:** linux/amd64  
**CPU:** AMD EPYC 9V74 80-Core Processor                  

## Field Read

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Reflect | 57.8 | 8 | 1 | — |
| ReflectFast | 2.50 | 0 | 0 | 23.1× faster |
| SafeRefl | 33.3 | 0 | 0 | 1.7× faster |
| Offset | 9.09 | 0 | 0 | 6.4× faster |
| Accessor | 0.936 | 0 | 0 | 61.7× faster |
| Native | 0.275 | 0 | 0 | 210.5× faster |

## Slice At

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.904 | 0 | 0 | — |
| Direct | 0.921 | 0 | 0 | 1.0× slower |
| Reflect | 3.02 | 0 | 0 | 3.3× slower |

## Map Len

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.546 | 0 | 0 | — |
| Builtin | 0.275 | 0 | 0 | 2.0× faster |
| Reflect | 3.56 | 0 | 0 | 6.5× slower |

## Kind Of

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.819 | 0 | 0 | — |
| Reflect | 1.64 | 0 | 0 | 2.0× slower |

## Is Nil_ptr

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 2.46 | 0 | 0 | — |
| Reflect | 2.19 | 0 | 0 | 1.1× faster |

## Each Field

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 40.9 | 0 | 0 | — |
| Reflect | 122 | 56 | 5 | 3.0× slower |
| ReflectFull | 124 | 56 | 5 | 3.0× slower |
| Reflect2 | 20.8 | 0 | 0 | 2.0× faster |

## Copy Fields

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 208 | 0 | 0 | — |
| Manual | 0.274 | 0 | 0 | 758.3× faster |
| Reflect | 487 | 80 | 10 | 2.3× slower |

## To Map

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 175 | 336 | 2 | — |
| Reflect | 390 | 432 | 12 | 2.2× slower |
| JSON | 1931 | 776 | 25 | 11.0× slower |

## Map For Each

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 693 | 0 | 0 | — |
| Range | 719 | 0 | 0 | 1.0× slower |

## Get_int

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 33.1 | 0 | 0 | — |
| Reflect | 57.4 | 8 | 1 | 1.7× slower |
| ReflectFast | 2.47 | 0 | 0 | 13.4× faster |
| Offset | 9.25 | 0 | 0 | 3.6× faster |
| Accessor | 0.819 | 0 | 0 | 40.4× faster |
| AccFrom | 2.60 | 0 | 0 | 12.7× faster |
| Direct | 0.273 | 0 | 0 | 121.1× faster |

## Set_string

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 33.6 | 0 | 0 | — |
| Reflect | 60.9 | 8 | 1 | 1.8× slower |
| ReflectFast | 3.82 | 0 | 0 | 8.8× faster |
| Offset | 10.6 | 0 | 0 | 3.2× faster |
| Accessor | 1.09 | 0 | 0 | 30.7× faster |
| AccOn | 2.76 | 0 | 0 | 12.2× faster |
| Direct | 0.546 | 0 | 0 | 61.5× faster |

## DI Resolve

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 0.572 | 0 | 0 | — |
| SafeRefl | 110 | 0 | 0 | 191.6× slower |
| Accessor | 2.75 | 0 | 0 | 4.8× slower |
| Reflect2 | 17.0 | 0 | 0 | 29.7× slower |
| Reflect | 201 | 24 | 3 | 351.1× slower |

## JSON Decode

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| StdlibJSON | 1901 | 392 | 10 | — |
| SafeRefl | 380 | 0 | 0 | 5.0× faster |
| Reflect | 1430 | 160 | 20 | 1.3× faster |
| Reflect2 | 66.3 | 0 | 0 | 28.7× faster |
| Accessor | 6.10 | 0 | 0 | 311.7× faster |

## ORM Scan

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 11.1 | 0 | 0 | — |
| SafeRefl | 400 | 0 | 0 | 36.1× slower |
| Accessor | 11.7 | 0 | 0 | 1.1× slower |
| Reflect2 | 66.1 | 0 | 0 | 6.0× slower |
| Reflect | 789 | 80 | 10 | 71.3× slower |
| Copier | 5219 | 880 | 58 | 471.7× slower |

## Struct Copy

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 7.21 | 0 | 0 | — |
| Accessor | 7.83 | 0 | 0 | 1.1× slower |
| Reflect2 | 33.7 | 0 | 0 | 4.7× slower |
| Offset | 148 | 0 | 0 | 20.5× slower |
| Reflect | 653 | 80 | 10 | 90.5× slower |
| SafeRefl | 372 | 0 | 0 | 51.6× slower |
| Copier | 2388 | 552 | 32 | 331.2× slower |

