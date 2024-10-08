# `ai speech intent`

The `ai speech intent` command recognizes streaming audio captured from a device microphone or stored in local or remote audio files and returns intent information from that recognition using PATTERNS.

### Usage

``` bash
ai speech intent [...]
```

### Options

| Option             | Description                                                                 |
|--------------------|-----------------------------------------------------------------------------|
| `--key KEY`          | Subscription key for the Azure Speech Service.                              |
| `--region REGION`    | Region for the Azure Speech Service.                                        |
| `--pattern PATTERN`  | Simple pattern to use for recognizing intents.                              |
| `--pattern INTENTID=PATTERN` | Associate a pattern with a specific intent ID.                      |
| `--patterns PATTERN1;PATTERN2` | Use multiple patterns for recognizing intents.                    |
| `--patterns @PATTERNS.txt` | Use patterns listed in a text file.                                   |
| `--microphone`       | Use the device microphone as the input source.                              |
| `--file FILE`        | Use a local audio file as the input source.                                 |
| `--files PATTERN`    | Use multiple local audio files as input sources.                            |
| `--files @FILELIST.txt` | Use audio files listed in a text file as input sources.                  |
| `--format FORMAT`    | Specify the audio format (e.g., wav, mp3).                                  |
| `--once[+]`          | Perform a single recognition for the input source (with optional repetition).|
| `--continuous`       | Perform continuous recognition for the input source.                        |
| `--keyword FILENAME` | Perform recognition based on a keyword detected in the audio.               |
| `--language LANGUAGE` | Specify the language of the input audio (e.g., en-US).                     |
| `--log FILENAME`     | Save the recognition log to a file.                                         |
| `--proxy HOSTNAME`   | Use a proxy server for the recognition.                                     |
| `--foreach in @ITEMS.txt` | Iterate the recognition over multiple items listed in a text file.     |
| `--threads NUMBER`   | Specify the number of threads to use for parallel processing.               |

### Examples

``` bash title="Recognize intent from a local audio file using a simple pattern"
ai speech intent --file audio.wav --pattern "What's the weather like?"
```

``` bash title="Recognize intents from multiple audio files using patterns"
ai speech intent --files *.wav --patterns "turn on the light";"turn off the light"
```

``` bash title="Recognize intents from audio files listed in a file using patterns from another file"
ai speech intent --files @audiofiles.txt --patterns @patterns.txt
```

``` bash title="Perform continuous intent recognition from the microphone input"
ai speech intent --microphone --continuous
```
