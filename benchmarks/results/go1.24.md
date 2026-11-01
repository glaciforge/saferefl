# Benchmark Results

**Generated:** 2026-11-01 12:44 UTC  
**Go:** 1.24  
**Platform:** linux/amd64  
**CPU:** AMD EPYC 9V74 80-Core Processor                  

## Field Read

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Reflect | 50.0 | 0 | 0 | — |
| ReflectFast | 2.48 | 0 | 0 | 20.2× faster |
| SafeRefl | 35.1 | 0 | 0 | 1.4× faster |
| Offset | 8.04 | 0 | 0 | 6.2× faster |
| Accessor | 0.821 | 0 | 0 | 60.9× faster |
| Native | 0.547 | 0 | 0 | 91.4× faster |

## Slice At

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.903 | 0 | 0 | — |
| Direct | 0.921 | 0 | 0 | 1.0× slower |
| Reflect | 3.01 | 0 | 0 | 3.3× slower |

## Map Len

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.548 | 0 | 0 | — |
| Builtin | 0.548 | 0 | 0 | 1.0× slower |
| Reflect | 3.83 | 0 | 0 | 7.0× slower |

## Kind Of

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.820 | 0 | 0 | — |
| Reflect | 1.64 | 0 | 0 | 2.0× slower |

## Is Nil_ptr

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 1.97 | 0 | 0 | — |
| Reflect | 2.46 | 0 | 0 | 1.2× slower |

## Each Field

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 33.8 | 0 | 0 | — |
| Reflect | 105 | 56 | 5 | 3.1× slower |
| ReflectFull | 108 | 56 | 5 | 3.2× slower |
| Reflect2 | 19.5 | 0 | 0 | 1.7× faster |

## Copy Fields

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 192 | 0 | 0 | — |
| Manual | 0.273 | 0 | 0 | 701.1× faster |
| Reflect | 411 | 0 | 0 | 2.1× slower |

## To Map

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 153 | 336 | 2 | — |
| Reflect | 343 | 392 | 7 | 2.2× slower |
| JSON | 1797 | 776 | 25 | 11.8× slower |

## Map For Each

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 588 | 0 | 0 | — |
| Range | 604 | 0 | 0 | 1.0× slower |

## Get_int

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 35.0 | 0 | 0 | — |
| Reflect | 49.7 | 0 | 0 | 1.4× slower |
| ReflectFast | 2.47 | 0 | 0 | 14.2× faster |
| Offset | 8.00 | 0 | 0 | 4.4× faster |
| Accessor | 0.550 | 0 | 0 | 63.6× faster |
| AccFrom | 2.19 | 0 | 0 | 16.0× faster |
| Direct | 0.547 | 0 | 0 | 63.9× faster |

## Set_string

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 36.0 | 0 | 0 | — |
| Reflect | 53.1 | 0 | 0 | 1.5× slower |
| ReflectFast | 3.83 | 0 | 0 | 9.4× faster |
| Offset | 10.1 | 0 | 0 | 3.6× faster |
| Accessor | 1.10 | 0 | 0 | 32.8× faster |
| AccOn | 2.46 | 0 | 0 | 14.6× faster |
| Direct | 0.547 | 0 | 0 | 65.9× faster |

## DI Resolve

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 0.559 | 0 | 0 | — |
| SafeRefl | 111 | 0 | 0 | 198.0× slower |
| Accessor | 2.48 | 0 | 0 | 4.4× slower |
| Reflect2 | 16.4 | 0 | 0 | 29.3× slower |
| Reflect | 183 | 0 | 0 | 327.5× slower |

## JSON Decode

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| StdlibJSON | 1835 | 392 | 10 | — |
| SafeRefl | 364 | 0 | 0 | 5.0× faster |
| Reflect | 1274 | 0 | 0 | 1.4× faster |
| Reflect2 | 64.0 | 0 | 0 | 28.7× faster |
| Accessor | 6.29 | 0 | 0 | 291.8× faster |

## ORM Scan

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 11.1 | 0 | 0 | — |
| SafeRefl | 385 | 0 | 0 | 34.7× slower |
| Accessor | 10.0 | 0 | 0 | 1.1× faster |
| Reflect2 | 64.7 | 0 | 0 | 5.8× slower |
| Reflect | 728 | 0 | 0 | 65.6× slower |
| Copier | 4804 | 640 | 28 | 433.1× slower |

## Struct Copy

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 7.26 | 0 | 0 | — |
| Accessor | 7.84 | 0 | 0 | 1.1× slower |
| Reflect2 | 29.4 | 0 | 0 | 4.0× slower |
| Offset | 125 | 0 | 0 | 17.2× slower |
| Reflect | 575 | 0 | 0 | 79.1× slower |
| SafeRefl | 382 | 0 | 0 | 52.6× slower |
| Copier | 2085 | 432 | 17 | 287.1× slower |

