/*BANCO DE DADOS I
LAB04
MARCELO DOLABELLA*/

--1)
SELECT e.nom_empregado FROM empregado AS e
WHERE e.num_matricula IN
	(SELECT num_matricula FROM alocacao);

--2)
SELECT d.nom_depto FROM departamento AS d
WHERE d.cod_depto IN
	(SELECT cod_depto FROM projeto);

--3)
SELECT e.nom_empregado FROM empregado AS e
WHERE e.num_matricula IN
	(SELECT num_matricula_supervisor FROM empregado);

--4)
SELECT d.nom_dependente FROM dependente AS d
WHERE d.num_matricula IN
	(SELECT e.num_matricula FROM empregado AS e
		WHERE e.num_matricula IN
			(SELECT dtp.num_matricula_gerente FROM departamento AS dpt));
--5)
SELECT dtp.nom_depto FROM departamento AS dpt
WHERE dtp.cod_depto NOT IN
	(SELECT dtpl.cod_depto FROM departamento_local AS dtpl);
