# Utilities

Here is a list of utility scripts to aid with debugging and maintenance:


## Memory checking

  1. Put the following lines in your configuration file 
  ```
  process.SimpleMemoryCheck = cms.Service("SimpleMemoryCheck",ignoreTotal = cms.untracked.int32(1) )
  ```
  2. Run you configuration into a log file
  ```
  cmsRun yourfile.py >& log_name
  ```
  3. Generate a macro root file via the script:
  ```
  ./memorycheck.csh log_name
  ```
  4. Deploy the output file
  ```
  root -l -b -q draw.C
  ```
  5. output file is shown in check.pdf

p.s. More information in https://twiki.cern.ch/twiki/bin/view/CMSPublic/SWGuideTroubleShootingMore
