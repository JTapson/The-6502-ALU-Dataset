# The-6502-ALU-Dataset

This dataset was generated to reproduce the input-output performance of the MOS Technology 6502 ALU.  The dataset consists of four files:

ALU_in_train - Input training data.

ALU_out_train - Corresponding outputs for the inputs in ALU_in_train.

ALU_in_test - Input testing data.

ALU_out_test - Corresponding outputs for the inputs in ALU_in_test.

The data formats are:

Input - 23 binary bits (columns) and approximately 650000 samples (rows).  The column order is:

SUM AND EOR OR SR DAA I/ADDC A7 A6 ... A1 A0 B7 B6 ... B1 B0

Output - 11 binary bits x approximately 650000 rows, corresponding to the input data rows.  The column order is:

AVR ACR HC ADD7 ADD6 ... ADD1 ADD0
