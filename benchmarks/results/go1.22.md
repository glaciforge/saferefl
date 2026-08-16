# Benchmark Results

**Generated:** 2026-08-16 06:38 UTC  
**Go:** 1.22  
**Platform:** linux/amd64  
**CPU:** INTEL(R) XEON(R) PLATINUM 8573C  

## Field Read

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Reflect | 48.8 | 8 | 1 | — |
| ReflectFast | 2.30 | 0 | 0 | 21.2× faster |
| SafeRefl | 35.8 | 0 | 0 | 1.4× faster |
| Offset | 8.03 | 0 | 0 | 6.1× faster |
| Accessor | 0.849 | 0 | 0 | 57.4× faster |
| Native | 0.281 | 0 | 0 | 173.5× faster |

## Slice At

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.898 | 0 | 0 | — |
| Direct | 0.944 | 0 | 0 | 1.1× slower |
| Reflect | 2.82 | 0 | 0 | 3.1× slower |

## Map Len

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.564 | 0 | 0 | — |
| Builtin | 0.423 | 0 | 0 | 1.3× faster |
| Reflect | 3.24 | 0 | 0 | 5.8× slower |

## Kind Of

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.664 | 0 | 0 | — |
| Reflect | 1.47 | 0 | 0 | 2.2× slower |

## Is Nil_ptr

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 2.39 | 0 | 0 | — |
| Reflect | 2.33 | 0 | 0 | 1.0× faster |

## Each Field

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 41.3 | 0 | 0 | — |
| Reflect | 109 | 56 | 5 | 2.6× slower |
| ReflectFull | 116 | 56 | 5 | 2.8× slower |
| Reflect2 | 15.3 | 0 | 0 | 2.7× faster |

## Copy Fields

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 234 | 0 | 0 | — |
| Manual | 0.282 | 0 | 0 | 830.8× faster |
| Reflect | 431 | 80 | 10 | 1.8× slower |

## To Map

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 182 | 336 | 2 | — |
| Reflect | 397 | 432 | 12 | 2.2× slower |
| JSON | 2022 | 776 | 25 | 11.1× slower |

## Map For Each

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 700 | 0 | 0 | — |
| Range | 715 | 0 | 0 | 1.0× slower |

## Get_int

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 35.7 | 0 | 0 | — |
| Reflect | 48.4 | 8 | 1 | 1.4× slower |
| ReflectFast | 2.31 | 0 | 0 | 15.5× faster |
| Offset | 8.35 | 0 | 0 | 4.3× faster |
| Accessor | 0.839 | 0 | 0 | 42.6× faster |
| AccFrom | 2.38 | 0 | 0 | 15.0× faster |
| Direct | 0.281 | 0 | 0 | 127.0× faster |

## Set_string

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 36.6 | 0 | 0 | — |
| Reflect | 49.2 | 8 | 1 | 1.3× slower |
| ReflectFast | 3.65 | 0 | 0 | 10.0× faster |
| Offset | 10.0 | 0 | 0 | 3.7× faster |
| Accessor | 1.19 | 0 | 0 | 30.9× faster |
| AccOn | 2.39 | 0 | 0 | 15.3× faster |
| Direct | 0.560 | 0 | 0 | 65.4× faster |

## DI Resolve

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 0.560 | 0 | 0 | — |
| SafeRefl | 110 | 0 | 0 | 196.1× slower |
| Accessor | 2.20 | 0 | 0 | 3.9× slower |
| Reflect2 | 13.9 | 0 | 0 | 24.8× slower |
| Reflect | 189 | 24 | 3 | 336.7× slower |

## JSON Decode

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| StdlibJSON | 2075 | 392 | 10 | — |
| SafeRefl | 424 | 0 | 0 | 4.9× faster |
| Reflect | 1240 | 160 | 20 | 1.7× faster |
| Reflect2 | 52.9 | 0 | 0 | 39.2× faster |
| Accessor | 6.88 | 0 | 0 | 301.8× faster |

## ORM Scan

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 10.9 | 0 | 0 | — |
| SafeRefl | 440 | 0 | 0 | 40.3× slower |
| Accessor | 9.95 | 0 | 0 | 1.1× faster |
| Reflect2 | 54.3 | 0 | 0 | 5.0× slower |
| Reflect | 731 | 80 | 10 | 66.8× slower |
| Copier | 5682 | 880 | 58 | 519.3× slower |

## Struct Copy

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 6.73 | 0 | 0 | — |
| Accessor | 6.74 | 0 | 0 | 1.0× slower |
| Reflect2 | 28.3 | 0 | 0 | 4.2× slower |
| Offset | 132 | 0 | 0 | 19.6× slower |
| Reflect | 545 | 80 | 10 | 81.0× slower |
| SafeRefl | 426 | 0 | 0 | 63.3× slower |
| Copier | 2488 | 552 | 32 | 369.6× slower |

