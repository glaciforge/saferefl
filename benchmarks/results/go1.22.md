# Benchmark Results

**Generated:** 2026-09-20 10:43 UTC  
**Go:** 1.22  
**Platform:** linux/amd64  
**CPU:** AMD EPYC 7763 64-Core Processor                  

## Field Read

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Reflect | 68.6 | 8 | 1 | — |
| ReflectFast | 3.17 | 0 | 0 | 21.6× faster |
| SafeRefl | 45.2 | 0 | 0 | 1.5× faster |
| Offset | 11.6 | 0 | 0 | 5.9× faster |
| Accessor | 0.938 | 0 | 0 | 73.1× faster |
| Native | 0.313 | 0 | 0 | 219.3× faster |

## Slice At

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 1.01 | 0 | 0 | — |
| Direct | 1.00 | 0 | 0 | 1.0× faster |
| Reflect | 3.75 | 0 | 0 | 3.7× slower |

## Map Len

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.626 | 0 | 0 | — |
| Builtin | 0.313 | 0 | 0 | 2.0× faster |
| Reflect | 4.68 | 0 | 0 | 7.5× slower |

## Kind Of

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 0.936 | 0 | 0 | — |
| Reflect | 2.19 | 0 | 0 | 2.3× slower |

## Is Nil_ptr

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 3.43 | 0 | 0 | — |
| Reflect | 2.50 | 0 | 0 | 1.4× faster |

## Each Field

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 51.3 | 0 | 0 | — |
| Reflect | 157 | 56 | 5 | 3.1× slower |
| ReflectFull | 160 | 56 | 5 | 3.1× slower |
| Reflect2 | 24.9 | 0 | 0 | 2.1× faster |

## Copy Fields

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 281 | 0 | 0 | — |
| Manual | 0.313 | 0 | 0 | 899.9× faster |
| Reflect | 594 | 80 | 10 | 2.1× slower |

## To Map

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 226 | 336 | 2 | — |
| Reflect | 516 | 432 | 12 | 2.3× slower |
| JSON | 2769 | 776 | 25 | 12.2× slower |

## Map For Each

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 954 | 0 | 0 | — |
| Range | 974 | 0 | 0 | 1.0× slower |

## Get_int

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 45.3 | 0 | 0 | — |
| Reflect | 70.1 | 8 | 1 | 1.5× slower |
| ReflectFast | 3.12 | 0 | 0 | 14.5× faster |
| Offset | 11.7 | 0 | 0 | 3.9× faster |
| Accessor | 0.937 | 0 | 0 | 48.4× faster |
| AccFrom | 3.12 | 0 | 0 | 14.5× faster |
| Direct | 0.312 | 0 | 0 | 145.2× faster |

## Set_string

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| SafeRefl | 46.4 | 0 | 0 | — |
| Reflect | 72.5 | 8 | 1 | 1.6× slower |
| ReflectFast | 4.99 | 0 | 0 | 9.3× faster |
| Offset | 13.7 | 0 | 0 | 3.4× faster |
| Accessor | 1.25 | 0 | 0 | 37.2× faster |
| AccOn | 3.44 | 0 | 0 | 13.5× faster |
| Direct | 0.624 | 0 | 0 | 74.3× faster |

## DI Resolve

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 0.632 | 0 | 0 | — |
| SafeRefl | 154 | 0 | 0 | 243.0× slower |
| Accessor | 3.12 | 0 | 0 | 4.9× slower |
| Reflect2 | 20.9 | 0 | 0 | 33.0× slower |
| Reflect | 242 | 24 | 3 | 382.4× slower |

## JSON Decode

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| StdlibJSON | 2687 | 392 | 10 | — |
| SafeRefl | 521 | 0 | 0 | 5.2× faster |
| Reflect | 1739 | 160 | 20 | 1.5× faster |
| Reflect2 | 79.6 | 0 | 0 | 33.7× faster |
| Accessor | 9.55 | 0 | 0 | 281.5× faster |

## ORM Scan

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 14.1 | 0 | 0 | — |
| SafeRefl | 541 | 0 | 0 | 38.4× slower |
| Accessor | 12.3 | 0 | 0 | 1.1× faster |
| Reflect2 | 83.2 | 0 | 0 | 5.9× slower |
| Reflect | 997 | 80 | 10 | 70.8× slower |
| Copier | 7253 | 880 | 58 | 514.6× slower |

## Struct Copy

| Variant | ns/op | B/op | allocs/op | vs first |
|---|---|---|---|---|
| Manual | 9.69 | 0 | 0 | — |
| Accessor | 10.5 | 0 | 0 | 1.1× slower |
| Reflect2 | 40.5 | 0 | 0 | 4.2× slower |
| Offset | 186 | 0 | 0 | 19.2× slower |
| Reflect | 780 | 80 | 10 | 80.6× slower |
| SafeRefl | 524 | 0 | 0 | 54.1× slower |
| Copier | 3227 | 552 | 32 | 333.1× slower |

