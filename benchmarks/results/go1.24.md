# Benchmark Results

**Generated:** 2026-08-02 08:23 UTC  
**Go:** 1.24  
**Platform:** linux/amd64  
**CPU:** AMD EPYC 7763 64-Core Processor                  

## Field Read

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Reflect | 60.0 | 0 | 0 | — |
| ReflectFast | 3.12 | 0 | 0 | 19.2× faster |
| SafeRefl | 55.3 | 0 | 0 | 1.1× faster |
| Offset | 10.3 | 0 | 0 | 5.8× faster |
| Accessor | 0.938 | 0 | 0 | 64.0× faster |
| Native | 0.625 | 0 | 0 | 96.1× faster |

## Slice At

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 1.08 | 0 | 0 | — |
| Direct | 0.999 | 0 | 0 | 1.1× faster |
| Reflect | 3.75 | 0 | 0 | 3.5× slower |

## Map Len

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.625 | 0 | 0 | — |
| Builtin | 0.626 | 0 | 0 | 1.0× slower |
| Reflect | 4.69 | 0 | 0 | 7.5× slower |

## Kind Of

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.936 | 0 | 0 | — |
| Reflect | 1.87 | 0 | 0 | 2.0× slower |

## Is Nil_ptr

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 2.81 | 0 | 0 | — |
| Reflect | 2.81 | 0 | 0 | 1.0× slower |

## Each Field

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 42.9 | 0 | 0 | — |
| Reflect | 141 | 56 | 5 | 3.3× slower |
| ReflectFull | 154 | 56 | 5 | 3.6× slower |
| Reflect2 | 23.3 | 0 | 0 | 1.8× faster |

## Copy Fields

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 249 | 0 | 0 | — |
| Manual | 0.313 | 0 | 0 | 794.1× faster |
| Reflect | 490 | 0 | 0 | 2.0× slower |

## To Map

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 216 | 336 | 2 | — |
| Reflect | 447 | 392 | 7 | 2.1× slower |
| JSON | 2636 | 776 | 25 | 12.2× slower |

## Map For Each

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 828 | 0 | 0 | — |
| Range | 853 | 0 | 0 | 1.0× slower |

## Get_int

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 55.2 | 0 | 0 | — |
| Reflect | 59.0 | 0 | 0 | 1.1× slower |
| ReflectFast | 3.12 | 0 | 0 | 17.7× faster |
| Offset | 10.3 | 0 | 0 | 5.4× faster |
| Accessor | 0.627 | 0 | 0 | 88.0× faster |
| AccFrom | 3.12 | 0 | 0 | 17.7× faster |
| Direct | 0.625 | 0 | 0 | 88.3× faster |

## Set_string

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 46.9 | 0 | 0 | — |
| Reflect | 62.6 | 0 | 0 | 1.3× slower |
| ReflectFast | 4.99 | 0 | 0 | 9.4× faster |
| Offset | 12.8 | 0 | 0 | 3.7× faster |
| Accessor | 1.25 | 0 | 0 | 37.5× faster |
| AccOn | 3.49 | 0 | 0 | 13.4× faster |
| Direct | 0.625 | 0 | 0 | 75.0× faster |

## DI Resolve

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 0.628 | 0 | 0 | — |
| SafeRefl | 144 | 0 | 0 | 228.6× slower |
| Accessor | 2.86 | 0 | 0 | 4.6× slower |
| Reflect2 | 19.8 | 0 | 0 | 31.5× slower |
| Reflect | 225 | 0 | 0 | 358.9× slower |

## JSON Decode

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| StdlibJSON | 2838 | 392 | 10 | — |
| SafeRefl | 469 | 0 | 0 | 6.1× faster |
| Reflect | 1525 | 0 | 0 | 1.9× faster |
| Reflect2 | 80.0 | 0 | 0 | 35.5× faster |
| Accessor | 9.79 | 0 | 0 | 289.7× faster |

## ORM Scan

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 14.1 | 0 | 0 | — |
| SafeRefl | 487 | 0 | 0 | 34.5× slower |
| Accessor | 12.2 | 0 | 0 | 1.2× faster |
| Reflect2 | 77.3 | 0 | 0 | 5.5× slower |
| Reflect | 914 | 0 | 0 | 64.8× slower |
| Copier | 6933 | 640 | 28 | 491.3× slower |

## Struct Copy

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 9.69 | 0 | 0 | — |
| Accessor | 8.48 | 0 | 0 | 1.1× faster |
| Reflect2 | 36.4 | 0 | 0 | 3.8× slower |
| Offset | 167 | 0 | 0 | 17.2× slower |
| Reflect | 686 | 0 | 0 | 70.8× slower |
| SafeRefl | 498 | 0 | 0 | 51.4× slower |
| Copier | 3010 | 432 | 17 | 310.6× slower |

