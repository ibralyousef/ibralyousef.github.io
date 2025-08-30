---
layout: umq-event
title: "Review of 'Coplanar Waveguide Resonators for Circuit Quantum Electrodynamics'"
presenter: "Mahmoud Almansouri, PhD Candidate @ KAUST"
event_date: 2025-08-27
time: "4:30 PM - 6:30 PM"
location: "Zoom & Jeddah Initiative Hub"
reading_material: "Coplanar Waveguide Resonators for Circuit Quantum Electrodynamics"
reading_url: "https://qudev.phys.ethz.ch/static/content/science/papers/Goeppl2008.pdf"
show_as_next: false
hidden: false
registration_url: "https://forms.gle/cWizbj2dNbD5GPSH7"
abstract: |
  Resonators are fundamental components in superconducting quantum circuits, enabling qubit readout, photon storage, and coherent qubit-qubit coupling in circuit quantum electrodynamics (cQED). Among the two main types—lumped element and coplanar waveguide (CPW) resonators—CPWs offer better frequency control, reduced parasitics, and straightforward 50 Ω integration. This seminar focuses on CPW resonators and their practical integration with qubits, emphasizing key design parameters such as coupling capacitance, external quality factor, and mode frequency. We base our discussion on the foundational design framework established by Göppl et al., and extend it to practical implementation using HFSS, COMSOL, or Maxwell 3D to extract capacitance matrices, control cross-talk, and ensure accurate frequency and quality factor targeting in quantum processors.
---

## Reading Material

[{{ page.reading_material }}]({{ page.reading_url }})

## Abstract

{{ page.abstract }}

## Session Recording

<video width="100%" controls>
  <source src="/assets/videos/coplanar-waveguide-session.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

## Presentation Slides

[Download Presentation (PowerPoint)](/assets/presentations/coplanar-waveguide-presentation.pptx)

## Recommended Resources

### Foundational Text (Beginner to Intermediate)

**[Quantum Computation and Quantum Information](/assets/resources/nielsen-chuang-quantum-computation.pdf)** by Michael Nielsen & Isaac Chuang  
Often referred to as "Mike and Ike," this is the standard textbook in quantum information science. With over 58,000 citations, it provides a comprehensive introduction assuming minimal prior knowledge of quantum mechanics or computer science. Covers fundamental topics including quantum circuits, quantum algorithms (Fourier transform, search), quantum noise, error correction, and information theory. Essential for building a strong theoretical foundation.

### Hardware and Implementation (Intermediate to Advanced)

**[A Quantum Engineer's Guide to Superconducting Qubits](/assets/resources/quantum-engineers-guide-superconducting-qubits.pdf)** by Krantz et al. (2019)  
An introductory guide bridging fundamental concepts with contemporary applications in quantum computing. Reviews 20 years of evolution from basic research to engineering large-scale quantum systems. Covers superconducting circuit design, qubit control, readout techniques, noise properties, and circuit quantum electrodynamics (cQED). Ideal for understanding the hardware implementation of quantum computers.

**[Introduction to Experimental Quantum Measurement with Superconducting Qubits](/assets/resources/experimental-quantum-measurement-superconducting-qubits.pdf)** by Mahdi Naghiloo (2019)  
A pedagogical introduction to quantum measurement in superconducting systems, exploring the dynamics of single qubits under continuous monitoring. Covers experimental quantum dynamics, quantum thermodynamics, and weak measurement techniques. Provides an in-depth experimental perspective essential for those working with physical quantum systems.

### Practical Applications (Advanced)

**[Practical Introduction to Benchmarking and Characterization of Quantum Computers](/assets/resources/benchmarking-characterization-quantum-computers.pdf)** by Hashim et al. (2025)  
A comprehensive tutorial on quantum characterization, verification, and validation (QCVV) tools. Designed for both newcomers and experts, it provides essential techniques to evaluate and enhance quantum computing performance. Critical for understanding how to assess the quality and reliability of quantum computations in practice.