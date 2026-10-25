# Benchmark Results

**Generated:** 2026-10-25 10:49 UTC  
**Go:** 1.24  
**Platform:** linux/amd64  
**CPU:** AMD EPYC 9V45 96-Core Processor                  

## Field Read

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Reflect | 34.4 | 0 | 0 | — |
| ReflectFast | 1.68 | 0 | 0 | 20.4× faster |
| SafeRefl | 24.9 | 0 | 0 | 1.4× faster |
| Offset | 6.04 | 0 | 0 | 5.7× faster |
| Accessor | 0.448 | 0 | 0 | 76.8× faster |
| Native | 0.234 | 0 | 0 | 146.7× faster |

## Slice At

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.668 | 0 | 0 | — |
| Direct | 0.719 | 0 | 0 | 1.1× slower |
| Reflect | 2.08 | 0 | 0 | 3.1× slower |

## Map Len

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.269 | 0 | 0 | — |
| Builtin | 0.237 | 0 | 0 | 1.1× faster |
| Reflect | 2.51 | 0 | 0 | 9.3× slower |

## Kind Of

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.536 | 0 | 0 | — |
| Reflect | 1.11 | 0 | 0 | 2.1× slower |

## Is Nil_ptr

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 1.47 | 0 | 0 | — |
| Reflect | 1.35 | 0 | 0 | 1.1× faster |

## Each Field

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 23.8 | 0 | 0 | — |
| Reflect | 76.6 | 56 | 5 | 3.2× slower |
| ReflectFull | 77.8 | 56 | 5 | 3.3× slower |
| Reflect2 | 12.8 | 0 | 0 | 1.9× faster |

## Copy Fields

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 147 | 0 | 0 | — |
| Manual | 0.223 | 0 | 0 | 661.1× faster |
| Reflect | 276 | 0 | 0 | 1.9× slower |

## To Map

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 113 | 336 | 2 | — |
| Reflect | 247 | 392 | 7 | 2.2× slower |
| JSON | 1324 | 776 | 25 | 11.7× slower |

## Map For Each

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 448 | 0 | 0 | — |
| Range | 508 | 0 | 0 | 1.1× slower |

## Get_int

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 26.6 | 0 | 0 | — |
| Reflect | 36.6 | 0 | 0 | 1.4× slower |
| ReflectFast | 1.78 | 0 | 0 | 15.0× faster |
| Offset | 6.35 | 0 | 0 | 4.2× faster |
| Accessor | 0.277 | 0 | 0 | 96.1× faster |
| AccFrom | 1.59 | 0 | 0 | 16.7× faster |
| Direct | 0.244 | 0 | 0 | 108.9× faster |

## Set_string

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 25.9 | 0 | 0 | — |
| Reflect | 35.2 | 0 | 0 | 1.4× slower |
| ReflectFast | 2.71 | 0 | 0 | 9.6× faster |
| Offset | 7.21 | 0 | 0 | 3.6× faster |
| Accessor | 0.476 | 0 | 0 | 54.5× faster |
| AccOn | 1.59 | 0 | 0 | 16.3× faster |
| Direct | 0.237 | 0 | 0 | 109.4× faster |

## DI Resolve

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 0.337 | 0 | 0 | — |
| SafeRefl | 74.9 | 0 | 0 | 222.4× slower |
| Accessor | 1.32 | 0 | 0 | 3.9× slower |
| Reflect2 | 11.0 | 0 | 0 | 32.8× slower |
| Reflect | 125 | 0 | 0 | 369.9× slower |

## JSON Decode

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| StdlibJSON | 1279 | 392 | 10 | — |
| SafeRefl | 254 | 0 | 0 | 5.0× faster |
| Reflect | 854 | 0 | 0 | 1.5× faster |
| Reflect2 | 42.7 | 0 | 0 | 30.0× faster |
| Accessor | 3.59 | 0 | 0 | 356.7× faster |

## ORM Scan

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 8.11 | 0 | 0 | — |
| SafeRefl | 263 | 0 | 0 | 32.4× slower |
| Accessor | 7.00 | 0 | 0 | 1.2× faster |
| Reflect2 | 44.0 | 0 | 0 | 5.4× slower |
| Reflect | 512 | 0 | 0 | 63.2× slower |
| Copier | 3592 | 640 | 28 | 442.8× slower |

## Struct Copy

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 4.46 | 0 | 0 | — |
| Accessor | 4.69 | 0 | 0 | 1.1× slower |
| Reflect2 | 21.4 | 0 | 0 | 4.8× slower |
| Offset | 91.6 | 0 | 0 | 20.5× slower |
| Reflect | 387 | 0 | 0 | 86.9× slower |
| SafeRefl | 262 | 0 | 0 | 58.8× slower |
| Copier | 1531 | 432 | 17 | 343.2× slower |

