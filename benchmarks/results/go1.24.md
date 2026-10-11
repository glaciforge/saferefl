# Benchmark Results

**Generated:** 2026-10-11 12:11 UTC  
**Go:** 1.24  
**Platform:** linux/amd64  
**CPU:** AMD EPYC 9V45 96-Core Processor                  

## Field Read

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Reflect | 34.9 | 0 | 0 | — |
| ReflectFast | 1.74 | 0 | 0 | 20.0× faster |
| SafeRefl | 24.9 | 0 | 0 | 1.4× faster |
| Offset | 6.14 | 0 | 0 | 5.7× faster |
| Accessor | 0.449 | 0 | 0 | 77.8× faster |
| Native | 0.247 | 0 | 0 | 141.4× faster |

## Slice At

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.677 | 0 | 0 | — |
| Direct | 0.720 | 0 | 0 | 1.1× slower |
| Reflect | 1.99 | 0 | 0 | 2.9× slower |

## Map Len

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.276 | 0 | 0 | — |
| Builtin | 0.235 | 0 | 0 | 1.2× faster |
| Reflect | 2.54 | 0 | 0 | 9.2× slower |

## Kind Of

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.543 | 0 | 0 | — |
| Reflect | 1.17 | 0 | 0 | 2.2× slower |

## Is Nil_ptr

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 1.46 | 0 | 0 | — |
| Reflect | 1.34 | 0 | 0 | 1.1× faster |

## Each Field

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 23.9 | 0 | 0 | — |
| Reflect | 76.4 | 56 | 5 | 3.2× slower |
| ReflectFull | 78.4 | 56 | 5 | 3.3× slower |
| Reflect2 | 12.9 | 0 | 0 | 1.9× faster |

## Copy Fields

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 148 | 0 | 0 | — |
| Manual | 0.222 | 0 | 0 | 666.7× faster |
| Reflect | 277 | 0 | 0 | 1.9× slower |

## To Map

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 113 | 336 | 2 | — |
| Reflect | 244 | 392 | 7 | 2.2× slower |
| JSON | 1322 | 776 | 25 | 11.7× slower |

## Map For Each

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 463 | 0 | 0 | — |
| Range | 473 | 0 | 0 | 1.0× slower |

## Get_int

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 25.2 | 0 | 0 | — |
| Reflect | 34.9 | 0 | 0 | 1.4× slower |
| ReflectFast | 1.71 | 0 | 0 | 14.7× faster |
| Offset | 6.14 | 0 | 0 | 4.1× faster |
| Accessor | 0.277 | 0 | 0 | 91.1× faster |
| AccFrom | 1.62 | 0 | 0 | 15.6× faster |
| Direct | 0.231 | 0 | 0 | 109.0× faster |

## Set_string

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 26.0 | 0 | 0 | — |
| Reflect | 34.5 | 0 | 0 | 1.3× slower |
| ReflectFast | 2.72 | 0 | 0 | 9.5× faster |
| Offset | 7.21 | 0 | 0 | 3.6× faster |
| Accessor | 0.482 | 0 | 0 | 53.9× faster |
| AccOn | 1.62 | 0 | 0 | 16.0× faster |
| Direct | 0.232 | 0 | 0 | 111.7× faster |

## DI Resolve

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 0.340 | 0 | 0 | — |
| SafeRefl | 76.3 | 0 | 0 | 224.3× slower |
| Accessor | 1.35 | 0 | 0 | 4.0× slower |
| Reflect2 | 11.1 | 0 | 0 | 32.5× slower |
| Reflect | 129 | 0 | 0 | 380.7× slower |

## JSON Decode

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| StdlibJSON | 1336 | 392 | 10 | — |
| SafeRefl | 260 | 0 | 0 | 5.1× faster |
| Reflect | 862 | 0 | 0 | 1.5× faster |
| Reflect2 | 44.0 | 0 | 0 | 30.4× faster |
| Accessor | 3.54 | 0 | 0 | 377.1× faster |

## ORM Scan

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 8.12 | 0 | 0 | — |
| SafeRefl | 270 | 0 | 0 | 33.3× slower |
| Accessor | 7.03 | 0 | 0 | 1.2× faster |
| Reflect2 | 44.2 | 0 | 0 | 5.4× slower |
| Reflect | 513 | 0 | 0 | 63.2× slower |
| Copier | 3596 | 640 | 28 | 442.7× slower |

## Struct Copy

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 4.50 | 0 | 0 | — |
| Accessor | 4.85 | 0 | 0 | 1.1× slower |
| Reflect2 | 22.0 | 0 | 0 | 4.9× slower |
| Offset | 93.6 | 0 | 0 | 20.8× slower |
| Reflect | 399 | 0 | 0 | 88.7× slower |
| SafeRefl | 286 | 0 | 0 | 63.6× slower |
| Copier | 1579 | 432 | 17 | 351.0× slower |

