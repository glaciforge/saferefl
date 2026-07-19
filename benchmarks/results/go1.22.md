# Benchmark Results

**Generated:** 2026-07-19 08:17 UTC  
**Go:** 1.22  
**Platform:** linux/amd64  
**CPU:** AMD EPYC 9V74 80-Core Processor                  

## Field Read

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Reflect | 57.8 | 8 | 1 | — |
| ReflectFast | 2.49 | 0 | 0 | 23.2× faster |
| SafeRefl | 32.8 | 0 | 0 | 1.8× faster |
| Offset | 9.13 | 0 | 0 | 6.3× faster |
| Accessor | 0.822 | 0 | 0 | 70.3× faster |
| Native | 0.273 | 0 | 0 | 211.5× faster |

## Slice At

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.902 | 0 | 0 | — |
| Direct | 0.920 | 0 | 0 | 1.0× slower |
| Reflect | 3.01 | 0 | 0 | 3.3× slower |

## Map Len

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.547 | 0 | 0 | — |
| Builtin | 0.274 | 0 | 0 | 2.0× faster |
| Reflect | 3.56 | 0 | 0 | 6.5× slower |

## Kind Of

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.820 | 0 | 0 | — |
| Reflect | 1.64 | 0 | 0 | 2.0× slower |

## Is Nil_ptr

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 2.46 | 0 | 0 | — |
| Reflect | 2.19 | 0 | 0 | 1.1× faster |

## Each Field

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 41.0 | 0 | 0 | — |
| Reflect | 122 | 56 | 5 | 3.0× slower |
| ReflectFull | 124 | 56 | 5 | 3.0× slower |
| Reflect2 | 20.8 | 0 | 0 | 2.0× faster |

## Copy Fields

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 209 | 0 | 0 | — |
| Manual | 0.274 | 0 | 0 | 761.9× faster |
| Reflect | 490 | 80 | 10 | 2.3× slower |

## To Map

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 171 | 336 | 2 | — |
| Reflect | 388 | 432 | 12 | 2.3× slower |
| JSON | 1964 | 776 | 25 | 11.5× slower |

## Map For Each

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 689 | 0 | 0 | — |
| Range | 723 | 0 | 0 | 1.0× slower |

## Get_int

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 32.7 | 0 | 0 | — |
| Reflect | 57.4 | 8 | 1 | 1.8× slower |
| ReflectFast | 2.48 | 0 | 0 | 13.2× faster |
| Offset | 9.33 | 0 | 0 | 3.5× faster |
| Accessor | 0.822 | 0 | 0 | 39.7× faster |
| AccFrom | 2.19 | 0 | 0 | 14.9× faster |
| Direct | 0.273 | 0 | 0 | 119.7× faster |

## Set_string

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 33.3 | 0 | 0 | — |
| Reflect | 61.0 | 8 | 1 | 1.8× slower |
| ReflectFast | 3.82 | 0 | 0 | 8.7× faster |
| Offset | 10.6 | 0 | 0 | 3.1× faster |
| Accessor | 1.09 | 0 | 0 | 30.5× faster |
| AccOn | 2.46 | 0 | 0 | 13.5× faster |
| Direct | 0.546 | 0 | 0 | 61.0× faster |

## DI Resolve

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 0.555 | 0 | 0 | — |
| SafeRefl | 110 | 0 | 0 | 199.2× slower |
| Accessor | 2.75 | 0 | 0 | 5.0× slower |
| Reflect2 | 17.2 | 0 | 0 | 30.9× slower |
| Reflect | 201 | 24 | 3 | 361.7× slower |

## JSON Decode

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| StdlibJSON | 1901 | 392 | 10 | — |
| SafeRefl | 386 | 0 | 0 | 4.9× faster |
| Reflect | 1445 | 160 | 20 | 1.3× faster |
| Reflect2 | 68.4 | 0 | 0 | 27.8× faster |
| Accessor | 6.08 | 0 | 0 | 312.6× faster |

## ORM Scan

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 11.1 | 0 | 0 | — |
| SafeRefl | 395 | 0 | 0 | 35.7× slower |
| Accessor | 10.1 | 0 | 0 | 1.1× faster |
| Reflect2 | 65.9 | 0 | 0 | 6.0× slower |
| Reflect | 794 | 80 | 10 | 71.9× slower |
| Copier | 5174 | 880 | 58 | 468.3× slower |

## Struct Copy

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 7.20 | 0 | 0 | — |
| Accessor | 7.82 | 0 | 0 | 1.1× slower |
| Reflect2 | 34.0 | 0 | 0 | 4.7× slower |
| Offset | 145 | 0 | 0 | 20.2× slower |
| Reflect | 652 | 80 | 10 | 90.6× slower |
| SafeRefl | 370 | 0 | 0 | 51.5× slower |
| Copier | 2322 | 552 | 32 | 322.7× slower |

