# Mandarin Tone Sandhi Realization: Evidence from Large Speech Corpora


## Dataset


### Free ST Chinese Mandarin Corpus (Speaker Info) 
This corpus were recorded in silence in-door environment using cellphone. It has 855 speakers. Each speaker has 120 utterances. All utterances were carefully transcribed and checked by human. Transcription accuracy is guaranteed.
http://www.openslr.org/38/

20170001P00189I0036	女	31	四川	我有两张君悦皇家浴场

P00189I: speaker number
0036: speech number

### MAGICDATA Mandarin Chinese Read Speech Corpus (Read Speech)(Speaker Info)
The corpus by Magic Data Technology Co., Ltd. , containing 755 hours of scripted read speech data from 1080 native speakers of the Mandarin Chinese spoken in mainland China. The sentence transcription accuracy is higher than 98%.
http://www.openslr.org/68/




### aidatatang_200zh 

The contents and the corresponding descriptions of the corpus include:

The corpus contains 200 hours of acoustic data, which is mostly mobile recorded data.
600 speakers from different accent areas in China are invited to participate in the recording.
The transcription accuracy for each sentence is larger than 98%.
Recordings are conducted in a quiet indoor environment.
The database is divided into training set, validation set, and testing set in a ratio of 7: 1: 2.
Detail information such as speech data coding and speaker information is preserved in the metadata file.
Segmented transcripts are also provided.


http://www.openslr.org/62/


## Process pipelines

### Metadata Stat

### Forced Alignment
We use Charsiu to do the vowel level forced alignment.

https://github.com/lingjzhu/charsiu/

Because the authors of Charsiu released the textgrid files we want, here we directly used their alignments files:

https://github.com/lingjzhu/charsiu/blob/main/misc/data.md#alignments-for-mandarin-speech-datasets

### Segmentation

We use LTP to do the word segmentation

https://github.com/HIT-SCIR/ltp

### Tone Annotation

We use g2pM to do the tone annotation

https://github.com/kakaobrain/g2pM

## Features

We generated the following features for each character of the utterances in all three datasets:

character;tone; position_type:start_word,end_word,middle; word; word_len; syllable; previous_tone;
following_tone; previous_syllable; following_syllable; speaker_id; gender; 
age; province; vowel_dur; char_dur.



