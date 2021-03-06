1
00:00:06,539 --> 00:00:07,809
Hello again.

2
00:00:07,809 --> 00:00:10,499
In this video, we'll talk about character strings.

3
00:00:11,149 --> 00:00:14,049
We've see what a character was.

4
00:00:14,049 --> 00:00:18,049
so here's a example of main with a character "c".

5
00:00:18,849 --> 00:00:22,849
I gave "char c" the ASCII value for " * ".

6
00:00:22,849 --> 00:00:26,079
So if I do a putchar of "char c",

7
00:00:26,079 --> 00:00:28,809
it should display an asterisk onscreen

8
00:00:28,809 --> 00:00:32,049
compiling... launching. All good!

9
00:00:32,463 --> 00:00:37,103
In a previous video, I made a mistake... remember? I used quotation marks...

10
00:00:37,103 --> 00:00:40,163
instead of inverted comas.

11
00:00:40,163 --> 00:00:42,913
quotation marks are for character strings.

12
00:00:43,000 --> 00:00:44,880
So, what's a character string?

13
00:00:44,952 --> 00:00:48,952
It's an ensemble of bytes, one byte next to the other.

14
00:00:48,952 --> 00:00:51,662
So a series of bytes each containing one character.

15
00:00:51,662 --> 00:00:52,762
And normally,

16
00:00:52,762 --> 00:00:56,762
this string's last element should be "\0" or the value "0",

17
00:00:56,762 --> 00:01:00,762
the ASCII character for "\0" or "0", they're all the same thing.

18
00:01:01,019 --> 00:01:03,569
Actually, for each ASCII character,

19
00:01:03,569 --> 00:01:07,569
there's a "numerical value" that defines the end of the string.

20
00:01:08,666 --> 00:01:10,806
How could we use this?

21
00:01:11,269 --> 00:01:12,109
It's simple.

22
00:01:13,088 --> 00:01:19,808
When you type "Toto", it'll be replaced by the address

23
00:01:19,808 --> 00:01:23,808
of 1st element of the character string "toto".

24
00:01:25,032 --> 00:01:27,042
Which is the address of "t".

25
00:01:28,634 --> 00:01:29,594
Be careful...

26
00:01:30,078 --> 00:01:32,618
I just spoke about addresses...

27
00:01:32,632 --> 00:01:34,492
We're talking about pointers.

28
00:01:34,492 --> 00:01:38,492
You're probably telling yourself "Okay, we're going to need a pointer"

29
00:01:38,764 --> 00:01:40,834
This time I'm going to call it "*str".

30
00:01:40,834 --> 00:01:43,654
Nah, actually I'm going to call it "*ptr", it'll be better.

31
00:01:43,654 --> 00:01:46,273
It's the same thing, we're still talking about pointers.

32
00:01:46,273 --> 00:01:50,273
I'm going to write something that the Norm forbids...

33
00:01:50,273 --> 00:01:53,153
Actually, no, that'll just be confusing.

34
00:01:53,497 --> 00:01:59,287
So "ptr" equals to the address of the "toto" character string.

35
00:01:59,553 --> 00:02:02,393
I told you a few seconds ago

36
00:02:02,414 --> 00:02:07,134
that "Toto" is a series of bytes, one after the other, that ends with a "\0"

37
00:02:07,134 --> 00:02:09,164
and so when we write "Toto",

38
00:02:09,164 --> 00:02:13,164
the character string "Toto", we simply return the address of the 1st character

39
00:02:13,405 --> 00:02:15,795
"ptr" can only contain an address.

40
00:02:15,872 --> 00:02:17,522
That's an important fact.

41
00:02:17,534 --> 00:02:19,924
From now on, and for the rest of the video,

42
00:02:19,964 --> 00:02:22,424
we will talk about character strings.

43
00:02:22,424 --> 00:02:23,224
But remember,

44
00:02:23,224 --> 00:02:26,404
when we talk about a pointer to string (character string of course)

45
00:02:26,404 --> 00:02:28,424
In a way, it's still a pointer to char.

