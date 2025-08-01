# Ontology Learning without Data Leakage

When evaluation ontology learning tools, many works use existing public ontologies. Especially for very popular ontologies, it is likely that the LLM has seen those ontologies and/or publications explaining those ontologies during training. Thus, this kind of evaluation does not guarantee that test data is not leaked.

We propose an alternative way of running ontology learning evaluations with LLMs: instead of using public ontologies, we suggest using an LLM to create test ontologies on the fly for one-time use. Re-running this process iteratively does not only allow for testing LLM-based tools in a way that prevents data leakage, but also for analyzing the tools' stability, e.g., by computing standard deviations.

![Overview of the approach](/img/schema.png)

The approach foresees generating ontologies from an input ontology on the fly, and running experiments with the generated ontologies. The generated ontologies should not be reused for further experiments.

# Provided files

This repository contains three folders:
- [prompts](/prompts) contains the prompts used both for ontology generation as well as for the experiments on taxonomy and domain/range induction.
- [ontologies](/ontologies) contains a set of ontologies created for experiments in the paper, and are solely present for reproducibility. They should not be reused for other experiments.
- [experiment_results](/experiment_results) contains the output of the LLMs that the results in the paper are based on
