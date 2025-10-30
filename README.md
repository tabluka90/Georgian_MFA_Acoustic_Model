This repository contains a Georgian acoustic model trained for use with Montreal Forced Aligner (MFA).
The model can be used for forced alignment of Georgian speech, allowing conversion of audio and transcripts into time-aligned phone and word sequences.


 Model Overview
----------------------
Language: Georgian
Phone set: XPF (compatible with MFA Georgian dictionary)
Training data: Common Voice Corpus 22.0 Georgian, ~116,586 utterances (~586k seconds) across 2,316 speakers 

Contents
----------------------
ka_v3.zip – Georgian acoustic model
ka_v3.dict – Dictionary

Usage
----------------------
You should have installed and running MFA on your machine.

To Run forced alignment on a corpus, simply download new acousti model and dictionary, put it in your path and run it with mfa align command.
mfa align [OPTIONS] CORPUS_DIRECTORY DICTIONARY_PATH ACOUSTIC_MODEL_PATH
          OUTPUT_DIRECTORY

Example:
mfa align /myfiles/mfa/audio_corpus \
          /myfiles/mfa/ka_v3.dict \
          /myfiles/mfa/ka_v3.zip \
          /myfiles/mfa/output_aligned
          --clean \
          --single_speaker \
          --beam 4000 \
          --retry_beam 16000

          
Citation
----------------------
@misc{Tabagari_2025,
    author       = {Tabagari, Luka},
    title        = {Georgian Acoustic Model and Dictionary for Montreal Forced Aligner},
    howpublished = {\url{https://github.com/tabluka90/Georgian_MFA_Acoustic_Model}},
    publisher    = {GitHub},
    year         = {2025},
    month        = {Oct}
}