46
00:02:28,424 --> 00:02:31,264
It's a pointer to the first element of the character string.

47
00:02:31,264 --> 00:02:33,264
Let's just hope that in the end,

48
00:02:33,264 --> 00:02:36,254
when you go through your bytes, thanks to pointers arithmetics,

49
00:02:36,254 --> 00:02:38,224
all the way at the end, you'll have a "\0"

50
00:02:38,224 --> 00:02:39,594
that'll tell you to stop.

51
00:02:39,594 --> 00:02:41,114
But when you write this,

52
00:02:41,114 --> 00:02:43,754
the compiler will automatically set "toto" in its memory

53
00:02:43,754 --> 00:02:46,484
So char "t", char "o", char "t", char "o" AND char "\0"

54
00:02:46,965 --> 00:02:50,965
and will return the address of the first character, so "t".

55
00:02:53,539 --> 00:02:54,779
Here's the proof.

56
00:02:55,115 --> 00:03:03,965
If I display "*ptr" - the element pointed by "ptr"

57
00:03:07,910 --> 00:03:09,900
See, here's my "t".

58
00:03:13,205 --> 00:03:17,205
Remember, I told you about another way to write this,

59
00:03:17,211 --> 00:03:18,761
which is easier...

60
00:03:18,937 --> 00:03:20,827
Using square brackets.

61
00:03:20,959 --> 00:03:23,609
This should give me the exact same result.

62
00:03:25,325 --> 00:03:26,335
See, still "t".

63
00:03:26,790 --> 00:03:30,790
So if I wanted to move around my string "toto",

64
00:03:30,790 --> 00:03:34,130
The last element of the string, as we said earlier,

65
00:03:34,130 --> 00:03:38,130
when I told you to allocate 10 elements on the stack, with an array,

66
00:03:38,130 --> 00:03:43,610
so the last element is the 9th element. Exactly.

67
00:03:44,247 --> 00:03:48,247
So how many elements have I allocated for tToto"? Truely?

68
00:03:49,154 --> 00:03:51,694
Nope, not 4! I'm sure everybody thought 4...

69
00:03:52,002 --> 00:03:52,752
It's 5!

70
00:03:52,804 --> 00:03:55,474
I told you earlier there was an extra "\0" at the end...

71
00:03:55,558 --> 00:03:58,028
So in reality, I have 5 on the stack.

72
00:03:58,028 --> 00:04:00,348
But the "\0" is something special...

73
00:04:00,348 --> 00:04:03,728
Because it'll allow us to know when we're done browsing through memory,

74
00:04:03,728 --> 00:04:06,038
and that we're done reading the character string.

75
00:04:06,075 --> 00:04:09,275
So when you'll create character strings, manually, you must remember

76
00:04:09,275 --> 00:04:11,155
to always end your string with a "\0".

77
00:04:11,207 --> 00:04:14,767
Otherwise, all programs that can read character strings, will keep reading,

78
00:04:14,767 --> 00:04:16,827
until they find a "\0". And it could crash.

79
00:04:16,827 --> 00:04:17,947
"crashing" = bad!

80
00:04:18,584 --> 00:04:22,294
So. "ptr[0]". If I wanted to access the last "o",

81
00:04:23,120 --> 00:04:27,120
"ptr[1]" is the first "o", "ptr[2]" is the second "t",

82
00:04:27,654 --> 00:04:29,614
"ptr[3]" that's the last "o".

83
00:04:30,058 --> 00:04:34,058
Let's display it.

84
00:04:35,121 --> 00:04:35,821
See!

85
00:04:36,553 --> 00:04:38,553
Cool! I've displayed the last "o".

86
00:04:38,572 --> 00:04:40,892
If I try to display "ptr[4]"...

