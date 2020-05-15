************************
Verification Review Form
************************

TBC - Just notes for now


Process
=======

This section attempts to explore the verification process.
This can be considered as **The what**

Strategy
--------

#. Where is the verification strategy document defined?
   * E.g. Block based unit testing + top level integration and system testing"
		
Verification Plans
------------------

#. Requirements & Feature Extraction
   * Verification checks that the SoC meets the SoC specs.
     The features to be verified must be extracted from the specs.
     i.e. What is to be verified?

#. Test Case Management System (TCMS)
   * What format are the features to be verified stored in?
     e.g. simple spreadsheet or a TCMS (TestLink/TestRail/VManager)

#. Coverage matrix
   * Where is the feature / functional coverage matrix?
     The TCMS should provde the coverage matrix
     i.e. of the features to test, what has and hasn't been tested?

#. Categories
   * Have all verification categories been considered (i.e. not just
     functional testing)? E.g.
     * Functional
     * DFT (Stuck-at scan / Transition Fault Testing / IDDQ Testing / Memory BIST & BISR /Boundary Scan)
     * Power Domains
     * Clock Domain Crossing
     * Reset Domain Checking


Methodology
===========

This section attempts to explore how the verification has been done to ensure robustness, repeatability and quality.
This can be considered as **The how**

Root of trust
-------------

#. Synthesis RTL verified
   * This check poses the simple question: Have we verified what we're building?
     E.g. Have we verified the ASIC (SYNTHESIS) RTL view or just the behavioural and/or FPGA views?
     Given that we equivalence check the netlist to the SYNTHESIS RTL view we must fully verifiy that view as it is the root of trust"
		
Automation
----------

#. Self-checking regressions
   * Has all verification been re-run on the final RTL?
   * Continuous Integration - Has CI (e.g. Jenkins) been used to ensure repeatable automated testing?
		
Checklists & Reviews
--------------------

#. Have basic checklists been completed?
   E.g. Checklist Question: Do all designs use or assume the same style of reset?"
		
Models
------

#. Analog / memories / IO / PLL / SerDes etc.
   * Where simulation models have been used (e.g. analog) have they been checked/reviewed to be consistent with their implementation?
		
Verification Types
------------------

#. Foreach verification category, what verification types are deployed?
   For those types not deployed, provide justification as why it is safe not
   to deploy them
   * Directed Simulation
   * Metric driven / constrained random
   * Formal property
   * UPF Dynamic & Formal
   * ABV - Assertion Based Verification
   * CDC - Clock Domain Crossing
   * RDC - Reset Domain Checking
   * X-prop - X Propagation Checking
   * Linting
   * FPGA prototyping
   * Emulator
   * Verilator model


Quality Metrics
===============

This section attempts to answer the simple question of: Is verification
complete?

Bug Curves
----------

Graphs of bugs found over time are a good metric for verification completeness.
* Are they available?
* Do they show a flattening off trend?"

Bug Tickets
-----------

* Are all bug tickets (e.g. JIRA) in the FIXED or WONTFIX state?

Code coverage metrics
---------------------

* Are code coverage metrics available?
* Are they at an acceptable level?"

Functional coverage metrics
---------------------------

* Are functional coverage metrics (from the TCMS) available?
* Have all deficiencies been accepted at waived?"

Gut Feel
--------

Lastly, provide and honest "gut feel" assessment of the verification completeness
