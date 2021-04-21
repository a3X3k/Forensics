# Special

![bi0s](https://github.com/a3X3k/Forensics/blob/main/Special/Assets/1.png?raw=true)

- There is a `PDF` given in this challenge.
- After analysing I [carved](https://www.extractpdf.com/) out the `JPEG` Image.
- After spending lot of time in analysing the image I was not able to trace anything.
- So I started to analyse the `HexDump` of the `PDF` file.

![bi0s](https://github.com/a3X3k/Forensics/blob/main/Special/Assets/5.png?raw=true)

- After seeing multiple `EOF`'s in the file I [googled](https://www.garykessler.net/library/file_sigs.html) to learn something about them.
- Then started to remove some bytes after the `EOF`.
- Intially started with the last `EOF`. 
- But it showed error.
- So started to remove from the first `EOF`.

![bi0s](https://github.com/a3X3k/Forensics/blob/main/Special/Assets/6.png?raw=true)

- Then there were some changes in the `PDF`.
- So I started to remove the chunks further.
- After deleting few chunks I was able to see the `Special Word`.

![bi0s](https://github.com/a3X3k/Forensics/blob/main/Special/Assets/2.png?raw=true)
![bi0s](https://github.com/a3X3k/Forensics/blob/main/Special/Assets/3.png?raw=true)
![bi0s](https://github.com/a3X3k/Forensics/blob/main/Special/Assets/4.png?raw=true)

```
Flag --> flag{BROFIST}
```
