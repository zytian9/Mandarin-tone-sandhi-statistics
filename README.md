
---

# Mandarin Tone Sandhi Realization: Evidence from Large Speech Corpora

## Dataset

### Free ST Chinese Mandarin Corpus (Speaker Info)
This corpus was recorded in a quiet, indoor environment using a cellphone. It includes 855 speakers, each contributing 120 utterances. All utterances were meticulously transcribed and verified by human annotators, ensuring transcription accuracy.

**Speaker Data Example**:  
20170001P00189I0036 | Gender: Female | Age: 31 | Region: Sichuan | Utterance: 我有两张君悦皇家浴场  
- P00189I: Speaker number  
- 0036: Speech number  

[Free ST Chinese Mandarin Corpus](http://www.openslr.org/38/)

### MAGICDATA Mandarin Chinese Read Speech Corpus (Read Speech) (Speaker Info)
Developed by Magic Data Technology Co., Ltd., this corpus contains 755 hours of scripted read speech data from 1080 native Mandarin speakers from mainland China. The sentence transcription accuracy exceeds 98%.

[MAGICDATA Mandarin Chinese Read Speech Corpus](http://www.openslr.org/68/)

### aidatatang_200zh
This corpus includes:
- 200 hours of mostly mobile-recorded acoustic data.
- 600 speakers from various accent regions in China.
- Transcription accuracy for each sentence is over 98%.
- Recordings were made in quiet indoor settings.
- The database is split into a training set, validation set, and testing set in a 7:1:2 ratio.
- Detailed information such as speech data coding and speaker information is included in the metadata file.
- Segmented transcripts are provided.

[aidatatang_200zh](http://www.openslr.org/62/)

## Process Pipelines

### Metadata Statistics

### Forced Alignment
We utilized Charsiu for vowel-level forced alignment. Since the authors of Charsiu have released the textgrid files we require, we directly used their alignment files.

[Charsiu Forced Alignment](https://github.com/lingjzhu/charsiu/blob/main/misc/data.md#alignments-for-mandarin-speech-datasets)

### Segmentation
Word segmentation is performed using LTP.

[LTP - Language Technology Platform](https://github.com/HIT-SCIR/ltp)

### Tone Annotation
Tone annotation is conducted using g2pM.

[g2pM - Grapheme to Phoneme for Mandarin](https://github.com/kakaobrain/g2pM)

## Features
We generated the following features for each character in the utterances across all three datasets:

## References
If you want to use the data, please cite the following papers:

For Tone Sandhi Data:
```
@inproceedings{Tian2022MandarinTS,
  title={Mandarin Tone Sandhi Realization: Evidence from Large Speech Corpora},
  author={Zuoyu Tian and Xiao Dong and Feier Gao and Haining Wang and Charles Steven Lin},
  booktitle={Interspeech},
  year={2022},
  url={https://www.isca-speech.org/archive/pdfs/interspeech_2022/tian22e_interspeech.pdf}
}
```

For Forced Alignment Files:
```
@article{zhu2022charsiu,
  title={Phone-to-audio alignment without text: A Semi-supervised Approach},
  author={Zhu, Jian and Zhang, Cong and Jurgens, David},
  journal={IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP)},
  year={2022}
}
```

---
