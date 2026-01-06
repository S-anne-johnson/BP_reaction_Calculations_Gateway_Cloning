#Input: spreadsheet that contains gene names (titled "Gene name"), DNA sequences (titled "BP cloning sequence"), and measured concentrations of the samples (titled "Concentration from Nanodrop (ng/uL)")

#The script will perform the following process:

  #Add column for the ng needed to get 25 fmol gene fragment.
      #ng needed to get 25 fmol gene fragment = (length of DNA sequence) x 0.0165

  #Add a dilution column. Add a column for the uL needed to pipet of the diluted or undiluted DNA sample.
      #Divide required nanograms by the concentration.
        #If the volume is approximately between 1-2 uL, this is the volume value. The dilution value is 'None'
        #Otherwise, if the volume is greater than 2 uL: make this the volume value anyway, but print an error message that the sample is too dilute. The dilution value is 'None'
        #Otherwise, if the volume is less than 1 uL: make a dilution (try 1/2X dilution first, then 1/3X, etc).
          #Add the dilution value to the dilution column (ex. 1/2X). Add the volume value to the volume column.

  #Outputs a spreadsheet containing the required dilutions and sample volumes to add for the BP cloning reaction.
