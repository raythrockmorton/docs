When you use {{ site.data.variables.product.prodname_codeql }} to scan code, the {{ site.data.variables.product.prodname_codeql }} analysis engine generates a database from the code and runs queries on it. Para obtener más información, consulta la sección "[Acerca de{{ site.data.variables.product.prodname_code_scanning }}](/github/finding-security-vulnerabilities-and-errors-in-your-code/about-code-scanning#about-codeql)".

{{ site.data.variables.product.prodname_codeql }} analysis uses a default set of queries, but you can specify more queries to run, in addition to the default queries. Las consultas que quieras ejecutar deberán pertenecer a un paquete de {{ site.data.variables.product.prodname_ql }} y pueden estar en tu propio repositorio o en cualquier repositorio público. Para obtener más información, consulta la sección "[Acerca de los paquetes de {{ site.data.variables.product.prodname_ql }}](https://help.semmle.com/codeql/codeql-cli/reference/qlpack-overview.html)".

Las consultas solo deberán depender de las bibliotecas estándar (es decir, aquellas referenciadas por una declaración `import LANGUAGE` en tu consulta), o de aquellas en el mismo paquete de {{ site.data.variables.product.prodname_ql }} que la consulta. Las bibliotecas estándar se ubican en el repositorio [github/codeql](https://github.com/github/codeql). For more information, see "[About CodeQL queries](https://help.semmle.com/QL/learn-ql/writing-queries/introduction-to-queries.html)."

Puedes especificar un solo archivo _.ql_, un directorio que contenga varios archivos _.ql_, un archivo de definición de suite de consulta _.qls_, o cualquier combinación de éstos. For more information about query suite definitions, see "[Creating {{ site.data.variables.product.prodname_codeql }} query suites](https://help.semmle.com/codeql/codeql-cli/procedures/query-suites.html)."

{% if currentVersion == "free-pro-team@latest" %}We don't recommend referencing query suites directly from the `github/codeql` repository, like `github/codeql/cpp/ql/src@main`. Such queries may not be compiled with the same version of {{ site.data.variables.product.prodname_codeql }} as used for your other queries, which could lead to errors during analysis.{% endif %}