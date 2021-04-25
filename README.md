## Java Microbenchmark Harness

# 1. Introdução
Este artigo rápido se concentra em JMH (o Java Microbenchmark Harness). Primeiro, nos familiarizamos com a API e aprendemos seus fundamentos. Em seguida, veríamos algumas práticas recomendadas que devemos considerar ao escrever microbenchmarks.

Simplificando, o JMH cuida de coisas como o aquecimento da JVM e os caminhos de otimização de código, tornando o benchmarking o mais simples possível.

# 2. Primeiros passos
Para começar, podemos realmente continuar trabalhando com Java 8 e simplesmente definir as dependências:

```
<dependency>
    <groupId>org.openjdk.jmh</groupId>
    <artifactId>jmh-core</artifactId>
    <version>1.28</version>
</dependency>
<dependency>
    <groupId>org.openjdk.jmh</groupId>
    <artifactId>jmh-generator-annprocess</artifactId>
    <version>1.28</version>
</dependency>
```

As versões mais recentes do JMH Core e do JMH Annotation Processor podem ser encontradas no Maven Central.

Em seguida, crie um benchmark simples utilizando a anotação @Benchmark (em qualquer classe pública):

```
@Benchmark
public void init() {
    // Do nothing
}
```