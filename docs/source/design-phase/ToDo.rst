.. SoC Development Guides: ToDo List

*********
ToDo List
*********


SoC Phase 4
===========

This is a simple list of items to document as I think of them

* UPF
* Clocks
* Reset architecture (tradeoffs and recommendations)
* Implementation

  * Physically aware synthesis
  * Designer generate physical guidance to steer PnR
* RTL

  * Build Targets (ASIC/FPGA/GENERIC - which is the default/else case?)
  * Use ```ifdef SIMULATE`` for simulation specifics
  * Use ```ifdef UPF SVA`` etc.
  * Coding style based upon: https://github.com/lowRISC/style-guides/blob/master/VerilogCodingStyle.md
* CDC
* RDC
* X-Prop
* Linting

  * HAL doesn't trace through cells with ```celldefine``
  * Must therefore HAL lint both GENERIC and ASIC RTL views
  * Verilator can (probably) only LEC the GENERIC view
  * Style checking with: https://github.com/google/verible
* Verification

  * Power aware (UPF)
  * Formal Property Verification (FPV)
  * SVA (always use bind files)
  * Formal power check
  * Directed
  * Metric driven
  * Bug curves
  * Coverage
  * Root of trust
    
    * SYNTH RTL
    * MBIST RTL
    * Process
      
* LEC (against the root of trust)
* Automation
  
  * Jenkins
  * Jenkins job builder
* DFT
  
  * MBIST/MBISR
* Checklists
* PROCESS PROCESS PROCESS

* Packageing

  * Substrates
  * Stiffner ring

SoC Phase 5
===========

* Validation
