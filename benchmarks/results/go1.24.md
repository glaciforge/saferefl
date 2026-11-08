# Benchmark Results

**Generated:** 2026-11-08 12:50 UTC  
**Go:** 1.24  
**Platform:** linux/amd64  
**CPU:** Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz  

## Field Read

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Reflect | 46.8 | 0 | 0 | — |
| ReflectFast | 2.90 | 0 | 0 | 16.2× faster |
| SafeRefl | 40.3 | 0 | 0 | 1.2× faster |
| Offset | 8.72 | 0 | 0 | 5.4× faster |
| Accessor | 0.875 | 0 | 0 | 53.5× faster |
| Native | 0.586 | 0 | 0 | 79.8× faster |

## Slice At

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 1.16 | 0 | 0 | — |
| Direct | 1.16 | 0 | 0 | 1.0× slower |
| Reflect | 3.56 | 0 | 0 | 3.1× slower |

## Map Len

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.580 | 0 | 0 | — |
| Builtin | 0.580 | 0 | 0 | 1.0× faster |
| Reflect | 3.21 | 0 | 0 | 5.5× slower |

## Kind Of

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.753 | 0 | 0 | — |
| Reflect | 1.45 | 0 | 0 | 1.9× slower |

## Is Nil_ptr

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 2.13 | 0 | 0 | — |
| Reflect | 2.63 | 0 | 0 | 1.2× slower |

## Each Field

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 38.1 | 0 | 0 | — |
| Reflect | 135 | 56 | 5 | 3.5× slower |
| ReflectFull | 141 | 56 | 5 | 3.7× slower |
| Reflect2 | 22.1 | 0 | 0 | 1.7× faster |

## Copy Fields

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 206 | 0 | 0 | — |
| Manual | 0.290 | 0 | 0 | 708.2× faster |
| Reflect | 462 | 0 | 0 | 2.2× slower |

## To Map

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 224 | 336 | 2 | — |
| Reflect | 462 | 392 | 7 | 2.1× slower |
| JSON | 2386 | 776 | 25 | 10.6× slower |

## Map For Each

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 770 | 0 | 0 | — |
| Range | 780 | 0 | 0 | 1.0× slower |

## Get_int

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 41.1 | 0 | 0 | — |
| Reflect | 46.8 | 0 | 0 | 1.1× slower |
| ReflectFast | 2.90 | 0 | 0 | 14.2× faster |
| Offset | 8.71 | 0 | 0 | 4.7× faster |
| Accessor | 0.580 | 0 | 0 | 70.9× faster |
| AccFrom | 2.61 | 0 | 0 | 15.7× faster |
| Direct | 0.579 | 0 | 0 | 71.0× faster |

## Set_string

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 40.5 | 0 | 0 | — |
| Reflect | 53.9 | 0 | 0 | 1.3× slower |
| ReflectFast | 4.16 | 0 | 0 | 9.7× faster |
| Offset | 10.2 | 0 | 0 | 4.0× faster |
| Accessor | 1.16 | 0 | 0 | 35.0× faster |
| AccOn | 2.78 | 0 | 0 | 14.6× faster |
| Direct | 0.581 | 0 | 0 | 69.7× faster |

## DI Resolve

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 0.584 | 0 | 0 | — |
| SafeRefl | 122 | 0 | 0 | 208.7× slower |
| Accessor | 2.68 | 0 | 0 | 4.6× slower |
| Reflect2 | 14.4 | 0 | 0 | 24.7× slower |
| Reflect | 207 | 0 | 0 | 353.9× slower |

## JSON Decode

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| StdlibJSON | 2405 | 392 | 10 | — |
| SafeRefl | 456 | 0 | 0 | 5.3× faster |
| Reflect | 1335 | 0 | 0 | 1.8× faster |
| Reflect2 | 59.6 | 0 | 0 | 40.4× faster |
| Accessor | 6.72 | 0 | 0 | 357.7× faster |

## ORM Scan

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 11.6 | 0 | 0 | — |
| SafeRefl | 475 | 0 | 0 | 41.0× slower |
| Accessor | 11.4 | 0 | 0 | 1.0× faster |
| Reflect2 | 61.2 | 0 | 0 | 5.3× slower |
| Reflect | 816 | 0 | 0 | 70.4× slower |
| Copier | 6544 | 640 | 28 | 564.8× slower |

## Struct Copy

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 7.22 | 0 | 0 | — |
| Accessor | 7.16 | 0 | 0 | 1.0× faster |
| Reflect2 | 30.1 | 0 | 0 | 4.2× slower |
| Offset | 134 | 0 | 0 | 18.5× slower |
| Reflect | 584 | 0 | 0 | 80.9× slower |
| SafeRefl | 459 | 0 | 0 | 63.5× slower |
| Copier | 2938 | 432 | 17 | 406.8× slower |

