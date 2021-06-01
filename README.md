---
description: v0.1.0.1-beta-3.1 for epispot v2.1.1
---

# The epispot manual

**This manual is currently in development. Unlinked sections have not been created yet.**

This is the official manual to the epispot package. It includes background information on the mathematical modeling of infectious diseases, the motivation behind the epispot package, a complete guide to using epispot and understanding its documentation, and a full explanation of the epispot development process. As epispot grows, this manual is subject to change and will be versioned on the [GitHub repo](https://github.com/epispot/manual/releases). This current version of the manual is maintained at [https://github.com/epispot/manual](https://github.com/epispot/manual) and ported to both HTML and PDF formats via GitBook.

## Table of Contents

1. [Compartmental Models in Epidemiology](ch1.md)
   * 1.1 [Basic Disease Models](ch1.md#1-1-basic-disease-models)
   * 1.2 [Related Modeling Techniques](ch1.md#1-2-related-modeling-techniques)
     * 1.2.1 [Agent-based Modeling](ch1.md#1-2-1-agent-based-modeling)
     * 1.2.2 [Compartmental Models](ch1.md#1-2-2-compartmental-models)
   * 1.3 [The SIR Model](ch1.md#1-3-the-sir-model)
     * 1.3.1 [Motivation](ch1.md#1-3-1-motivation)
     * 1.3.2 [Definitions](ch1.md#1-3-2-definitions)
     * 1.3.3 [Derivation](ch1.md#1-3-3-derivation)
     * 1.3.4 [In Practice](ch1.md#1-3-4-in-practice)
2. [The Structure of epispot](ch2.md)
   * 2.1 [Visualizing Compartmental Models](ch2.md#2-1-visualizing-compartmental-models)
     * 2.1.1 [The SIR Model](ch2.md#2-1-1-the-sir-model)
     * 2.1.2 [Expanding Models](ch2.md#2-1-2-expanding-models)
     * 2.1.3 [More Complex Models](ch2.md#2-1-3-more-complex-models)
   * 2.2 [Epispot's Layer Combination Rules](ch2.md#2-2-epispots-layer-combination-rules)
   * 2.3 [Compiling Models with epispot](ch2.md#2-3-compiling-models-with-epispot)
     * 2.3.1 [The Basics: Pre-compiled Models](ch2.md#2-3-1-the-basics-pre-compiled-models)
     * 2.3.2 [Playing with the Model](ch2.md#2-3-2-playing-with-the-model)
     * 2.3.3 [Compiling the SIHRD Model](ch2.md#2-3-3-compiling-the-sihrd-model)
3. [Contributing Guidelines](ch3.md)
   * 3.1 [Introduction](ch3.md#3-1-introduction)
   * 3.2 Installation
     * 3.2.1 Cloning from VCS
     * 3.2.2 Environment Setup
     * 3.2.3 Building from source
   * 3.3 Structure
     * 3.3.1 Repository Structure
     * 3.3.2 Package Structure
   * 3.4 Development
     * 3.4.1 Testing & Code Coverage
     * 3.4.2 Documentation
     * 3.4.3 Security
     * 3.4.4 VCS Notes
   * 3.5 Contributing to this Manual
4. Credits
   * 4.1 Open-Source Policy
   * 4.2 Licensing
   * 4.3 Citations
   * 4.4 Idea & Inspiration
   * 4.5 Dependencies
   * 4.6 External Code Management Tools

