The BP cloning reaction of Gateway Cloning requires that each DNA sample be concentrated enough to obtain 6-25 fmol by pipetting a minimum of 1 uL and maximum of 2 uL. If 6 fmol cannot be obtained from 2 uL, reaction efficiency may be negatively impacted, in which case you would need to concentrate your DNA. If 1 uL contains more than 25 fmol, you must dilute your sample so that 1-2 uL corresponds to 6-25 fmol. The purpose of this script is to automate these calculations for sample dilutions and volumes to add for the reaction. Note that the outputted dilutions and volumes are for a final DNA amount of 25 fmol.

#Input: spreadsheet that contains gene names (titled "Gene name"), DNA sequences (titled "BP cloning sequence"), and measured concentrations of the samples (titled "Concentration from Nanodrop (ng/uL)")

The script will perform the following process:

1.Add column for the ng needed to get 25 fmol gene fragment.
  
- ng needed to get 25 fmol gene fragment = (length of DNA sequence) x 0.0165

2. Add a dilution column. Add a column for the uL needed to pipet of the diluted or undiluted DNA sample.

3. Divide required nanograms by the concentration.

4. If the volume is approximately between 1-2 uL, this is the volume value. The dilution value is 'None'

- Otherwise, if the volume is greater than 2 uL: make this the volume value anyway, but print an error message that the sample is too dilute. The dilution value is 'None'

- Otherwise, if the volume is less than 1 uL: make a dilution (try 1/2X dilution first, then 1/3X, etc).

5. Add the dilution value to the dilution column (ex. 1/2X). Add the volume value to the volume column.

#Outputs a spreadsheet containing the required dilutions and sample volumes to add for the BP cloning reaction.
