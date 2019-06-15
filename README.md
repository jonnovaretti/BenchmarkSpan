# BenchmarkSpan

Results

// * Summary *

BenchmarkDotNet=v0.11.5, OS=Windows 10.0.17134.765 (1803/April2018Update/Redstone4)
Intel Core i5-6200U CPU 2.30GHz (Skylake), 1 CPU, 4 logical and 2 physical cores
Frequency=2343746 Hz, Resolution=426.6674 ns, Timer=TSC
.NET Core SDK=2.2.203
  [Host]     : .NET Core 2.2.4 (CoreCLR 4.6.27521.02, CoreFX 4.6.27521.01), 64bit RyuJIT  [AttachedDebugger]
  DefaultJob : .NET Core 2.2.4 (CoreCLR 4.6.27521.02, CoreFX 4.6.27521.01), 64bit RyuJIT


|          Method |        Mean |      Error |     StdDev | Rank |    Gen 0 |   Gen 1 | Gen 2 | Allocated |
|---------------- |------------:|-----------:|-----------:|-----:|---------:|--------:|------:|----------:|
|       resultUtf | 2,095.88 us | 42.4098 us | 120.309 us |    3 | 246.0938 | 54.6875 |     - |  496160 B |
|    resultNewton | 2,230.31 us | 81.0892 us | 230.037 us |    4 | 121.0938 | 31.2500 |     - |  420072 B |
|      resultSpan |    23.24 us |  0.6393 us |   1.834 us |    1 |   0.0610 |       - |     - |     128 B |
| resultSubstring |   219.70 us |  3.6589 us |   3.055 us |    2 |   0.2441 |       - |     - |     672 B |
