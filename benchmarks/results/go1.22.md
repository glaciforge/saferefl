# Benchmark Results

**Generated:** 2026-09-27 11:29 UTC  
**Go:** 1.22  
**Platform:** linux/amd64  
**CPU:** AMD EPYC 9V74 80-Core Processor                  

## Field Read

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Reflect | 57.3 | 8 | 1 | — |
| ReflectFast | 2.48 | 0 | 0 | 23.1× faster |
| SafeRefl | 32.9 | 0 | 0 | 1.7× faster |
| Offset | 9.02 | 0 | 0 | 6.4× faster |
| Accessor | 0.831 | 0 | 0 | 69.0× faster |
| Native | 0.273 | 0 | 0 | 209.9× faster |

## Slice At

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.901 | 0 | 0 | — |
| Direct | 0.921 | 0 | 0 | 1.0× slower |
| Reflect | 3.01 | 0 | 0 | 3.3× slower |

## Map Len

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.546 | 0 | 0 | — |
| Builtin | 0.275 | 0 | 0 | 2.0× faster |
| Reflect | 3.56 | 0 | 0 | 6.5× slower |

## Kind Of

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.820 | 0 | 0 | — |
| Reflect | 1.64 | 0 | 0 | 2.0× slower |

## Is Nil_ptr

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 2.47 | 0 | 0 | — |
| Reflect | 2.19 | 0 | 0 | 1.1× faster |

## Each Field

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 41.3 | 0 | 0 | — |
| Reflect | 122 | 56 | 5 | 3.0× slower |
| ReflectFull | 124 | 56 | 5 | 3.0× slower |
| Reflect2 | 20.8 | 0 | 0 | 2.0× faster |

## Copy Fields

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 205 | 0 | 0 | — |
| Manual | 0.277 | 0 | 0 | 739.6× faster |
| Reflect | 487 | 80 | 10 | 2.4× slower |

## To Map

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 170 | 336 | 2 | — |
| Reflect | 384 | 432 | 12 | 2.3× slower |
| JSON | 1911 | 776 | 25 | 11.2× slower |

## Map For Each

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 693 | 0 | 0 | — |
| Range | 714 | 0 | 0 | 1.0× slower |

## Get_int

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 33.3 | 0 | 0 | — |
| Reflect | 57.1 | 8 | 1 | 1.7× slower |
| ReflectFast | 2.47 | 0 | 0 | 13.5× faster |
| Offset | 9.12 | 0 | 0 | 3.6× faster |
| Accessor | 0.820 | 0 | 0 | 40.6× faster |
| AccFrom | 2.19 | 0 | 0 | 15.2× faster |
| Direct | 0.273 | 0 | 0 | 121.9× faster |

## Set_string

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 33.6 | 0 | 0 | — |
| Reflect | 60.9 | 8 | 1 | 1.8× slower |
| ReflectFast | 3.83 | 0 | 0 | 8.8× faster |
| Offset | 10.6 | 0 | 0 | 3.2× faster |
| Accessor | 1.09 | 0 | 0 | 30.8× faster |
| AccOn | 2.46 | 0 | 0 | 13.7× faster |
| Direct | 0.552 | 0 | 0 | 60.9× faster |

## DI Resolve

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 0.557 | 0 | 0 | — |
| SafeRefl | 111 | 0 | 0 | 199.6× slower |
| Accessor | 2.73 | 0 | 0 | 4.9× slower |
| Reflect2 | 16.6 | 0 | 0 | 29.9× slower |
| Reflect | 200 | 24 | 3 | 358.3× slower |

## JSON Decode

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| StdlibJSON | 1890 | 392 | 10 | — |
| SafeRefl | 387 | 0 | 0 | 4.9× faster |
| Reflect | 1429 | 160 | 20 | 1.3× faster |
| Reflect2 | 68.0 | 0 | 0 | 27.8× faster |
| Accessor | 6.10 | 0 | 0 | 310.1× faster |

## ORM Scan

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 11.1 | 0 | 0 | — |
| SafeRefl | 391 | 0 | 0 | 35.3× slower |
| Accessor | 10.2 | 0 | 0 | 1.1× faster |
| Reflect2 | 65.6 | 0 | 0 | 5.9× slower |
| Reflect | 788 | 80 | 10 | 71.3× slower |
| Copier | 5182 | 880 | 58 | 468.9× slower |

## Struct Copy

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 7.19 | 0 | 0 | — |
| Accessor | 7.85 | 0 | 0 | 1.1× slower |
| Reflect2 | 33.4 | 0 | 0 | 4.6× slower |
| Offset | 145 | 0 | 0 | 20.2× slower |
| Reflect | 657 | 80 | 10 | 91.4× slower |
| SafeRefl | 373 | 0 | 0 | 51.9× slower |
| Copier | 2399 | 552 | 32 | 333.7× slower |

