# 🗣️ FunASR Speech-to-Text with Timestamps

This project demonstrates the use of Alibaba's FunASR to transcribe multilingual speech (Chinese and English) into text with accurate timestamps.

---

## 🔧 Technologies Used
- Python
- FunASR Toolkit
- PyTorch
- Pretrained ASR Models

---

## 🎯 Goals
- Transcribe English and Chinese speech
- Generate timestamped output (word-level or sentence-level)
- Use pretrained ASR models from FunASR

---

## 📁 Features
✅ Multilingual support (Chinese & English)  
✅ Timestamps for each sentence  
✅ CLI and Python usage examples  
✅ High-accuracy transcription

---

## ▶️ How to Use

### 1. Clone the Repository
```bash
git clone https://github.com/deepakpalve8205/FunASR_Speech_to_text_with_timestamp.git
cd FunASR_Speech_to_text_with_timestamp

### 2. Install Dependencies
pip install funasr

### 3. Run Inference
funasr-cli --model paraformer-zh --input ./your_audio_file.wav


###For English:

funasr-cli --model paraformer-en --input ./your_english_audio.wav
### Outputs
### for chinese
rtf_avg: 0.069, time_speech:  70.471, time_escape: 4.877: 100%|████████████████████████████████████████████████████████| 1/1 [00:04<00:00,  4.88s/it]
[{'key': 'chinese_lang', 'text': '试错的过程很简单啊，今特别是今天冒名插血卡的同学，你们可以听到后面的有专门的活动课，它会大大降低你的思错成本。其实你也可以不要来听课，为什么你自己写嘛？我先今天写五个点，我就实试实验一下。反正这五个点不行，我再写五个点，再是再不行，那再写五个点嘛。你总会所谓的活动大神和所谓的高手都是只有一个，把所有的错所有的坑全部趟一遍，留下正确的。你就是所谓的大神，明白吗？所以说关于活动通过这一块，我只送给你们四个字啊，换位思考。如果说你要想降低你的试错成本，今天来这里你们就是对的。因为有创企创需要搞这个机会。所以说关于活动过于不过这个问题，或者活动很难通过这个话题。呃，如果真的要坐下来聊的话，要聊一天，但是我觉得我刚才说的四个字足够。好，谢谢。好，非常感谢那个三毛老师的回答啊。三毛老师说我们在整个店铺的这个活动当中，我们要学会换位思考。其实。', 'timestamp': [[380, 620], [640, 740], [740, 940], [940, 1020], [1020, 1260], [1500, 1740], [1740, 1840], [1840, 2135], [2830, 3010], [3010, 3210], [3210, 3290], [3290, 3370], [3370, 3470], [3470, 3590], [3590, 3830], [3950, 4130], [4130, 4270], [4270, 4350], [4350, 4470], [4470, 4590], [4590, 4690], [4690, 4770], [4770, 5010], [5250, 5410], [5410, 5530], [5530, 5650], [5650, 5975], [6670, 6830], [6830, 6970], [6970, 7110], [7110, 7230], [7230, 7470], [7490, 7730], [8070, 8310], [8310, 8430], [8430, 8670], [8690, 8910], [8910, 9030], [9030, 9270], [9550, 9750], [9750, 9910], [9910, 10110], [10110, 10350], [10670, 10910], [10950, 11130], [11130, 11250], [11250, 11370], [11370, 11490], [11490, 11630], [11630, 11730], [11730, 11970], [12310, 12490], [12490, 12610], [12610, 12710], [12710, 12790], [12790, 12910], [12910, 13110], [13110, 13270], [13270, 13350], [13350, 13490], [13490, 13630], [13630, 13870], [14030, 14250], [14250, 14350], [14350, 14589], [14630, 14850], [14850, 14950], [14950, 15070], [15070, 15250], [15250, 15490], [15950, 16150], [16150, 16390], [16390, 16470], [16470, 16610], [16610, 16750], [16750, 16850], [16850, 16970], [16970, 17210], [17270, 17390], [17390, 17570], [17570, 17810], [17990, 18230], [18310, 18410], [18410, 18550], [18550, 18650], [18650, 18870], [18870, 19010], [19010, 19090], [19090, 19190], [19190, 19310], [19310, 19390], [19390, 19490], [19490, 19590], [19590, 19830], [19970, 20130], [20130, 20250], [20250, 20430], [20430, 20550], [20550, 20670], [20670, 20910], [21090, 21270], [21270, 21510], [21510, 21650], [21650, 21750], [21750, 21990], [22470, 22609], [22609, 22710], [22710, 22890], [22890, 22970], [22970, 23070], [23070, 23190], [23190, 23485], [24060, 24280], [24280, 24380], [24380, 24620], [25120, 25360], [25500, 25660], [25660, 25985], [27030, 27230], [27230, 27410], [27410, 27510], [27510, 27750], [27810, 27990], [27990, 28150], [28150, 28270], [28270, 28350], [28350, 28430], [28430, 28755], [30180, 30320], [30320, 30560], [30600, 30720], [30720, 30840], [30840, 30940], [30940, 31235], [32020, 32260], [32280, 32440], [32440, 32620], [32620, 32700], [32700, 32940], [33200, 33340], [33340, 33440], [33440, 33560], [33560, 33800], [33960, 34160], [34160, 34360]



### for english
import datetime

# Your ASR result (copy it here)
result = [{
    'key': 'deepak_english_audio',
    'text': ' Hi, my name is the bug pile where i had completed my graduation, invest say, computer science.',
    'timestamp': [[110, 350], [390, 590], [590, 850], [850, 1050], [1050, 1250], [1250, 1490], [1490, 1830],
                  [1830, 2010], [2010, 2170], [2170, 2410], [2510, 3110], [3110, 3310], [3310, 4030], [4150, 4690],
                  [4690, 4930], [4930, 5450], [5450, 6085]]
}]

# Extract text and timestamps
words = result[0]['text'].strip().split()
timestamps = result[0]['timestamp']

def ms_to_timestamp(ms):
    seconds = ms / 1000
    return str(datetime.timedelta(seconds=seconds))[:-3]

# Combine each word with its readable timestamp
for word, (start, end) in zip(words, timestamps):
    readable_start = ms_to_timestamp(start)
    readable_end = ms_to_timestamp(end)
    print(f"[{readable_start} - {readable_end}] {word}")
    above in scrpit and below one in terminal



tejgyan@Tejgyans-MacBook-Pro new % python readable_output.py  
[0:00:00.110 - 0:00:00.350] Hi,
[0:00:00.390 - 0:00:00.590] my
[0:00:00.590 - 0:00:00.850] name
[0:00:00.850 - 0:00:01.050] is
[0:00:01.050 - 0:00:01.250] the
[0:00:01.250 - 0:00:01.490] bug
[0:00:01.490 - 0:00:01.830] pile
[0:00:01.830 - 0:00:02.010] where
[0:00:02.010 - 0:00:02.170] i
[0:00:02.170 - 0:00:02.410] had
[0:00:02.510 - 0:00:03.110] completed
[0:00:03.110 - 0:00:03.310] my
[0:00:03.310 - 0:00:04.030] graduation,
[0:00:04.150 - 0:00:04.690] invest
[0:00:04.690 - 0:00:04.930] say,
[0:00:04.930 - 0:00:05.450] computer
[0:00:05.450 - 0:00:06.085] science.
tejgyan@Tejgyans-MacBook-Pro new % 
