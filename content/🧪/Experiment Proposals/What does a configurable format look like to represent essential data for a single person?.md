---
date: 2024-04-26
---

**Estimated Time To Create:** 2 days

# Summary

The current landscape of personal data management is fragmented, with individual information scattered across multiple third-party platforms. This project aims to address the lack of a universally accessible and individual-controlled format for managing personal data. By developing a minimal viable product (MVP) that utilizes a simple YAML file, this experiment proposes to consolidate various personal data points into a single, individual-controlled document. This approach would shift control back to the individual, allowing for a more integrated and self-managed system of personal data, which encompasses IDs, medical records, digital footprints, software data, and even vectorized or translated versions of personal content like artwork.

# Related Work

This initiative is inspired by several existing systems, including OpenAI's [open source evaluation](https://github.com/openai/evals) configurations that use `yaml` for describing the eval setup and `.jsonl` for input data, as well as the data storage practices of big entities like the U.S. government, Apple, and Google. Common data export formats from social platforms like LinkedIn also seem helpful.

CRUD operation (Create, Read, Update, and Delete) also seem pretty standard and sufficient. 

# Risks

The primary risks associated with this experiment involve the challenges of keeping the YAML document updated as external data changes over time. This probably requires maintaining integrations that can adapt to changes in personal data across various platforms without compromising the integrity or control of the data by the individual. 

Ensuring the document's usability and the individual's satisfaction with managing their own data through this new format are also critical to the project's success.

# Questions for experiments that will de-risk the project

1. How can we ensure that the YAML file remains synchronized with real-time changes in personal data?
2. What mechanisms can be implemented to automate updates to the YAML file while ensuring the individual's control over the process?
3. Are there specific security measures that need to be integrated into the YAML configuration to protect sensitive personal data?
4. Do we store different formats of the same data "object"? If not, which format is the source of truth? Example: A photo of the self that is represented both through its metadata, unique id, jpg, and vectorized version. 

# Evaluation

The evaluation plan for this first experiment focuses on a handwave-y variable: my personal satisfaction while using such a file. 

The implementation of the YAML configuration will be tested through tasks related to compiling and managing personal data within the file. Since I use Obsidian, I'll likely compile the information in the frontmatter of a Markdown to start and then migrate that over to YAML at some point. 

The success of this configuration will be measured by its ability to enhance the user's control and organization of their personal data. Monitoring these factors will help assess the feasibility of this approach and its potential for broader application and integration with various data sources.



