---
layout: default
title: Projects
---

## LUNA — Latent Untargeted Network Annotation

Mass spectrometry measures mass-to-charge ratios of compounds in a sample. Determining which molecular formulas could produce a given observed mass is equivalent to a subset sum problem — NP-hard in the general case. Brute force enumeration scales as O(N<sup>k</sup>), making it intractable for comprehensive element sets. Existing tools like SIRIUS and Rdisop are limited to ~10 elements or fewer.

LUNA restates this as a signal processing problem. By defining generating functions for each element as Dirac combs bounded by search parameters, the full combinatorial space can be computed via the convolution theorem in O(k log k) time. A mixed-radix encoding scheme stores element counts in the phase component of each generating function, allowing recovery of exact elemental compositions for every bin with non-zero magnitude.

The FFT approach introduces aliasing: when multiple element combinations sum to the same value at a given grid resolution, phases are corrupted. A dual encoding approach inspired by the Chinese Remainder Theorem detects aliasing, which can be minimized by using sufficiently high grid resolutions and by mixing the FFT approach with traditional enumeration of common elements.

Written in Python leveraging highly optimized FFT libraries. Developed on a custom Threadripper Pro workstation with a persistent memory (pmem) accelerated ZFS array for efficient result storage and querying. The result is a formula enumeration engine that can search 20+ elements simultaneously, far exceeding the capabilities of any existing tool. Manuscript in preparation.

---

## Homelab Infrastructure

I am passionate about data privacy and sought to minimize my dependency on big-tech cloud-hosted services. Building a home cluster also serves as a dev environment to learn about virtualization and cloud technologies, and to prototype distributed computing projects at home.

Three machines were built from e-waste commodity components to minimize cost. Both converged and hyperconverged architectures were explored using combinations of ZFS and Ceph with 10 Gbps Ethernet or 56 Gbps Infiniband before settling on a pseudo-HA configuration based on 10 Gbps and ZFS replication. Optane persistent memory, NVRAM accelerators, and other exotic hardware is employed as needed to meet the performance requirements of various projects.

Raspberry Pis, used for initial iterations of the cluster, serve as lower-power worker nodes for Dask. Bulk storage is provided by replicated TrueNAS instances. Networking is managed using the Unifi ecosystem. The cluster currently runs Proxmox and hosts self-hosted LLMs, private cloud services, and development environments.

---

## C.A.R.S. — Cellular Automata Rafting Simulation

C.A.R.S. was my solution to the 2012 COMAP Mathematical Competition in Modeling (MCM) discrete mathematics problem. The challenge was to maximize the number of customers able to take rafting trips on a hypothetical river using various forms of travel.

Rather than focusing on a scheduling optimization algorithm such as simulated annealing, I developed a cellular automata-based simulation that treats the river as a series of bins evolving over time using a mixture of hard-coded rules and heuristics. The model included a layer for simulating weather and adverse events while also maximizing visitor enjoyment, parameterized by various metrics. I implemented the solution in Perl and used my lab's HPC resources to evaluate a wide range of conditions to arrive at an optimal rule set.

Our solution greatly outperformed competing entries that year. Our team was awarded "Outstanding Winner" — a distinction given to only 10 of 3600+ competing teams — and received the SIAM Award. We were invited to present our results at the SIAM Annual Meeting in Minneapolis, and the solution was later published in the *Harvard College Mathematics Review*.
