# OpenMP

## intro 

O padrão OpenMP é desenvolvido e mantido pelo grupo OpenMP
Architecture Review Board (ARB), formado pelos maiores fabricantes de
software e hardware do mundo, tais como SUN Microsystems, SGI, IBM,
Intel, dentre outros, que, no final de 1997, reuniram esforços para criar um
padrão de programação paralela para arquiteturas de memória
compartilhada.

Representa um padrão que define como os compiladores devem gerar códigos paralelos
através da incorporação, nos programas seqüenciais, de diretivas que indicam
como o trabalho será dividido entre os processadores ou cores.

OpenMP foi planejado para satisfazer a implementação
em larga escala das arquiteturas SMPs.

![Modelo SMP]("imgs/smp.png")

## diretivas

O OpenMP trabalha na lógica fork-join, no qual após a declaração da diretiva, as threads executam suas tarefas de maneira paralela(fork) e após o término de uma, aguarda o encerramento das outras(join). Essa ideia denota que o código multi-thread tem uma parte paralela(fork) e uma sequencial(join).

![Modelo SMP]("imgs/forkjoin.png")

```c
OMP_NOME
```

- Declaração de uma variavel de ambiente

```c
#pragma omp diretiva [cláusula]
```

- Definição das diretivas

```c
omp_serviço (...)
```

- Lib de serviço

