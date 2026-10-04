# Benchmark Results

**Generated:** 2026-10-04 11:50 UTC  
**Go:** 1.24  
**Platform:** linux/amd64  
**CPU:** AMD EPYC 9V74 80-Core Processor                  

## Field Read

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Reflect | 49.8 | 0 | 0 | — |
| ReflectFast | 2.50 | 0 | 0 | 19.9× faster |
| SafeRefl | 35.5 | 0 | 0 | 1.4× faster |
| Offset | 8.05 | 0 | 0 | 6.2× faster |
| Accessor | 0.823 | 0 | 0 | 60.5× faster |
| Native | 0.548 | 0 | 0 | 90.9× faster |

## Slice At

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.903 | 0 | 0 | — |
| Direct | 0.920 | 0 | 0 | 1.0× slower |
| Reflect | 3.01 | 0 | 0 | 3.3× slower |

## Map Len

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.547 | 0 | 0 | — |
| Builtin | 0.546 | 0 | 0 | 1.0× faster |
| Reflect | 3.83 | 0 | 0 | 7.0× slower |

## Kind Of

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.819 | 0 | 0 | — |
| Reflect | 1.64 | 0 | 0 | 2.0× slower |

## Is Nil_ptr

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 2.08 | 0 | 0 | — |
| Reflect | 2.46 | 0 | 0 | 1.2× slower |

## Each Field

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 33.6 | 0 | 0 | — |
| Reflect | 105 | 56 | 5 | 3.1× slower |
| ReflectFull | 109 | 56 | 5 | 3.2× slower |
| Reflect2 | 19.4 | 0 | 0 | 1.7× faster |

## Copy Fields

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 190 | 0 | 0 | — |
| Manual | 0.274 | 0 | 0 | 693.6× faster |
| Reflect | 418 | 0 | 0 | 2.2× slower |

## To Map

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 152 | 336 | 2 | — |
| Reflect | 339 | 392 | 7 | 2.2× slower |
| JSON | 1797 | 776 | 25 | 11.8× slower |

## Map For Each

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 590 | 0 | 0 | — |
| Range | 600 | 0 | 0 | 1.0× slower |

## Get_int

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 35.1 | 0 | 0 | — |
| Reflect | 49.9 | 0 | 0 | 1.4× slower |
| ReflectFast | 2.48 | 0 | 0 | 14.2× faster |
| Offset | 8.03 | 0 | 0 | 4.4× faster |
| Accessor | 0.547 | 0 | 0 | 64.2× faster |
| AccFrom | 2.19 | 0 | 0 | 16.1× faster |
| Direct | 0.552 | 0 | 0 | 63.5× faster |

## Set_string

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 36.7 | 0 | 0 | — |
| Reflect | 53.1 | 0 | 0 | 1.4× slower |
| ReflectFast | 3.83 | 0 | 0 | 9.6× faster |
| Offset | 9.96 | 0 | 0 | 3.7× faster |
| Accessor | 1.09 | 0 | 0 | 33.5× faster |
| AccOn | 2.46 | 0 | 0 | 14.9× faster |
| Direct | 0.550 | 0 | 0 | 66.6× faster |

## DI Resolve

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 0.560 | 0 | 0 | — |
| SafeRefl | 110 | 0 | 0 | 196.5× slower |
| Accessor | 2.47 | 0 | 0 | 4.4× slower |
| Reflect2 | 16.8 | 0 | 0 | 30.0× slower |
| Reflect | 184 | 0 | 0 | 328.2× slower |

## JSON Decode

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| StdlibJSON | 1836 | 392 | 10 | — |
| SafeRefl | 373 | 0 | 0 | 4.9× faster |
| Reflect | 1276 | 0 | 0 | 1.4× faster |
| Reflect2 | 64.7 | 0 | 0 | 28.4× faster |
| Accessor | 6.29 | 0 | 0 | 292.0× faster |

## ORM Scan

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 11.1 | 0 | 0 | — |
| SafeRefl | 371 | 0 | 0 | 33.5× slower |
| Accessor | 9.97 | 0 | 0 | 1.1× faster |
| Reflect2 | 65.7 | 0 | 0 | 5.9× slower |
| Reflect | 726 | 0 | 0 | 65.7× slower |
| Copier | 4806 | 640 | 28 | 434.5× slower |

## Struct Copy

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 7.23 | 0 | 0 | — |
| Accessor | 7.85 | 0 | 0 | 1.1× slower |
| Reflect2 | 29.6 | 0 | 0 | 4.1× slower |
| Offset | 125 | 0 | 0 | 17.3× slower |
| Reflect | 574 | 0 | 0 | 79.4× slower |
| SafeRefl | 379 | 0 | 0 | 52.4× slower |
| Copier | 2090 | 432 | 17 | 288.9× slower |

