# java-assinatura-digital-utils
Repositório dedicado a exemplos e tutoriais de criptografia e assinatura digital utilizando Java. Explore implementações práticas e conceitos fundamentais.

# Conceitos fundamentais

## Segurança da informação

Segurança da informação significa proteger a informação e os sistemas de informação de uso e acesso desautorizado, modificação ou destruição a fim de garantir os três pilares da segurança da informação, confidencialidade, integridade e disponibilidade.

O conceito de segurança é compreendido por uma vastidão de aspectos, o que o torna extremamente vago. As ferramentas tecnológicas são apenas instrumentos que podem, ou não, ser aplicados de forma eficaz para se implantar a segurança. Elas devem ser complementadas com uma abordagem organizacional, com a definição, implantação e manutenção de políticas de segurança e também uma abordagem em âmbitos pessoais, levando em consideração os aspectos humanos.

Os métodos ou ferramentas tecnológicas que podem ser utilizadas para se alcançar a segurança são conceitos como criptografia, controle de acesso e integridade dos dados.

Este artigo apresentará os conceitos de criptografia simétrica, assimétrica, funções de hash, evelopamento digital e assinatura digital.

## Criptografia simétrica

Criptografia simétrica é um método de criptografia onde é utilizada uma chave, chamada chave secreta, para a cifragem da informação. A chave secreta é utilizada tanto para a cifrar quanto para a decifrar. Em relação a criptografia assimétrica, os algorítimos de criptografia simétrica são mais eficientes, em termos de velocidade. Sua desvantagem fica na distribuição de gerenciamento das chaves secretas.

Os algorítimos de criptografia simétrica então divididos em duas classes: stream ciphers e block ciphers. Stream ciphers são algorítimos que criptografam digito a digito os dados, existem vários algorítimos deste tipo, muitos já foram quebrados. Os block ciphers são algorítimos que criptografam blocos de dados, estes blocos são de tamanho fixo, o algoritmo mais conhecido é DES (Data Encryption Standard), outro algoritmo é o AES (Advanced Encryption Standard), criado recentemente, é o mais utilizado atualmente.

**TODO exemplos java**

## Criptografia assimétrica

Criptografia assimétrica é outro método de criptografia que foi criado para solucionar o problema de gerenciamento e distribuição das chaves para criptografia simétrica. Neste método existem duas chaves, uma publica e uma privada, onde a privada é de conhecimento apenas de seu proprietário e a publica é de conhecimento publico, sendo que os dados criptografados pela chave privada só podem ser recuperados pela chave publica e vise versa.

O principal algoritmo assimétrico é o RSA, um algoritmo que possui este nome devido a seus inventores: Ron Rivest, Adi Shamir e Len Adleman, que o criaram em 1977 no MIT. Atualmente, é o algoritmo de chave pública mais amplamente utilizado, além de ser uma das mais poderosas formas de criptografia de chave pública conhecidas até o momento.

Para garantir que apenas o destinatário possa recuperar uma informação basta criptografar utilizando a chave publica do destinatário, assim se somente ele tiver conhecimento de sua chave privada, apenas ele poderá recuperá-la, garantindo assim a confidencialidade da informação. 

Integridade, autenticidade e não repúdio da informação são garantidos com a criptografia utilizando a chave privada do remetente, assim apenas a chave publica dele poderá decifrar a mensagem, esse processo também é chamado de assinatura digital.

**TODO exemplos java**

## Assinatura digital 

A assinatura digital é a garantia de integridade e autenticidade das informações eletrônicas. A assinatura digital permite comprovar que a informação não foi alterada e que foi assinado pela entidade ou pessoa que possui a chave criptográfica (chave privada) utilizada na assinatura.

Utilizando a criptografia assimétrica, o remetente de uma mensagem ou o proprietário de uma informação utiliza sua chave privada para cifragem, garantindo a autenticidade e não-repudio da informação, pois apenas sua chave publica poderá decifrar a infomação.

Para comprovar que um par de chaves publica e privada pertence a determinada pessoa existe o certificado digital. Certificado digital é um documento eletrônico assinado digitalmente, contendo a identificação de uma pessoa, sua chave pública (utilizada na verificação da validade da assinatura) e assinado digitalmente por uma autoridade certificadora.

## Envelopamento digital

Os modelos de criptografia simétrica e assimétrica possuem suas vantagens e desvantagens, com isso houve a combinação das vantagens de cada modelo, eliminando suas desvantagens.  Essa combinação funciona da seguinte maneira, a criptografia simétrica é utilizada para criptografar a informação, pois sua velocidade é superior, e a criptografia assimétrica é utilizada para criptografar a chave secreta utilizada para criptografar a informação, eliminando a necessidade da troca de chaves secretas. 

Também pode ser utilizada a assinatura digital e funções de hash para garantir a integridade e autenticidade. Essa combinação de modelos criptograficos é chamada de envelopamento digital.

O envelopamento digital é a técnica que utiliza a criptografia simétrica, assimétrica e a assinatura digital, praticamente eliminando suas desvantagens.

## Funções de hash

Função de hash é uma função que recebe uma entrada de dados de tamanho variável e gera uma saída de tamanho fixo que representa o dado de entrada. Comumente utilizada para garantir a integridade dos dados, suas principais propriedades:
* Não é possível determinar a entrada a partir da saída, por isso são chamadas de funções unidirecionais.
* A menor mudança nos dados de entrada geram uma saída completamente diferente.
* Não existem duas entradas com a mesma saída.
* Uma entrada nunca gera uma saída diferente.
 

O algorítimo mais comum e mais utilizado atualmente é o SHA-256 ou SHA-512, há algum tempo atrás o MD5 era o mais utilizado mas tornou-se menos confiável e está caindo em desuso.
 
Deve se ter em mente que ainda não foi desenvolvido um método de construção de funções de hash que seja comprovadamente forte, sendo um campo bastante intenso de pesquisas.

## Referências

ALEXANDRIA, J. C. S. DE. Gestão da segurança da informação: uma proposta para potencializar a efetividade da segurança da informação em ambiente de pesquisa científica. USP, 2009. Disponível em: <http://www.teses.usp.br/teses/disponiveis/85/85131/tde-22092011-095831/pt-br.php>. Acesso em: 27 jun. 2013.

KOBAYASHI, L. O. M. Abordagem criptográfica para integridade e autenticidade em imagens médicas. USP, 2007. Disponível em: <http://www.teses.usp.br/teses/disponiveis/3/3142/tde-14012008-122458/pt-br.php>. Acesso em: 28 jun. 2013.

https://www.ronielton.eti.br/publicacoes/artigorevistasegurancadigital2012.pdf

SILVA, A. Assinaturas digitais. Gestão em TI. Disponível em: <http://hercules-now.com/tag/assinaturas-digitais/>. Acesso em: 15 jul. 2013.

CASTELLÓ, T; VAZ, V. Assinatura digital. UFRJ. Disponível em: <http://www.gta.ufrj.br/grad/07_1/ass-dig/TiposdeCriptografia.html>. Acesso em: 15 jul. 2013.,
