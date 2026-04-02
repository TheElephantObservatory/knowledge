---
slug: managing-systemic-drift-through-continuous-autonomous-correction
title: "Managing Systemic Drift through Continuous Autonomous Correction"
subtitle: "Steering the machine back to its true north"
observer: "Mark Burgess"
observer_slug: mark-burgess
source_title: "EP28 Mark Burgess on Promise Theory, AI & Spacetime"
source_url: "https://www.youtube.com/watch?v=jOZzi1Wj0ks"
source_author: "The Jim Rutt Show"
tags: [Systems Thinking, Process Philosophy, Complexity Science]
edges:
  - target: optimal-adaptation-at-the-edge-of-chaos
    type: extends
created_at: "2026-03-18"
---

# Managing Systemic Drift through Continuous Autonomous Correction

Steering the machine back to its true north

---

> Computer systems don't stay where you put them — they drift. Mark Burgess's maintenance theorem reframes system management as physics: define the desired state, then let an autonomous agent continuously steer reality back toward it.

One of the deepest insights behind cfengine — and what later became promise theory — is what Mark Burgess calls the 'maintenance theorem': the idea that you should never think of a computer system as a machine that does what you tell it, but rather as a *phenomenon* that exists in a state space and drifts away from desired states over time due to entropy, interference, and network effects. The standard computer science story is that computers do exactly what we program them to do. But anyone who has actually worked with computers knows that is an extraordinarily optimistic and idealized view. Once you connect machines to a network, it's no longer just what you programmed your machine to do — it's what every neighboring machine is doing, how they're sharing resources, how external agents are modifying state. The system becomes genuinely complex and somewhat unpredictable. Burgess's insight was to stop fighting this and instead model it honestly: specify the *intended end state* of the system in a high-level declarative way — what it's supposed to look like, what security settings it should have, who the allowed users are — and then build an intelligent agent that wakes up, investigates its environment, adapts to it, and continuously steers the system back toward that desired state. This is essentially a physics framing: you're not issuing commands, you're defining an attractor in configuration space and letting the system roll toward it. The maintenance theorem formalizes this — a system under continuous autonomous correction can maintain equilibrium against entropy and interference through something analogous to detailed balance in statistical mechanics. This reframing, from imperative command to declarative intention, from one-time programming to continuous self-correction, is the conceptual seed that eventually grew into promise theory and influenced everything from Puppet and Chef to Kubernetes.

## Apprentice

Most people assume computers do exactly what they're told. Write a program, the machine follows instructions, done. But anyone who has managed real systems — especially networked ones — knows this is a fantasy. Other machines interfere, software updates collide, configurations drift, unexpected agents modify things. The system you built yesterday is subtly different today, and different again tomorrow.

Mark Burgess noticed this and drew a radical conclusion: stop pretending computers are obedient machines and start treating them as physical phenomena that naturally drift away from the state you want. His answer was to describe the desired end state — what the system should look like, what settings it should have — and then deploy a small autonomous agent that wakes up repeatedly, checks what's actually there, and nudges things back toward that description.

This shift from giving commands to declaring intentions turns out to be enormously powerful. Instead of a fragile script that breaks when reality doesn't match expectations, you get a self-correcting system that absorbs disturbances and keeps finding its way back. The idea seeded an entire generation of infrastructure tools — Puppet, Chef, Kubernetes — and the underlying theory eventually became promise theory, a formal framework for reasoning about how autonomous agents cooperate.

## Adept

The standard imperative model of computing assumes a closed, deterministic system: instructions execute, state changes predictably, outcomes are fully specified by the program. This model breaks down catastrophically in networked, multi-agent environments where external processes, shared resources, and concurrent modifications make global state genuinely non-deterministic. Mark Burgess formalized this breakdown in what he calls the maintenance theorem, the conceptual core of both cfengine and the later promise theory.

The theorem reframes system administration through a physics lens. Rather than issuing imperative commands — do this, change that — an operator specifies a desired configuration as a declarative policy: a point or region in the system's configuration space. An autonomous agent then runs continuously, sampling actual state, computing the divergence from the declared intent, and applying corrective actions. The system is modeled not as a machine executing instructions but as a dynamical system subject to entropic drift, with the agent functioning as a restoring force. Burgess draws an explicit analogy to detailed balance in statistical mechanics: under continuous autonomous correction, a system can maintain statistical equilibrium against perturbation.

This reframing — from imperative to declarative, from one-shot execution to continuous convergence — had profound practical consequences. It produced infrastructure tooling that is robust to partial failure and environmental noise, because correctness is defined as a persistent attractor rather than a completed sequence. The conceptual lineage runs directly from cfengine through Puppet, Chef, Ansible, and into the reconciliation loops that are the architectural heart of Kubernetes. Promise theory later generalized the framework, providing formal semantics for how autonomous agents make and honor commitments without central coordination.

## Magus

Classical computer science inherits a command-execution epistemology from its mathematical foundations: a Turing machine is a closed, deterministic transducer, and correctness is defined relative to a halting state reachable by a finite instruction sequence. This ontology becomes untenable in open, networked systems where state is continuously perturbed by exogenous agents, resource contention, and cascading network effects. Mark Burgess's maintenance theorem constitutes a formal repudiation of this epistemology and its replacement with a dynamical systems framing borrowed from statistical physics.

The theorem's core claim is that a managed system should be modeled as a stochastic process evolving over a high-dimensional configuration space, subject to entropic drift away from operationally desired regions. The administrator's role is reconceived as specifying an intended invariant — a target manifold in configuration space — rather than a procedural path toward it. A continuously executing autonomous agent samples system state, computes deviation from the declared policy, and applies corrective actions, functioning as a feedback controller that enforces something analogous to detailed balance: the net probability flux away from the desired state is counteracted by the restoring flux of autonomous correction, yielding a non-equilibrium steady state. Burgess is explicit that this is not metaphor but a structural isomorphism with thermodynamic equilibrium maintenance.

The epistemological consequences are significant. Declarative policy specification decouples intent from mechanism, making correctness invariant under environmental perturbation rather than contingent on execution path. This is the conceptual architecture that promise theory later axiomatizes: agents make unilateral promises about their own behavior, and system-level properties emerge from the composition of those promises without requiring global coordination or shared mutable state. The influence on distributed systems engineering — from configuration management to Kubernetes's reconciliation loop model — represents one of the more consequential transfers of physical intuition into software architecture of the past three decades.
