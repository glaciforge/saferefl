# Benchmark Results

**Generated:** 2026-08-09 06:55 UTC  
**Go:** 1.22  
**Platform:** linux/amd64  
**CPU:** AMD EPYC 7763 64-Core Processor                  

## Field Read

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Reflect | 68.3 | 8 | 1 | — |
| ReflectFast | 3.15 | 0 | 0 | 21.7× faster |
| SafeRefl | 45.2 | 0 | 0 | 1.5× faster |
| Offset | 11.6 | 0 | 0 | 5.9× faster |
| Accessor | 0.944 | 0 | 0 | 72.3× faster |
| Native | 0.313 | 0 | 0 | 218.6× faster |

## Slice At

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 1.01 | 0 | 0 | — |
| Direct | 1.00 | 0 | 0 | 1.0× faster |
| Reflect | 3.76 | 0 | 0 | 3.7× slower |

## Map Len

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.627 | 0 | 0 | — |
| Builtin | 0.312 | 0 | 0 | 2.0× faster |
| Reflect | 4.68 | 0 | 0 | 7.5× slower |

## Kind Of

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.936 | 0 | 0 | — |
| Reflect | 2.18 | 0 | 0 | 2.3× slower |

## Is Nil_ptr

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 3.47 | 0 | 0 | — |
| Reflect | 2.52 | 0 | 0 | 1.4× faster |

## Each Field

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 51.2 | 0 | 0 | — |
| Reflect | 156 | 56 | 5 | 3.1× slower |
| ReflectFull | 160 | 56 | 5 | 3.1× slower |
| Reflect2 | 24.9 | 0 | 0 | 2.1× faster |

## Copy Fields

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 288 | 0 | 0 | — |
| Manual | 0.312 | 0 | 0 | 922.9× faster |
| Reflect | 590 | 80 | 10 | 2.1× slower |

## To Map

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 225 | 336 | 2 | — |
| Reflect | 515 | 432 | 12 | 2.3× slower |
| JSON | 2764 | 776 | 25 | 12.3× slower |

## Map For Each

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 956 | 0 | 0 | — |
| Range | 980 | 0 | 0 | 1.0× slower |

## Get_int

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 45.1 | 0 | 0 | — |
| Reflect | 67.7 | 8 | 1 | 1.5× slower |
| ReflectFast | 3.12 | 0 | 0 | 14.5× faster |
| Offset | 11.9 | 0 | 0 | 3.8× faster |
| Accessor | 0.940 | 0 | 0 | 48.0× faster |
| AccFrom | 3.15 | 0 | 0 | 14.3× faster |
| Direct | 0.313 | 0 | 0 | 144.1× faster |

## Set_string

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 45.9 | 0 | 0 | — |
| Reflect | 71.4 | 8 | 1 | 1.6× slower |
| ReflectFast | 4.99 | 0 | 0 | 9.2× faster |
| Offset | 13.7 | 0 | 0 | 3.3× faster |
| Accessor | 1.25 | 0 | 0 | 36.8× faster |
| AccOn | 4.77 | 0 | 0 | 9.6× faster |
| Direct | 0.626 | 0 | 0 | 73.3× faster |

## DI Resolve

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 0.628 | 0 | 0 | — |
| SafeRefl | 152 | 0 | 0 | 242.2× slower |
| Accessor | 3.12 | 0 | 0 | 5.0× slower |
| Reflect2 | 20.9 | 0 | 0 | 33.3× slower |
| Reflect | 241 | 24 | 3 | 383.3× slower |

## JSON Decode

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| StdlibJSON | 2701 | 392 | 10 | — |
| SafeRefl | 527 | 0 | 0 | 5.1× faster |
| Reflect | 1723 | 160 | 20 | 1.6× faster |
| Reflect2 | 79.7 | 0 | 0 | 33.9× faster |
| Accessor | 9.54 | 0 | 0 | 283.0× faster |

## ORM Scan

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 14.1 | 0 | 0 | — |
| SafeRefl | 540 | 0 | 0 | 38.3× slower |
| Accessor | 12.3 | 0 | 0 | 1.1× faster |
| Reflect2 | 82.5 | 0 | 0 | 5.9× slower |
| Reflect | 980 | 80 | 10 | 69.5× slower |
| Copier | 7206 | 880 | 58 | 511.4× slower |

## Struct Copy

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 9.69 | 0 | 0 | — |
| Accessor | 10.5 | 0 | 0 | 1.1× slower |
| Reflect2 | 40.3 | 0 | 0 | 4.2× slower |
| Offset | 184 | 0 | 0 | 19.0× slower |
| Reflect | 778 | 80 | 10 | 80.3× slower |
| SafeRefl | 521 | 0 | 0 | 53.8× slower |
| Copier | 3204 | 552 | 32 | 330.7× slower |

