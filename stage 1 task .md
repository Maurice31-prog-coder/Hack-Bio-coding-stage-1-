\# function for translating DNA to Protein

def dna\_transcription(dna\_sequences):

    """Convert a DNA sequence into an mRNA sequence by replacing Thymine (T) with Uracil (U)."""

    return dna\_sequences.replace('T', 'U') 

print(dna\_transcription("ATCGAAACTTTGCAAGGCTT"))

def translate\_rna(rna\_sequence):

    # Define the codon table with three-letter amino acid codes using dictionary

    Rna\_codon = {

        'AUA':'Ile', 'AUC':'Ile', 'AUU':'Ile', 'AUG':'Met',

        'ACA':'Thr', 'ACC':'Thr', 'ACG':'Thr', 'ACU':'Thr',

        'AAC':'Asn', 'AAU':'Asn', 'AAA':'Lys', 'AAG':'Lys',

        'AGC':'Ser', 'AGU':'Ser', 'AGA':'Arg', 'AGG':'Arg',

        'CUA':'Leu', 'CUC':'Leu', 'CUG':'Leu', 'CUU':'Leu',

        'CCA':'Pro', 'CCC':'Pro', 'CCG':'Pro', 'CCU':'Pro',

        'CAC':'His', 'CAU':'His', 'CAA':'Gln', 'CAG':'Gln',

        'CGA':'Arg', 'CGC':'Arg', 'CGG':'Arg', 'CGU':'Arg',

        'GUA':'Val', 'GUC':'Val', 'GUG':'Val', 'GUU':'Val',

        'GCA':'Ala', 'GCC':'Ala', 'GCG':'Ala', 'GCU':'Ala',

        'GAC':'Asp', 'GAU':'Asp', 'GAA':'Glu', 'GAG':'Glu',

        'GGA':'Gly', 'GGC':'Gly', 'GGG':'Gly', 'GGU':'Gly',

        'UCA':'Ser', 'UCC':'Ser', 'UCG':'Ser', 'UCU':'Ser',

        'UUC':'Phe', 'UUU':'Phe', 'UUA':'Leu', 'UUG':'Leu',

        'UAC':'Tyr', 'UAU':'Tyr', 'UAA':'Stop', 'UAG':'Stop',

        'UGC':'Cys', 'UGU':'Cys', 'UGA':'Stop', 'UGG':'Trp'

    }

   # Process the RNA sequence in groups of 3 (codons)

protein = "" # this define the protein outside the for loop

rna\_sequence = \["AUCGAAACUUUGCAAGGCUU"]

for i in range(0, len(rna\_sequence), 3):

    codon = rna\_sequence\[i:i+3] # for the sliced sequence

    amino\_acid = Rna\_codon.get(codon, '?') # Get the corresponding amino acid

    protein += RNA\_codon\[codon]

    if amino\_acid == 'Stop': # Stop translation if stop codon is found

            break

    protein += amino\_acid # Append amino acid to protein sequence

print(protein)

https\://github.com/Emmanueladewuyi/Hackbio-Bio-coding-Internship-.git
