<p align="center">
  <img src="https://github.com/hildocosta/hildocosta-Curso-Java--Nelio-Alves/blob/main/logo.png" width="300">
</p>
<h1 align="center">🚀 Explorando o Bloco Try-With-Resources em Java</h1>
<p>🔥 Bem-vindo ao repositório dedicado à exploração do bloco try-with-resources na linguagem de programação Java. Aqui, você encontrará informações e exemplos práticos sobre como usar o bloco try-with-resources para gerenciar recursos automaticamente em seus programas Java.</p>
<p>🎓 Este repositório é voltado para estudantes e desenvolvedores que desejam aprender como lidar com recursos, como arquivos ou conexões de banco de dados, de forma eficiente e segura em Java. Aqui, você encontrará explicações detalhadas, exemplos de código e exercícios para aprimorar suas habilidades no uso do bloco try-with-resources.</p>
<p>💡 Ao explorar o bloco try-with-resources em Java, você aprenderá como garantir que recursos externos sejam fechados de forma automática e segura, evitando vazamentos de recursos e erros relacionados ao gerenciamento de recursos. Isso contribui para a criação de programas mais robustos e confiáveis em Java.</p>
<h2 align="center">🔒 Licença</h2>
<p>⚖️ Este projeto está licenciado sob a <a href="LICENSE">Licença MIT</a>.</p>
<h2 align="center">📧 Contato</h2>
<h3>🔗 Redes Sociais e Contato</h3>
<ul>
  <li>📌 GitHub: <a href="https://github.com/hildocosta">hildocosta</a></li>
  <li>💼 LinkedIn: <a href="https://www.linkedin.com/in/hildo-costa-b83812231/">Hildo Costa</a></li>
  <li>✉️ Email: hildo.costa@pm.pr.gov.br</li>
</ul>
<p>Agora que estamos preparados, vamos explorar o bloco try-with-resources em Java!</p>
<h2 align="center">🚀 Vamos Começar</h2>
<h3>🔥 Bloco Try-With-Resources em Java</h3>
<p>O bloco try-with-resources em Java é uma maneira eficiente de garantir que recursos externos sejam fechados automaticamente após o uso, sem a necessidade de código adicional para fechá-los manualmente. Isso é especialmente útil para recursos que implementam a interface <code>AutoCloseable</code>, como arquivos, conexões de banco de dados ou sockets de rede.</p>
<p>Veja um exemplo de código para usar o bloco try-with-resources em Java:</p>


```java
import java.io.BufferedReader;
import java.io.FileReader;
import java.io.IOException;

public class Main {

    public static void main(String[] args) {
        
        String caminho = "caminho/do/arquivo.txt";
        
        try (BufferedReader br = new BufferedReader(new FileReader(caminho))) {
            String linha = br.readLine();
            while (linha != null) {
                System.out.println(linha);
                linha = br.readLine();
            }
        } catch(IOException e) {
            System.out.println("Erro ao ler o arquivo: " + e.getMessage());
        }
    }
}

```

<p>Neste exemplo, o bloco try-with-resources é usado para abrir e ler um arquivo de texto. O recurso <code>BufferedReader</code> é inicializado dentro do bloco try, e será fechado automaticamente após o término do bloco, garantindo que os recursos sejam liberados de forma automática e segura.</p>

<p>Agora que você entende como usar o bloco try-with-resources em Java, experimente aplicá-lo em seus próprios programas para garantir o gerenciamento eficiente de recursos!</p>
