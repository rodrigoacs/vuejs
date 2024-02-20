<template>
  <div>
    <h2 class="header">Rodrigo Augusto Correa Soares</h2>
    <p class="socials">
      <span> 14/05/2003</span>
    </p>
    <p class="socials">
      <span> MINAS GERAIS, BRASIL</span>
    </p>
    <p class="socials">
      <a
        target="_blank"
        href="mailto:rodrigohths@gmail.com"
      >rodrigohths@gmail.com</a>
      <a
        target="_blank"
        href="https://github.com/rodrigoacs"
      >&nbsp;|&nbsp;GitHub&nbsp;|&nbsp;</a>
      <a
        target="_blank"
        href="https://www.linkedin.com/in/rodrigoacsoares/"
      > LinkedIn | </a>
      <a
        target="_blank"
        href="https://rodrigoacs.com"
      >&nbsp;Site</a>
    </p>

    <h3>Resumo</h3>
    <p>
      Estou cursando o terceiro período de Sistemas de Informação no IFMG Campus Ouro Branco. Tenho
      interesse em aprimorar minhas habilidades técnicas em desenvolvimento backend e/ou fullstack.
      Atualmente trabalho como estagiário de engenharia de dados construindo soluções de integração
      de dados voltadas ao setor terciário, especialmente de varejo, no Brasil.
    </p>

    <h3>Formação</h3>
    <p>
      JANEIRO DE 2018 - ABRIL DE 2021 (CONCLUÍDO)<br />IFMG, Congonhas MG<br />Técnico Integrado em
      Mecânica
    </p>
    <br />
    <p>
      SETEMBRO DE 2022 - (CURSANDO)<br />IFMG, Ouro Branco MG<br />Bacharelado em Sistemas de
      Informação
    </p>

    <h3>Experiência</h3>
    <p>FEVEREIRO DE 2023 - ATUALMENTE<br />CLI Consultoria - Estagiário - Desenvolvimento ETL</p>
    <p>
      Construção de integrações de dados entre bancos de dados relacionais e APIs baseadas em
      MongoDB, manutenção em aplicações legado, gerenciamento de pipeline de dados. Suporte técnico
      interno para sistemas Linux (Ubuntu, CentOS). Gerenciamento de instâncias AWS EC2.
    </p>

    <h3>Linguagens, ferramentas e softwares</h3>
    <p>&gt; SQL, JavaScript(Node.js), Python, HTML, CSS, Java e C.</p>
    <p>&gt; Pentaho Data Integration, Postman, DBeaver e SAPGUI.</p>
    <p>&gt; RDBMS: Oracle, PostgreSQL e MySQL.</p>
    <p>&gt; Inglês intermediário.</p>
  </div>
</template>

<script setup></script>

<style scoped>
h3 {
  margin-top: 2rem;
}

.header {
  display: flex;
  align-items: center;
  margin-bottom: 1rem;
  margin-top: 2rem;
}

div a,
div li {
  color: var(--color-text-secondary);
}

.socials {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  text-align: justify;
  color: var(--color-text-secondary);
}
</style>
