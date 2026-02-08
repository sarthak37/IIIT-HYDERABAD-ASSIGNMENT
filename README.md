1. Installation (Windows)
   -> Open Anaconda Prompt and run:
      conda create -n mfa -c conda-forge montreal-forced-aligner -y
      conda activate mfa
    -> Verify installation:
       mfa --help
2.  Dataset Preparation
   -> Each audio file must have a matching transcript file with the same name inside a speaker folder.

3.  Download Models
   -> mfa model download acoustic english_us_arpa
   -> mfa model download dictionary english_us_arpa
   -> mfa model download g2p english_us_arpa

4. Forced Alignment (Before OOV)
   Validate corpus:-  mfa validate C:\Users\sarth\OneDrive\Desktop\mfa_project\data english_us_arpa english_us_arpa
   Run alignment:- mfa align C:\Users\sarth\OneDrive\Desktop\mfa_project\data english_us_arpa english_us_arpa C:\Users\sarth\OneDrive\Desktop\mfa_project\output

   mfa validate C:\Users\sarth\OneDrive\Desktop\mfa_project\data english_us_arpa english_us_arpa

   mfa align C:\Users\sarth\OneDrive\Desktop\mfa_project\data english_us_arpa english_us_arpa C:\Users\sarth\OneDrive\Desktop\mfa_project\output

   mfa validate C:\Users\sarth\OneDrive\Desktop\mfa_project\data english_us_arpa english_us_arpa > validate_before.txt

5. After OOV
   
   mfa align ^
More?   C:\Users\sarth\OneDrive\Desktop\mfa_project\data ^
More?   english_us_arpa ^
More?   english_us_arpa ^
More?   C:\Users\sarth\OneDrive\Desktop\mfa_project\output_after_oov ^
More?   --custom_dictionary C:\Users\sarth\OneDrive\Desktop\mfa_project\oov.dict






   

