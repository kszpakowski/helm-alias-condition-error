# Helm dependencies conditions error

This project contains 3 helm charts with dependencies, aliases and conditions.

Chart A is a simple chart without any dependencies,
Chart B conditionaly depends on chart A with an alias,
Chart C depends on B two times with different aliases.

When you render chart C `helm template chartC`, service account from chart A is being generated, against the condition in chart C values.
