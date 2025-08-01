# Ontology Learning without Data Leakage
When evaluation ontology learning tools, many works use existing public ontologies. Especially for very popular ontologies, it is likely that the LLM has seen those ontologies and/or publications explaining those ontologies during training. Thus, this kind of evaluation does not guarantee that test data is not leaked.

We propose an alternative way of running ontology learning evaluations with LLMs: instead of using public ontologies, we suggest using an LLM to create test ontologies on the fly for one-time use. Re-running this process iteratively does not only allow for testing LLM-based tools in a way that prevents data leakage, but also for analyzing the tools' stability, e.g., by computing standard deviations.
