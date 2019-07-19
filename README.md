# The-6502-ALU-Dataset

This dataset was generated to reproduce the input-output performance of the MOS Technology 6502 ALU.  The dataset consists of four files:

ALU_in_train - Input training data.

ALU_out_train - Corresponding outputs for the inputs in ALU_in_train.

ALU_in_test - Input testing data.

ALU_out_test - Corresponding outputs for the inputs in ALU_in_test.

The data formats are:

Input - 23 binary bits (columns) and approximately 650000 samples (rows).  The column order is:

SUM AND EOR OR SR DAA I/ADDC A7 A6 A5 A4 A3 A2 A1 A0 B7 B6 B5 B4 B3 B2 B1 B0

Output - 11 binary bits x approximately 650000 rows, corresponding to the input data rows.  The column order is:

AVR ACR HC ADD7 ADD6 ADD5 ADD4 ADD3 ADD2 ADD1 ADD0

I suggest for Python processing you import the .mat file - typical code below:

mat = spio.loadmat('ALU_6502.mat')

x_train = mat['ALU_in_train']/1.0

y_tr = np.array(mat['ALU_out_train'])

y_train = y_tr[:,10]

x_test = mat['ALU_in_test']/1.0

y_te = np.array(mat['ALU_out_test'])

y_test = y_te[:,10]