87
00:04:40,892 --> 00:04:43,712
(as I've said, we have 5 elements on the stack)

88
00:04:43,895 --> 00:04:46,585
This is what happens.

89
00:04:47,360 --> 00:04:49,830
It doesn't display anything, sort of.

90
00:04:49,879 --> 00:04:53,879
Let's use the "cat" command on it.

91
00:04:53,879 --> 00:04:57,879
With the "-e" option, which displays non-printable characters.

92
00:04:58,194 --> 00:05:02,194
See those characters on screen? They represent "\0".

93
00:05:02,885 --> 00:05:04,485
A simple character string.

94
00:05:05,100 --> 00:05:08,550
So I've successfully displayed the end of the "toto" character string.

95
00:05:08,764 --> 00:05:10,924
Something very important you should know,

96
00:05:10,924 --> 00:05:12,904
When you write this...

97
00:05:12,904 --> 00:05:14,744
you've been given an address.

98
00:05:14,744 --> 00:05:18,004
But "toto" is somewhere in memory, where you're not allowed to write.

99
00:05:18,004 --> 00:05:21,894
Meaning that if I wanted to transform "toto" into "poto"...

100
00:05:22,268 --> 00:05:29,498
If I write this ... (types)

101
00:05:30,249 --> 00:05:35,329
Normally, it should either not compile at all,

102
00:05:35,329 --> 00:05:39,329
or compile, but crash...

103
00:05:41,765 --> 00:05:45,765
"Bus error". I've crashed.

104
00:05:45,765 --> 00:05:48,325
Yay! That's exactly what I wanted to show you.

105
00:05:48,325 --> 00:05:51,535
"toto" here, is in an area where we're not allowed to write.

106
00:05:51,535 --> 00:05:57,135
The only way for me to write over "toto", would be to declare an array,

107
00:05:57,135 --> 00:06:02,385
but without setting its size. Look at what I'm typing.

108
00:06:03,216 --> 00:06:06,316
Once you've done this, the compiler knows you're trying

109
00:06:06,316 --> 00:06:09,226
to allocate an array, and that you want to write "toto" in it,

110
00:06:09,244 --> 00:06:13,244
so it'll allocate 5 elements, (t, o, t, o, \0)

111
00:06:13,244 --> 00:06:18,384
and it'll put those 5 elements' address on the stack,

112
00:06:18,384 --> 00:06:21,514
and "ptr" will be a pointer on that.

113
00:06:22,281 --> 00:06:24,891
So if I do the same thing, see?

114
00:06:25,578 --> 00:06:28,138
let's compile & execute.

115
00:06:28,560 --> 00:06:32,560
This time it worked, I have "p" as my string's 1st element.

116
00:06:36,086 --> 00:06:38,176
All of this seems fun for now...

117
00:06:38,340 --> 00:06:42,340
But I wanted to show you something to make things clearer.

118
00:06:42,482 --> 00:06:46,482
30 seconds ago, we had "char *ptr"

119
00:06:48,538 --> 00:06:52,538
and underneath "ptr = "toto;"

120
00:06:53,763 --> 00:06:57,763
What happens if I add another "char *",

121
00:06:58,083 --> 00:06:59,623
let's call it "ptr2".

122
00:07:00,480 --> 00:07:07,520
and then write " ptr2 = "lol"; "

123
00:07:08,530 --> 00:07:13,730
and then write "ptr = ptr2;"

124
00:07:15,785 --> 00:07:19,785
What happens when I check "ptr[0]"?

125
00:07:22,955 --> 00:07:24,185
Well it's simple...

126
00:07:24,865 --> 00:07:26,995
If we follow the logic,

127
00:07:26,995 --> 00:07:33,585
"ptr2" takes the address of "l" from "lol" & "ptr" takes the address of "toto"'s "t"

128
00:07:34,336 --> 00:07:36,556
Now. When I write "ptr = ptr2",

129
00:07:36,556 --> 00:07:40,266
on the right I have a pointer to char, on the left, I have a pointer to char...

130
00:07:40,272 --> 00:07:41,772
I'm allowed to write this.

131
00:07:41,772 --> 00:07:43,612
So what's "ptr2"? It's just an address.

132
00:07:43,612 --> 00:07:45,112
"ptr" also is an address.

133
00:07:45,180 --> 00:07:47,610
So I've overwritten the address contained in "ptr",

134
00:07:47,610 --> 00:07:49,850
by the address contained in "ptr2".

135
00:07:49,850 --> 00:07:53,160
So the result is that "ptr" now points to the "l" (from "lol").

136
00:07:53,177 --> 00:07:55,567
So normally, if I execute this...

137
00:07:56,849 --> 00:07:59,639
I've displayed an "l".

138
00:07:59,639 --> 00:08:02,909
So that's about everything you need to know about character strings.

139
00:08:02,909 --> 00:08:06,289
Just remember. A character string is a series of bytes (or characters),

140
00:08:06,289 --> 00:08:08,779
one after another, and that ends with a "\0".

> Buna ziua. In acest video vom vorbi despre sirurile de caractere. 

> Inca de la inceput, am putut vedea ce este un caracter. 

> Reluam un exemplu simplu de functie "main". 

> Declaram o variabila "c" de tip "char" care ia valoarea caracterului ASCII 

> Daca fac "putchar(c)" ar trebui sa afis '*' pe ecran. 

> Compilam, executam... 

> Intr-unul dintre videourile precedente m-am incurcat si am folosit ghilimele. 

> Si ghilimelele sunt folosite pentru definirea sirurilor de caractere. 

> e sunt sirurile de caractere? 

> Sirurile de caractere sunt o multime de bytes situati unul langa altul, care fiecare contin cate un caracter. 

> Ultima valoare dintr-un sir ar trebui sa fîe caracterul ASCII *\0' sau valoarea numerica 0 (sunt echivalente). 

> Pentru ca fiecare caracter ASCII are un cod numeric unic asociat. 

> Acest caracter defineste deci sfarsitul sirului. 

> Cum putem folosi asta? 

> E simplu. Cand scrieti, de exemplu, "toto", va fi inlocuit cu adresa primului element al sirului "toto". 

> Deci adresa lui "t". 

> Atentie... Vorbim despre adrese, deci despre pointeri, deci probabil va spuneti ca vom avea cu siguranta nevoie de un pointer. 

> O sa-l numim "str" de data asta... De fapt nu, il voi numi tot "ptr", ca sa vedeti ca e acelasi lucru, folosim tot pointeri. 

> Si aici voi scrie intr-un mod diferit de cum am scris inainte... 

> Desi... pana la urma il scriu totusi mai jos, in modul standard. 

> ptr = "toto"; 

> Am facut un abuz de limbaj, pentru ca abia v-am spus ca "toto" e un sir de bytes care se termina prin '\0', si ca modul de scriere "toto" va returna adresa primului caracter. 

> "ptr" nu poate contine altceva decat o adresa. 

> Asta e un punct foarte important. 

> Pentru restul videoului, de acum incolo, vom vorbi despre siruri de caractere, dar amintrti-va ca atunci cand spunem pointer catre un sir de caractere, de fapt vorbim de un pointer catre un "char",  pointer catre primul element din sir, si speram ca atunci cand parcurgem sirul prin aritmetica de pointeri la sfarsit vom gasi un ’\0' care ne va spune sa ne oprim. 

> Cand scriem asta compilatorul pune in memorie "toto", deci caracterele 't', 'o', deci le va pune in memorie si va va returna adresa primului 't' din "toto". 

> Ca demonstratie, daca aici afisez "*ptr", deci elementul pointat de catre "ptr", in mod normal ar trebui sa afisez un ’t'. Si chiar l-am afisat. 

> Dupa cum va amintiti v-am spus ca putem scrie si altfel, vom utiliza in continuare apelul folosind paranteze patrate. 

> Si ar trebui sa faca acelasi lucru, fac asta doar ca sa va reimprospatez memoria. Deci afisez tot 't'. 

> Daca vreau sa ma deplasez in sirul de caractere "toto"... 

> Mai tineti minte ce v-am spus mai devreme? V-am spus ca alocati 10 elemente pe stiva cu acel tablou, deci pentru a accesa ultimul element folositi indexul 9. 

> Deci cate elemente am alocat pentru "toto"? Am alocat... nu 4 cum va spuneti toti, ci 5, pentru ca dupa cum v-am spus la sfarsit e un 'XO’. 

> Deci am 5 elemente pe stiva, dar ’\0* e un caracter special care ne permite sa stim cand sa nu mai avansam in memorie pentru ca am terminat de citit sirul. 

> Deci cand creati manual siruri de caractere trebuie sa le terminati pintr-un '\0', daca nu, toate programele care vor citi siruri de caractere vor continua sa citeasca pana la primul '\0’, si riscati sa crape. 

> Si nu e bine sa crape programele... 

> "ptr[1]" e primul 'o’, "ptr[2]" al doilea 't', si "ptr[3]" e ultimul 'o'. 

> Deci il vom afisa. 

> Cool. Am afisat ultimul ’o'. 

> Daca acum caut "ptr[4]" (pentru ca avem 5 elemente in stiva), veti vedea ca nu afiseaza nimic. 

> Voi folosi acum "cat -e". 

> Si "cat -e" imi va face sa apara caracterele "non-afisabile", si ceea ce vedeti aici e un '\0'. 

> Deci e un sfarsit de sir de caractere. 

> Deci acum am afisat sfarsitul sirului de caractere "toto". 

> Ceva foarte important de stiut: cand scrieti asta, "toto" v-a dat o adresa. 

> Dar "toto" e intr-o parte a memoriei unde nu aveti voie sa scrieti. 

> Daca acum vreau sa transform "toto" in "poto", deci: ptr[O] = 'p'; (si nu sirul de caractere "p", nu e acelasi lucru) veti vedea ca in mod normal (si pentru asta reafisez "ptr[O]"), sau nici macar nu va compila,  sau programul va crapa. 

> Si in cazul de fata a crapat cu eroarea "bus error". 

> E exact ce voiam sa va arat. "toto" e intr-o zona in care nu avem dreptul sa scriem. 

> Singura modalitate prin care as putea scrie in "toto", e daca as fi declarat un tablou, fara marime, si as fi pus sirul de caractere in el. 

> O data ce ati scris asta, compilatorul stie ca ati vrut sa alocati un tablou, si sa puneti "toto" in el. 

> Va va aloca 5 elemente, 't', 'o', 't', 'o', '\0', dupa cum va amintiti. 

> deci 5 elemente, si va pune adresa lor pe stiva, in "ptr", si "ptr" va fi un pointer catre acest lucru. 

> Daca acum fac acelasi lucru... sa incercam... fac acelasi lucru si de data asta a mers, si am 'p' ca prim caracter al sirului. 

> Asta pare amuzant deocamdata, dar mai e ceva ce vreau sa va arat, ca sa fie totul clar. 

> Acum 30 de secunde eram pe "char *ptr", si: ptr = "toto"; 

> Aici eram. Ce se intampla daca iau un al doilea "char "ptr2", si voi scrie: ptr2 = "lol"; 

> Si acum scriu "ptr = ptr2 

> Ce se intampla cand caut "ptr[O]"? 

> Pai, daca urmarim logica, "ptr2" ia adresa primului T din "lol". 

> "ptr" ia adresa primului ’t’ din "toto". 

> Acum cand scriu "ptr = ptr2;", in dreapta am un pointer catre "char", in stanga am un pointer catre "char", am

> dreptul sa scriu asta. 

> Deci ce e "ptr2"? E doar o adresa. "ptr" e si el o adresa. 

> Deci acum am suprascris adresa din "ptr" cu adresa din "ptr2". 

> Si acum "ptr" pointeaza catre 'l'-ul din "lol". 

> Deci daca execut asta (si daca nu am gresit nimic), voi afisa un T. 

> Am facut turul sirurilor de caractere; amintiti-va deci ca sirurile sunt caractere (bytes) unele dupa altele, care se termina printr-un ’\0*. 