# Demonstração de Manipulação de Datas e Horários em Java

Este projeto consiste em um programa Java simples que demonstra várias formas de trabalhar com datas e horários utilizando as classes do pacote `java.time` introduzido no Java 8. O código mostra como obter a data e hora atuais, como analisar strings em diferentes formatos para criar objetos de data e hora, e como criar datas e horas especificando seus componentes individuais.

**Autor:** gustavodees

## Arquivos Incluídos

* `principal/Main.java`: Contém a classe principal com o método `main`, onde as diversas operações de manipulação de datas e horários são demonstradas.

## Como Usar

1.  **Salve o arquivo:** Salve o código fornecido em um arquivo chamado `Main.java` dentro de uma pasta chamada `principal`.
2.  **Compile o código:** Abra um terminal ou prompt de comando, navegue até o diretório raiz do seu projeto e compile o arquivo Java utilizando o compilador Java:

    ```bash
    javac principal/Main.java
    ```

3.  **Execute o programa:** Após a compilação ser concluída com sucesso, execute a classe `Main` com o comando:

    ```bash
    java principal.Main
    ```

4.  **Resultado:** O programa exibirá no console dez linhas, cada uma representando uma diferente forma de obter ou criar um objeto de data ou hora, formatado de acordo com a saída padrão do método `toString()` de cada classe (`LocalDate`, `LocalDateTime`, `Instant`).

## Explicação do Código

### `principal/Main.java`

Este arquivo contém a classe `Main`, que é o ponto de entrada do programa e demonstra a manipulação de datas e horários.

* **Método `main`:**
    1.  **Criação de `DateTimeFormatter`:** São criados dois objetos `DateTimeFormatter` para definir formatos específicos de data e hora:
        * `dtf` formata datas no padrão "dd/MM/yyyy".
        * `dtf2` formata data e hora no padrão "dd/MM/yyyy HH:mm".
    2.  **Obtendo a data e hora atuais:**
        * `LocalDate.now()`: Obtém a data atual.
        * `LocalDateTime.now()`: Obtém a data e hora atuais.
        * `Instant.now()`: Obtém o instante atual (representa um ponto na linha do tempo em UTC).
    3.  **Analisando strings para criar datas e horas:**
        * `LocalDate.parse("2022-07-20")`: Cria um objeto `LocalDate` a partir de uma string no formato ISO 8601 (aaaa-MM-dd).
        * `LocalDateTime.parse("2022-07-20T01:30:26")`: Cria um objeto `LocalDateTime` a partir de uma string no formato ISO 8601 (aaaa-MM-ddTHH:mm:ss).
        * `Instant.parse("2022-07-20T20:38:26-03:00")`: Cria um objeto `Instant` a partir de uma string no formato ISO 8601 com informações de timezone offset.
        * `LocalDate.parse("20/07/2022", dtf)`: Cria um objeto `LocalDate` a partir de uma string no formato "dd/MM/yyyy", utilizando o formatador `dtf` definido anteriormente.
        * `LocalDateTime.parse("20/07/2022 01:30", dtf2)`: Cria um objeto `LocalDateTime` a partir de uma string no formato "dd/MM/yyyy HH:mm", utilizando o formatador `dtf2`.
    4.  **Criando datas e horas especificando os componentes:**
        * `LocalDate.of(2022, 7, 20)`: Cria um objeto `LocalDate` especificando o ano, mês (7 para Julho) e dia.
        * `LocalDateTime.of(2022, 7, 20, 20, 30)`: Cria um objeto `LocalDateTime` especificando o ano, mês, dia, hora (em formato 24 horas) e minuto.
    5.  **Imprimindo os resultados:** Cada um dos objetos de data e hora criados é impresso no console utilizando `System.out.println()`. A saída mostrará a representação padrão de cada objeto.
