# Relatório

## Sequencial

### How to compile

```terminal
$ gcc8 -lstdc++ -o TestChain -std=c++11 -x c++ main.cpp Block.cpp Blockchain.cpp sha256.cpp

Para executar:

$ time ./TestChain
```

### Results

Mining block 1...  
Block mined: 00000d6d767bcf0f99025b4d4cbe490cf44ac38edc8f0c7aba82fa2749f0e408

Mining block 2...  
Block mined: 00000be7da9ff414ba6d52ed663ddf9ab7d79a3a3288a41378a12826ae33578e

Mining block 3...  
Block mined: 00000d3094df263d03737ffee835784a04a1debe0dd0152478ade8ceee40d4d7

```terminal
real    0m59.456s
user    0m59.437s
sys     0m0.004s
```

## OpenMP para multicore CPU

### How to compile

```terminal
$ gcc8 -fopenmp -O3 -lstdc++ -o TestChain -std=c++11 -x c++ main.cpp Block.cpp Blockchain.cpp sha256.cpp 

Para executar:

$ time ./TestChain
```

### Results

Mining block 1...  
Block mined: 00000604ee89d626655b6da9187eff19d27f0829e84b3e9b78d040d92e4c12f0

Mining block 2...  
Block mined: 00000613c1231fc60e552859ab6e30c88a45fd6aa9ec4c1300f8f3770ad5dfee

Mining block 3...  
Block mined: 00000763b8f852671829b0cd0f1747c778a18fd01f5f44a05183d4d9a2d720d5

```terminal
real    0m41.571s
user    2m36.132s
sys     0m9.967s
```

## OpenMP para GPU

Mining block 1...  
Block mined: 00000309ff401a0ac77b60a65953d0fd83c9775ff92e5e0244057610c27d843b

Mining block 2...  
Block mined: 00000b4f4337a3fa0d3d93b968192c02a5117ab92ac59f7b0696d294b687a854

Mining block 3...  
Block mined: 0000094dc7a302c77f4adc853171475d4673bfa4421c5d3c270090b50da9fac6

```terminal
real    0m27.340s
user    0m27.323s
sys     0m0.008s
```

## CUDA para GPU

Mining block 1...  
Block mined: 0000028991413da63767ab2ce4f16b02bc34e8b05fe7871d1a749fbfa8a06263

Mining block 2...  
Block mined: 000001df328529531a1a827adf8fc2e89ffe2589e84ac341842aee763c9593da

Mining block 3...  
Block mined: 00000cb5da3d524dbedc347d13ee2abcf6cfbc73f7542e8404c5fd0a75b0e081

```terminal
real    0m11.413s
user    0m11.405s
sys     0m0.004s
```
