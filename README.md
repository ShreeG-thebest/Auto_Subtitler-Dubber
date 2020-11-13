# Auto_Subtitler-Dubbers
This project aims to translate, dub and overlay video and audio files in other languages using modulated voices as well as subtitles for video files. This program accomplishes all this in real time, through using many different machine learning algorithms to detect when people are speaking, when mouths are moving and when mouths aren't moving (which is arguably more important). 

# How I made this project
I started this project using the IDE Visual Studio Code, but ended up switching over to PyCharm for the accessiblity features for the free version. For the datasets, I tried to using Friends episodes, but the laugh track made it hard to isolate the voices for the dubbing, so I ended up using a select few Office episodes. The datasets can be viewed in the DataSet folder. 

# What did I test for?
To maximize accuracy of dubbing voices while acters are moving their mouths, I used two different variables (the actual audio of the voices + when mouths were moving). For the first variable, I simple had to test for human voice using a human voice modulater open source software, that I pinged to my program with Docker. With a bit of specialized testing, I could accurately pinpoint when humans were talking in the show. For the second part, I used open source facial recognition software and combined it with my own specialized code to detect when there was a space between the the top and bottom lip of any given actor. 

# How did I integrate the variables into my final code?
Once I had isolated these two variables, and could accurately test when someone was talking and then when someone was moving their lips, all I had to do was add pre-written subtitles for the shows to my datasets, and fed them through a translation software to convert them to my desired language. I then used an google's open source audio overlay to generate computer generated voices to overlay on top of the episode. 

# Machine learning component:
I used unsupervised learning because I did not have a correct end result to show the computer. Within unspervised learning, I used association rule learning and FP Growth. Within a few thousand iterations, the program could accurately predict and pinpoint when characters were talking and overlay the translated rules. 

# Results
The first several thousand iterations were extremely choppy, as the computer could not predict when to overlay the voices even with accurate facial recognition software enabled. Instead of using dimensionality reduction through unsupervised learning, I switched to association rule learning, associating when the original voices were being broadcast to when the new dub should be voiced. This ended up working a lot better, effectively reducing my margin of error to minimal amounts. 
