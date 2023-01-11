# resilia_diagrama_modulo04
A Resilia está pensando em lançar um novo sistema de acompanhamento e para isso precisa de ajuda para modelar um banco de dados que vai armazenar seus cursos, turmas e alunos.



1 - Existem outras entidades além dessas três?

R: Sim, pois precisrá de mais intidades que se faz necessária para completar o modelo de negócio,
por exemplo, além de ter CURSOS, precisamos de BAIRROS para assim saber quais BAIRROS terá os CURSOS.
No caso de TURMAS, precisamos ter as MATÉRIAS para saber se as matérias das TURMAS.




2 - Quais são os principais campos e tipos?

R: Os campos são:
(Cursos) : NOME, PREÇO, DATA INÍCIO E TÉRMINO E CARGA HORÁRIA
(Turma) : MANHÃ, TARDE E NOITE
(Matérias) : SOFT E HARD
(Matrículas) : DATA DA MATRICULA E TOTAL DE MATRÍCULAS


(Cursos) :    VARCHAR(45) e INT
(Turma) :     VARCHAR(45) e INT
(Matérias) :  VARCHAR(45) e INT
(Matrículas): VARCHAR(45) e INT
(ALUNOS) :    VARCHAR(45) e INT
(BAIRROS) : VARCHAR(45)

(VARCHAR é de comprimento variável.)
Use VARCHAR quando os tamanhos a serem armazenados na coluna da tabela variam consideravelmente. Ex: Endereço,Nomes, URL, etc. 
Dessa forma um valor menor irá ocupar menos espaço que um valor maior.

É uma definição de uma variável chamada a que pode guardar valores do tipo int (inteiros).  A sintaxe das definições pode ser
algo complicada, mas em geral tem a forma acima, isto é, o nome do tipo seguido do nome da variável.



3 - Como essas entidades estão relacionadas?
CURSOS está ligado TURMA e BAIRROS 1:n("um para vários")
TURMA está ligada para BAIRROS e CURSOS 1:n("um para vários")
ALUNOS está ligada para MATRICULAS 1x1 ("um para um")
