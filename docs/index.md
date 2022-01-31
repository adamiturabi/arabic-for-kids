---
title: "An Arabic course for non-native children"
author: "A brother"
documentclass: book
geometry:
# A4 2 pages per sheet draft
- paper=a5paper               # a5: 148.5 by 210mm
# final
#- paperwidth=156mm  #170mm
#- paperheight=234mm #244mm
- bindingoffset=4mm
- textwidth=114.8mm           # = (170 - 6)*0.7
- textheight=170.8mm          # = 244 * 0.7
- twoside
mainfont: Junicode
mainfontoptions: Numbers=OldStyle
fontsize: 10pt
polyglossia-lang:
  name: en
polyglossia-otherlangs:
  - name: arabic
fontfamilies:
  - name: \arabicfont
    font: Scheherazade New
    options: Script=Arabic,Scale=1.0
csquotes: true
output:
  bookdown::gitbook:
    #split_by: "section"
    pandoc_args: ["--lua-filter=trn.lua"]
    keep_md: yes
    css: mystyle.css
    config:
      toc:
        collapse: section
        scroll_highlight: yes
        before: null
        after: null
      toolbar:
        position: fixed
      edit : null
      download: null
      search: yes
      fontsettings:
        theme: white
        family: serif
        size: 2
      sharing:
        facebook: yes
        github: no
        twitter: yes
        linkedin: yes
        weibo: no
        instapaper: no
        vk: no
        all: ['facebook', 'twitter', 'linkedin', 'weibo', 'instapaper']
      info: yes
  bookdown::pdf_book:
    number_sections: true
    pandoc_args: ["--lua-filter=trn.lua", "--columns=65"] # for forcing word wrap in pipe tables
    latex_engine: xelatex
    #template: default_latex_template.tex # with Brill font the PDF font is too large and this needs to be uncommented. includes and in_header should then be commented
    includes:
      in_header: "preamble.tex"
    keep_tex: true

---



# Introduction {-}

:::{lang=ar dir=rtl}
بسم الله الرحمن الرحيم  
الحمد لله والصلاة والسلام على نبينا محمد  
أشهد أن لا إله إلا الله وأشهد أن محمدا عبده ورسوله  
أما بعد:
:::

This course aims to teach Arabic to non-native speaking school children.

This is a work in progress and is currently incomplete. The development page is at: https://github.com/adamiturabi/arabic-for-kids

## Approach {-}

We will focus on basic grammar, vocabulary and comprehension. So for example, we will accept as correct:

[فَتَحَ الوَلَد بَاب وَذَهَبَ إِلَىٰ الحَديقَة]{.ar}  
[fataHa Eal-walad bAb wapahaba EilA Eal-HadIqah]{.trn}

rather than

[فَتَحَ الوَلَدُ بَابًا وَذَهَبَ إِلَى الحَديقَة]{.ar}  
[fataHa l-waladu bAban wapahaba Eila l-HadIqah]{.trn}

The reason for this is that our goal is for children to be able to parse sentences and read and write at a basic proficiency. Although case endings are essential for an in-depth understanding, and indeed for disambiguation from flexible word order ([ضَرَبَ عمرًا زيدٌ]{.ar}), we feel they are not imperative to understand sentences that follow normal word order. At this basic level, we fear that case endings will introduce additional complexity to a non-native speaking student.

Once the student is at a high-school or college level, they may take an [الآجرومية]{.ar} or similar course for a more complete study of the grammar.

We will however try to introduce the concept of inflection to the student. Perhaps the sound masculine plural inflection in the [marfooe]{.trn} vs other cases will be suitable for this since it is one of the more visible inflections in unvowelized text and the student will get accustomed to seeing it in his supplemental reading.

## Starting age {-}

Lesson 1 of this course should be suitable for a child of around 8 years of age.

## Pre-requisites {-}

The student should already know how to read fully vowelized Arabic at a beginner level, i.e., basic [fathah]{.trn}, [kasrah]{.trn}, [Dammah]{.trn}, [caddah]{.trn}, and long vowels. More complicated orthography, like [hamzat al-wasl]{.trn}, is not expected to be known. But it is assumed that the student is getting Quranic [tajwId]{.trn} instruction at the same time elsewhere.

## Instruction and drills {-}

Each lesson is to be instructed to the student with new vocabulary introduced.

This lesson is then reinforced by regular drills. The drills usually require the student to translate a few sentences from Arabic to English and English to Arabic.
 

<!--chapter:end:index.Rmd-->

# Nouns

Nouns are words for people, animals, places or things. Here is an example of a noun: "a boy". 

In Arabic, "a boy" is [وَلَد]{.ar}.

Note that in [وَلَد]{.ar}, the [و]{.ar} and [ل]{.ar} have a [fatHah]{.trn} but [د]{.ar} does not have any mark on it. For now, we will pretend that there is a [sukUn]{.trn} on [د]{.ar} so we will pronounce the word as [walad]{.trn}.

Here are some more Arabic nouns:

| English | Arabic |
|:--------|:-------------------|
| a boy   | [وَلَد]{.ar}  [walad]{.trn} |
| a lion  | [أَسَد]{.ar}  [asad]{.trn} |
| a house | [بَيْت]{.ar}  [bayt]{.trn} |
| a book  | [كِتَاب]{.ar} [kitAb]{.trn} |

In English we can say "a boy" or "the boy". Arabic does not have a word for "a" but it does have a word for "the".

The word for "the" in Arabic is [اَلْ]{.ar} [al]{.trn}. 

[اَلْ]{.ar} is joined to the noun. So "the boy" is [اَلْوَلَد]{.ar} "al-walad".

If an Arabic noun does not have [اَلْ]{.ar} joined to it then in English we will say the noun with "a".

+ [اَلْوَلَد]{.ar} "the boy"
+ [وَلَد]{.ar} "a boy"

Here are the nouns we saw earlier, with [اَلْ]{.ar}:

| Arabic | English |
|:----------------------|:-----------|
| [اَلْوَلَد]{.ar}  [al-walad]{.trn} | the boy   |
| [اَلْأَسَد]{.ar}  [al-asad]{.trn} |  the lion  |
| [اَلْبَيْت]{.ar}  [al-bayt]{.trn} |  the house |
| [اَلْكِتَاب]{.ar} [al-kitAb]{.trn} | the book  |

::: {.infobox data-latex="{caution}"}
**NOTE TO INSTRUCTOR**

It seems better to me to leave out [الحروف الشمسية والقمرية]{.ar} for now. It should be okay if the student pronounces [الدراجة]{.ar} as [al-darrAjah]{.trn} instead of [ad-darrAjah]{.trn}. In-shaa-Allah he will become familiar with the correct pronunciation when he reads it fully vowellized [الدَّرَّاجَة]{.ar} and with Quranic tajweed instruction.
:::

## Vocabulary

::: {.infobox data-latex="{caution}"}
**NOTE TO INSTRUCTOR**

The student should maintain a personal dictionary in a notebook. Set aside a few pages for:

1. Nouns
2. Verbs
3. Adjectives
4. Particles

Whenever new vocabulary is given the student should copy the new word and its meaning to his dictionary under the appropriate section.

Our first vocabulary list includes many words and the instructor may wish to give them to the student a few at a time.

If the students have been given Arabic instruction in pre-school they may already be familiar with many of these words.
:::

Here is a word list to memorize.

| Arabic | English |
|:----------------------|:--------------|
|[وَلَد]{.ar}   [walad]{.trn}    | a boy   |
|[أَسَد]{.ar}   [asad]{.trn}     | a lion   |
|[بَيْت]{.ar}   [bayt]{.trn}     | a house   |
|[كِتَاب]{.ar}  [kitAb]{.trn}    | a book   |
|[قِرْد]{.ar}   [qird]{.trn}     | a monkey   |
|[كَلْب]{.ar}   [kalb]{.trn}     | a dog   |
|[قِطَّة]{.ar}   [qiTTah]{.trn}   | a cat   |
|[سَيَّارَة]{.ar} [sayyArah]{.trn} | a car   |
|[دَرَّاجَة]{.ar} [darrAjah]{.trn} | a bike   |
|[مَسْجِد]{.ar}  [masjid]{.trn}   | a masjid   |
|[تُفَّاحَة]{.ar} [tuffAHah]{.trn} | an apple   |
|[مَوْزَة]{.ar}  [mawzah]{.trn}   | a banana   |
|[بُرْتُقَالَة]{.ar} [burtuqAlah]{.trn}   | an orange   |
|[بَيْضَة]{.ar}  [bayDah]{.trn}   | an egg   |
|[مَدْرَسَة]{.ar} [madrasah]{.trn} | a school   |
|[كُرَة]{.ar}   [kurah]{.trn}    | a ball   |
|[قَلَم]{.ar}   [qalam]{.trn}    | a pen   |
|[حَدِيقَة]{.ar} [HadIqah]{.trn}  | a garden |


::: {.infobox data-latex="{caution}"}
**NOTE TO INSTRUCTOR**

In drills, when writing the definite article [ال]{.ar} deliberately leave it without [tackIl]{.trn} in order to get the student familiarized with reading it.

Also, let the student write Arabic without any [tackIl]{.trn} on the letters. We will later ask him to vowelize only disambiguating letters, e.g. [كتبتُ]{.ar} vs [كتبتَ]{.ar}.
:::



## Drill 1 {-}

Translate from Arabic to English
Translate from Arabic to English



## Answer key for drill 1 {-}



## Drill 2 {-}

Translate from Arabic to English
Translate from Arabic to English



## Answer key for drill 2 {-}



<!--chapter:end:001.Rmd-->

# Verbs

Verbs are action words. Here are some examples of verbs:

+ rode
+ ate

Here are the verbs in Arabic:

| Arabic | English |
|:----------|:--------------|
|[رَكِبَ]{.ar} | he rode |
|[أَكَلَ]{.ar} | he ate |

Did you notice that in Arabic the verbs all mean "he" did something? This is because in Arabic the word "he" is part of the verb. If we want to say "she rode" or "I rode" or "You rode" the verb is modified. But we will learn all those later in-shaa-Allaah. For now, we will focus on "he" verbs because they are the easiest.

### Sentences with verbs

Here is a sentence with a verb:

"He rode a bike."

Let's see how to say this sentence in Arabic.

The verb "he rode" is [رَكِبَ]{.ar} and the noun "a bike" is [دَرَّاجَة]{.ar}. So our sentence is:

[رَكِبَ الدَّرَّاجَة]{.ar}  
"He rode a bike."

What if we want to say: "The boy rode the bike"?

In this case we still use the verb [رَكِبَ]{.ar} "he rode". But now, when we put the noun [الوَلَد]{.ar} next to it, we cross out the "he" in "he rode" and say "the boy rode".

[رَكِبَ الوَلَد الدَّرَّاجَة]{.ar}  
"The boy ~~he~~ rode the bike."  
"The boy rode the bike."

Note also that in Arabic the verb usually comes first. Then the person who does the action. And then the other noun.

Let's take a look at a few more examples:

"The boy rode a bike."  
[رَكِبَ الوَلَد درَّاجَة]{.ar}  

"A boy rode a bike."  
[رَكِبَ وَلَد درَّاجَة]{.ar}  

"Zayd rode the bike."  
[رَكِبَ زَيْد الدَّرَّاجَة]{.ar}  

## Vocabulary

he rode
he ate
he drank
he wrote
he read
water
milk


<!--chapter:end:002.Rmd-->

# Prepositions

Prepositions are words like "to", "in", "on", "from".

Here are some Arabic prepositions

| Arabic | English |
|:----------------|:---------|
|[إِلَىٰ]{.ar} [ilA]{.trn}  | to |
|[فِي]{.ar}  [fI]{.trn}   | in |
|[عَلَىٰ]{.ar} [ealA]{.trn} | on |
|[مِنْ]{.ar}  [min]{.trn}  | from |

Note that [إِلَىٰ]{.ar} and [عَلَىٰ]{.ar} end with [ىٰ]{.ar}: a [yaa]{.trn} with no dots and with a tiny [alif]{.trn} on top of it. This is pronounced like an [alif]{.trn}.

Prepositions come before nouns just like in English. Examples:

[إِلَىٰ المَسْجِد]{.ar}  
"to the masjid"

[فِي بَيْت]{.ar}  
"in a house"

[عَلَىٰ كِتَاب]{.ar}  
"on a book"

[مِنْ الوَلَد]{.ar}  
"from the boy"

::: {.infobox data-latex="{caution}"}
**NOTE TO INSTRUCTOR**

Notice that we are leaving the [sukUn]{.trn} on [مِنْ]{.ar} even when followed by a [همزة وصل]{.ar}. This is so as not to overburden the student. He may pronounce the phrase as [min al-walad]{.trn} instead of [mina l-walad]{.trn}.

Similarly, the student may pronounce [ilA al-masjid]{.trn} and [fI al-bayt]{.trn} instead of [ila l-masjid]{.trn} and [fi l-bayt]{.trn}.
:::

We can use prepositions in sentences with verbs as well:

[ذَهَبَ الوَلَد إلَىٰ البَيْت]{.ar}  
"The boy went to the house."


<!--chapter:end:003.Rmd-->

# Adjectives

Adjectives are words that describe nouns. Here are some adjectives in English:

+ big
+ small
+ good
+ fast

We can describe some nouns using these adjectives:

+ "a big house"
+ "a small cat"
+ "the good boy"
+ "the fast car"

Here are the Arabic adjectives:

| Arabic | English |
|:----------|:--------------|
|[كَبِير]{.ar} | big |
|[صَغِير]{.ar} | small |
|[حَسَن]{.ar} | good |
|[سَرِيع]{.ar} | fast|

In English we put the adjective before the noun, but in Arabic we put the adjective after the noun:

[بَيْت كَبِير]{.ar}  
"a big house"

[كَلْب صَغِير]{.ar}  
"a small dog"

However, adjectives are little more complicated in Arabic than in English. In Arabic, if the noun ends with a [ة]{.ar}, then a [ة]{.ar} is added to the adjective as well. For example,

[قِطَّة صَغِيرَة]{.ar}  
"a small cat"

When adding a [ة]{.ar}, the letter before the [ة]{.ar} always gets a [fatHah]{.trn}.

Adding [ة]{.ar} to the adjective is also done when the noun refers to a girl or a woman, even if the noun does not have a [ة]{.ar}.

"A mother" in Arabic is [أُمّ]{.ar}. If we want to say "a good mother" we will say

[أُمّ حَسَنَة]{.ar}  
NOT  
[أُمّ حَسَنَ]{.ar}  

Another rule for adjectives is that if the noun has [ال]{.ar} "the", then the adjective will also have [ال]{.ar}:

[الوَلَد الحَسَن]{.ar}  
"the good boy" (We still say in English "the good boy", not "the good the boy")

Now how about if the noun has both [ال]{.ar} and [ة]{.ar}? Well, we add both [ال]{.ar} and [ة]{.ar} to the adjective as well:

[السَّيَّارَة السَّرِيعَة]{.ar}  
"the fast car"

### Vocabulary

big
small
fast
good
beautiful
mother
tree
flower

<!--chapter:end:004.Rmd-->

# Multiple adjectives, "and"

In English sometimes we can use multiple adjectives to describe the same noun. For example:

"the big red apple"

We can have multiple adjectives in Arabic as well. We put them both after the noun.

[التُّفَّاحَة الكَبِيرَة الحَمْرَاء]{.ar}  
"the big red apple"

Sometimes we can put the word "and" between the adjectives:

"a fast and small car"

The Arabic word for and is [وَ]{.ar}. We can use it between adjectives:

[سَيَّارَة سَرِيعَة وَصَغِيرَة]{.ar}  
"a fast and small car"

Did you notice that [وَ]{.ar} "and" is written right next to the second word without any space? This is the rule for writing [وَ]{.ar} in Arabic.

[وَ]{.ar} can be used with nouns and verbs as well. Examples:

[أَكَلَ زَيْد تُفَّاحَة وَبُرتُقَالَة]{.ar}  
"Zayd ate an apple and an orange."

[أَكَلَ زَيْد الطَّعَام وَشَرِبَ المَاء]{.ar}  
"Zayd ate the food and he drank the water."

What if we have more than two items? In English we use commas, and write "and" for the last item.

"He ate an apple, an orange, and a banana."

In Arabic we don't use commas between multiple items. Instead we keep putting [وَ]{.ar}:

[أَكَلَ تُفَّاحَة وَبُرْتُقَالَة وَمَوْزَة]{.ar}  
"He ate an apple, an orange, and a banana."

## Vocabulary

tall
short
delicious
he sat
chair
desk
cold
girl
man


<!--chapter:end:005.Rmd-->

# Colors

Colors are adjectives. Just like you can say "a fast car" you can also say "a red car".

Here are some colors in Arabic:

|Arabic  |English |
|:------------ |:------------|
|[بُنِّيّ]{.ar}    | brown   |
|[بُرْتُقَالِيّ]{.ar}| orange   |
|[بَنَفْسَجِيّ]{.ar} | purple   |
|[وَرْدِيّ]{.ar}   | pink   |
|[أَحْمَر]{.ar}   | red   |
|[أَخْضَر]{.ar}   | green   |
|[أَصْفَر]{.ar}   | yellow   |
|[أَزْرَق]{.ar}   | blue   |
|[أَسْوَد]{.ar}   | black   |
|[أَبْيَض]{.ar}   | white   |

When using colors to describe nouns, then as we have already learned, if the noun has [ال]{.ar} then we add [ال]{.ar} to the color as well. Examples:

[كِتَاب أَحْمَر]{.ar}  
"a red book"

[الكِتَاب الأَحْمَر]{.ar}  
"the red book"

[قَلَم بُرْتُقَالِيّ]{.ar}  
"an orange pen"

[القَلَم البُرْتُقَالِيّ]{.ar}  
"the orange pen"

Did you notice that the words for the colors in Arabic are in two groups:

1. Those that end in [ـِيّ]{.ar} :
   + [بُنِّيّ]{.ar}    
   + [بُرْتُقَالِيّ]{.ar}
   + [بَنَفْسَجِيّ]{.ar} 
   + [وَرْدِيّ]{.ar}
2. Those that are all in the same pattern like:
   + [أَحْمَر]{.ar}
   + [أَخْضَر]{.ar}
   + [أَصْفَر]{.ar}
   + [أَزْرَق]{.ar}
   + [أَسْوَد]{.ar}
   + [أَبْيَض]{.ar}

Each of these groups is treated differently when using them to describe nouns that end in [ة]{.ar}

The first group that ends in [ـِيّ]{.ar} is treated the same way as we have already studied: If the noun has [ة]{.ar}, then we add [ة]{.ar} to the adjective as well. For example:

[زَهْرَة وَرْدِيَّة]{.ar}  
"a pink flower"

[السَّيَّارَة البُنِّيَّة]{.ar}  
"the brown car"

For the second group, when the noun ends with [ة]{.ar}, then we modify the colors in a different way:

   + [أَحْمَر]{.ar} becomes [حَمْرَاء]{.ar}
   + [أَخْضَر]{.ar} becomes [خَضْرَاء]{.ar}
   + [أَصْفَر]{.ar} becomes [صَفْرَاء]{.ar}
   + [أَزْرَق]{.ar} becomes [زَرْقَاء]{.ar}
   + [أَسْوَد]{.ar} becomes [سَوْدَاء]{.ar}
   + [أَبْيَض]{.ar} becomes [بَيْضَاء]{.ar}

Note that they are all modified in the same pattern.

So now we can say:

[زَهْرَة حَمْرَاء]{.ar}  
"a red flower"

[السَّيَّارَة الزَّرْقَاء]{.ar}  
"the blue car"

By the way, remember that nouns for girls and women are treated like they have [ة]{.ar} even if they don't actually have [ة]{.ar}. For example

[بِنْت حَمْرَاء]{.ar}  
"a red girl"


<!--chapter:end:006.Rmd-->

# Verb conjugations: "she"

We have learned how to say verbs for "he". Examples:

| English | Arabic |
|:----------|:--------------|
|he went |[ذَهَبَ]{.ar} | 
|he rode |[رَكِبَ]{.ar} | 
|he ate | [أَكَلَ]{.ar} | 

If we want to say "I went" or "you went" or "she went" we have to modify the verb. Today we will learn how to say "she" verbs. In-shaa-Allah next time we will kearn how to say "you" and "I" verbs.

| English | Arabic |
|:--------------------|:--------------|
|he went           |[ذَهَبَ]{.ar} | 
|she went          | [ذَهَبَتْ]{.ar} |

Examples:

[ذَهَبَ إِلَى المَسْجِد.]{.ar}  
"He went to the masjid."

[ذَهَبَتْ إِلَى المَسْجِد.]{.ar}  
"She went to the masjid."

These modifications are the same for all verbs. Example:

[رَكِبَتْ دَرَّاجَة.]{.ar}  
"She rode a bike."

Now, remember that if we want to say "Zayd went to the masjid", then we use the "he went" verb and cross out the "he"

[ذَهَبَ زَيْد إِلَى المَسْجِد.]{.ar}  
"Zayd ~~he~~ went to the masjid."  
"Zayd went to the masjid."

Similarly, if we want to say "Zaynab went to the masjid", then we use the "she went" verb and cross out the "she"

[ذَهَبَتْ زَيْنَب إِلَى المَسْجِد.]{.ar}  
"Zaynab ~~she~~ went to the masjid."  
"Zaynab went to the masjid."

Similarly,

[أَكَلَتْ الأُمّ الطَّعَام]{.ar}  
"The mother ate the food."

### It {-}

Arabic only has verbs for "he" and "she". It doesn't have any word for "it". So if you have sentence in English where an animal or a non-living thing does something, then you check if its noun has a [ة]{.ar}.

If it does not have [ة]{.ar} then we use the "he" verb. If it has a [ة]{.ar} then we use the "she" verb.

For example if you are talking about a dog and you say "It drank the water.", you will say:

[شَرِبَ المَاء.]{.ar}  
"It drank the water."

and

[شَرِبَ الكَلْب المَاء.]{.ar}  
"The dog drank the water."

Similarly, if you are talking about a car and you say "It went to the school.", you will say:

[ذَهَبَتْ إِلَى المَدْرَسَة.]{.ar}  
"It went to the school."

and

[ذَهَبَتْ السَّيَّارَة إِلَى المَدْرَسَة.]{.ar}  
"The car went to the school."

::: {.infobox data-latex="{caution}"}
**NOTE TO INSTRUCTOR**

I'm not modifying the [sukUn]{.trn} in [ذَهَبَتْ السيارة]{.ar} to a [kasrah]{.trn}: [ذَهَبَتِ السيارة]{.ar}. This is so the student does not confuse it with [ذَهَبْتِ]{.ar} which we will learn next time in-shaa-Allah. It is ok if the student pronounces [pahabat al-sayyArah]{.trn} instead of [pahabati l-sayyArah]{.trn} (or [pahabati s-sayyArah]{.trn}).
:::



<!--chapter:end:007.Rmd-->

# Verb conjugations: "you" and "I"

Last time we learned how to say "she" verbs, in addition to "he" verbs. Today we will learn how to say "you" and "I" verbs.

| English | Arabic |
|:--------------------|:--------------|
|he went           |[ذَهَبَ]{.ar} | 
|she went          | [ذَهَبَتْ]{.ar} |
|you^(boy)^ went   | [ذَهَبْتَ]{.ar} |
|you^(girl)^ went  | [ذَهَبْتِ]{.ar} |
|I went            | [ذَهَبْتُ]{.ar} |

Example:

[ذَهَبَتُ إِلَى المَسْجِد.]{.ar}  
"I went to the masjid."

[أَكَلْتُ مَوْزَة.]{.ar}  
"I ate a banana."

Did you notice that Arabic has two verbs for "you". One is for if you are talking to a boy and the other is if you are talking to a girl.

So if you say to a boy: "You went to the masjid", you would say:

[ذَهَبْتَ إِلَى المَسْجِد.]{.ar}  
"You^(boy)^ went to the masjid."

However, if you were talking to a girl, you would say:

[ذَهَبْتِ إِلَى المَسْجِد.]{.ar}  
"You^(girl)^ went to the masjid."



<!--chapter:end:008.Rmd-->

# "with", "above", and "under"

### "with" {-}

The word for "with" in Arabic is [ب]{.ar}.

[ب]{.ar} comes before a word and is joined to it. For example:

[كُرَة]{.ar}  
"a ball"

[بِكُرَة]{.ar}  
"with a ball"

If a word has [ال]{.ar} then [ب]{.ar} is joined to the [ال]{.ar}.

[الكُرَة]{.ar}  
"a ball"

[بِالكُرَة]{.ar}  
"with a ball"

[ب]{.ar} is joined to the [ال]{.ar}.When [ب]{.ar} is joined to [ال]{.ar}, we don't pronounce the [ا]{.ar} in [ال]{.ar}

[بِالكُرَة]{.ar} is pronounced [bil-kurah]{.trn}.

We can use [ب]{.ar} in a sentence:

[لَعِبَ زَيْد بِالكُرَة الصَّغِيرَة]{.ar}  
"Zayd played with the small ball."

### "above" and "under" {-}

The word for above is [فَوْقَ]{.ar}.

[فَوْقَ الشَّجَرَة]{.ar}  
"above the tree."

Similarly, the word for under is [تَحْتَ]{.ar}.

[تَحْتَ الشَّجَرَة]{.ar}  
"under the tree."


<!--chapter:end:009.Rmd-->

# Verbs "run" and "see"

Today we will learn two new verbs: "he ran" and "he saw".

The verb "he ran" is [جَرَىٰ]{.ar}. It has a [ىٰ]{.ar} at the end which is pronounced like an [ا]{.ar}, just like in [إِلَىٰ]{.ar} and [عَلَىٰ]{.ar}.

[جَرَىٰ زَيْد فِي الحَدِيقَة.]{.ar}  
"Zayd ran in the garden."

Let's see how to say "she ran", "you ran" and "I ran".

| English | Arabic |
|:--------------------|:--------------|
|he ran           | [جَرَىٰ]{.ar} | 
|she ran          | [جَرَتْ]{.ar} |
|you^(boy)^ ran   | [جَرَيْتَ]{.ar} |
|you^(girl)^ ran  | [جَرَيْتِ]{.ar} |
|I ran            | [جَرَيْتُ]{.ar} |

When we say "she ran" we drop the [ىٰ]{.ar} and say [جَرَتْ]{.ar} [jarat]{.trn}.

[جَرَتْ البِنْتُ في الحَدِيقَة]{.ar}  
"The girl ran in the garden."

And when we say "you ran" and "I ran" the [ىٰ]{.ar} becomes a normal [ي]{.ar} with a sukoon. Example:

[جَرَيْتَ في الحَدِيقَة]{.ar}  
"You ran in the garden."

Another verb just like [جَرَىٰ]{.ar} "he ran" is [رَأَىٰ]{.ar} "he saw"

| English | Arabic |
|:--------------------|:--------------|
|he saw           | [رَأَىٰ]{.ar} | 
|she saw          | [رَأَتْ]{.ar} |
|you^(boy)^ saw   | [رَأَيْتَ]{.ar} |
|you^(girl)^ saw  | [رَأَيْتِ]{.ar} |
|I saw            | [رَأَيْتُ]{.ar} |


<!--chapter:end:010.Rmd-->

# This, What?, Who?

Let's see how to say the sentence "This is a man."

The word for "this" is [هَـٰذَا]{.ar}. It is pronounced [hApA]{.trn}.

In Arabic we usually don't write any word for "is". So then we can say:

[هَـٰذَا رَجُل]{.ar}  
"This is a man."

Let's see now how to say "This is a girl." When we are talking about a girl, or a noun that has [ة]{.ar} we don't use [هَـٰذَا]{.ar}. Instead we use [هَـٰذِهِ]{.ar} [hApihi]{.trn}.

[هَـٰذِهِ بِنْت]{.ar}  
"This is a girl."

[هَـٰذِهِ قِطَّة]{.ar}  
"This is a cat."

[هَـٰذَا كَلْب]{.ar}  
"This is a dog."

### Questions {-}

We can ask a question "What is this?" The word for "What" is [مَا]{.ar}. Again, we don't write any word for "is". 

So if we are asking about noun which does not have [ة]{.ar} then we say:

[مَا هَـٰذَا؟ هَـٰذَا كَلْب]{.ar}  
"What is this? This is a dog."

But if we are asking about a noun which has [ة]{.ar} then we say:

[مَا هَـٰذِهِ؟ هَـٰذِهِ شَجَرَة]{.ar}  
"What is this? This is a tree."

Now if we are talking about a person, then we don't say "What is this?" Instead we say, "Who is this?"

The word for "who" is [مَنْ]{.ar}.


[مَنْ هَـٰذَا؟ هَـٰذَا رَجُل]{.ar}  
"Who is this? This is a man."

[مَنْ هَـٰذِهِ؟ هَـٰذِهِ بِنْت]{.ar}  
"Who is this? This is a girl."


<!--chapter:end:011.Rmd-->

# That

Last time we learned two words for "this":

1. [هَـٰذَا]{.ar} for boys or if the noun does not have [ة]{.ar}.
2. [هَـٰذِهِ]{.ar} for girls or if the noun has [ة]{.ar}.

Today, in-shaa-Allah we will learn how to say "that":

1. [ذَ ٰلِكَ]{.ar} for boys or if the noun does not have [ة]{.ar}.
2. [تِلْكَ]{.ar} for girls or if the noun has [ة]{.ar}.

[مَا ذَ ٰلِكَ؟ ذَ ٰلِكَ كَلْب]{.ar}  
"What is that? That is a dog."

[مَا تِلْكَ؟ تِلْكَ شَجَرَة]{.ar}  
"What is that? That is a tree."

[مَنْ ذَ ٰلِكَ؟ ذَ ٰلِكَ رَجُل]{.ar}  
"Who is that? That is a man."

[مَنْ تِلْكَ؟ تِلْكَ بِنْت]{.ar}  
"Who is that? That is a girl."

From now on we will write [هَذَا، هَذِهِ، ذَلِكَ]{.ar} instead of [هَـٰذَا، هَـٰذِهِ، ذَ ٰلِكَ]{.ar}. But you must remember to read them with the [alif]{.trn}.

<!--chapter:end:012.Rmd-->

# Nominal sentence

We have learned that Arabic doesn't have a word for "is". So if we want to say "This is a man", we will say,

[هَذِهِ مَرْأَة]{.ar}  
"This is a woman."

We can replace "this" with a noun:

[الأُمّ مَرْأَة]{.ar}  
"The mother is a woman."

We can also use proper nouns:

[زَيْنَب مَرْأَة]{.ar}  
"Zaynab is a woman."

[المَرْأَة زَيْنَب]{.ar}  
"The woman is Zaynab."

Now we will learn how to say sentences with adjectives like "The man is big."

First we write the word for "the man"[الرَّجُل]{.ar}. Then we don't write any word for "is". And, finally, we write the adjective [كَبِير]{.ar} "big" without [ال]{.ar}.

[الرَّجُل كَبِير]{.ar}  
"The man is big."

How about "The woman is big."? Now we will use the adjective [كَبِيرَة]{.ar} with [ة]{.ar}.

[المَرْأَة كَبِيرَة]{.ar}  
"The woman is big."

We can have proper nouns as well:

[زَيْدٌ كَبِير]{.ar}  
"Zayd is big."

[زَيْنَب كَبِيرَة]{.ar}  
"Zaynab is big."

We can also use colors as adjectives:

[الكِتَاب أَحْمَر]{.ar}  
"The book is red."

[الكُرَة حَمْرَاء]{.ar}  
"The ball is red."



<!--chapter:end:013.Rmd-->

# Detached pronouns, so

## Detached pronouns

In this chapter we will learn how to say pronouns. Here are the pronouns in Arabic.

| English | Arabic |
|:--------|:--------|
|He         |[هُوَ]{.ar} |
|She        |[هِيَ]{.ar} |
|I          |[أَنَا]{.ar} |
|You^(boy)^ |[أَنْتَ]{.ar} |
|You^(girl)^|[أَنْتِ]{.ar} |

"I" [أَنَا]{.ar} is always pronounced [Eana]{.trn} not [EanA]{.trn}

Examples:

## So

The Arabic word for "so" is [فَ]{.ar}. It is always joined to the word after it.

[ذَهَبَ الوَلَد إِلَى ال]

[رَأَىٰ الوَلَد الكُرَة فِي الحَدِيقَة فَلَعِبَ بِالكُرَة]{.ar}  
"Zayd saw the ball in the garden so he played with the ball."

[فَهُوَ]{.ar}

<!--chapter:end:014.Rmd-->

# Yes, no questions

Here are "yes" and "no" in Arabic

| English | Arabic |
|:--------|:---------|
|Yes  |[نَعَمْ]{.ar} |
|No   |[لا]{.ar} |

A "yes-no" question is one whose answer is either "yes" or "no". For example,

+ "Did you open the door?"
+ "Is the book heavy?"

In Arabic it is very easy to form these questions. You take a statement and put the word [هَلْ]{.ar} in front.

Statement:  
[فَتَحْتَ البَاب.]{.ar}  
"You opened the door."

Question:
[هَلْ فَتَحْتَ البَاب.]{.ar}  
"Did you open the door?"

Statement:  
[الكِتَاب ثَقِيل.]{.ar}  
"The book is heavy."

Question:  
[هَلْ الكِتَاب ثَقِيل.]{.ar}  
"Is the book heavy?"

When translating from Arabic to English, first ignore the word [هَلْ]{.ar} and translate with a questioning tone. Then reform the question into better English. For example:

[هَلْ أَنْتَ قَرِيب؟]{.ar}  
"You are near?" = "Are you near?"

[هَلْ ذَهَبَ إِلَى البَيْت؟]{.ar}  
"He went to the house?" = "Did he go to the house?"

<!--chapter:end:015.Rmd-->

# More questions

We have learned that [مَا]{.ar} "what" and [مَنْ]{.ar} "who" can be used to ask questions.

[مَا هَذَا؟ هَذَا كِتَاب.]{.ar}  
"What is this? This is a book."


[مَنْ هَذِهِ؟ هَذَا مَرْأَة.]{.ar}  
"Who is this? This is a woman."

Arabic also has another word for "what": [مَاذَا]{.ar}. 

[مَاذَا]{.ar} is generally used with verbs instead of [مَا]{.ar}.

[مَاذَا رَكِب؟ رَكِبَ الدَّرَّاجَة]{.ar}  
"What he rode?" = "What did he ride?"  
"He rode the bike."

We can use [مَاذَا]{.ar} with prepositions before it.

[فِي مَاذَا وَضَعْتَ الكِتِاب؟ وَضَعْتُ الكِتَاب في الحَقِيبَة]{.ar}  
"In what you put the book?" = "In what did you put the book?"  
"I put the book in th ebag."

[بِمَاذَا لَعِبَ الوَلَد؟ لَعِبَ الوَلَد بِالكُرَة.]{.ar}  
"With what the boy played?" = "With what did the boy play?"  
"The boy played with the ball."

## [مَعَ]{.ar}

We already learned the word [بِ]{.ar} which means "with".

Arabic has another word [مَعَ]{.ar} which also means "with".

[بِ]{.ar} is generally used if you do something with an object, e.g., you play _with_ a ball, you open a door _with_ a key.

::: {.infobox data-latex="{caution}"}
**NOTE TO INSTRUCTOR**

For now, we will not consider usages of the type:

[ذَهَبَ بِالرَّجُل و جَاءَ بِه]{.ar}  
"To take someone or bring someone to ..."
:::

[مَعَ]{.ar} is used when you do something _together with_ someone else. For example,

[ذَهَبْتُ إِلَى المَدْرَسَة مَعَ زَيْد]{.ar}  
"I went to the school with Zayd."

[لَعِبَتْ البِنْت مَعَ زَيْنَب]{.ar}  
"The girl played with Zaynab."

[مَعَ]{.ar} can also be used in a question:

[مَعَ مَنْ لَعِبْتَ؟]{.ar}  
"With whom you played?" = "With whom did you play?"


<!--chapter:end:016.Rmd-->

# The possessive (Part I: 's)

In English we can say 

+ "a boy's book"
+ "the woman's house"
+ "Zayd's school"

In Arabic we simply place the nouns together but we reverse the order of the two nouns. And only the second noun gets [ال]{.ar} for "the". Here are the Arabic for the above examples:

|Arabic | English |
|:----------|:--------------|
|[كِتَاب-وَلَد]{.ar}   |"a boy's book"       |
|[بَيْت-المَرْأَة]{.ar} |"the woman's house"  |
|[مَدْرَسَة-زَيْد]{.ar}  |"Zayd's school"      |

For now we will put a hyphen "-" between the words which are connected with "'s".

::: {.infobox data-latex="{caution}"}
**NOTE TO INSTRUCTOR**

We're using a hyphen because two nouns can occur next to each other without being a possessive, e.g., [رَأَتْ أُمّ وَلَد]{.ar} which, without case endings can be either

+ "A woman saw a boy.", or
+ "She saw a boy's mother."

So without introducing case endings we think it will be easier to facilitate recognition of the possessive, at least where there is ambiguity.
:::

Also, we we say [مَدْرَسَة-زَيْد]{.ar} we will pronounce it [madrasat zayd]{.trn} not [madrasah zayd]{.trn}.

So when translating from Arabic to English, if you see two nouns together with a hyphen "-" between them, you should translate them with ('s).

Start with last noun. if it has [ال]{.ar} then write "the". Then go backwards and connect nouns with ('s).

[سَيَّارَة-الرُّجُل]{.ar}  
"the man's car"

[سَيَّارَة-رَجُل]{.ar}  
"a man's car"

[سَيَّارَة زَيْد]{.ar}  
"Zayd's car"

By the way we can add more nouns connected with "'s":

[مِفْتَاح بَاب بَيْت رَجُل]{.ar}  
"a man's house's door's key"

[مِفْتَاح بَاب بَيْت الرَّجُل]{.ar}  
"the man's house's door's key"

Note that [ال]{.ar} is added only to the last noun.

::: {.infobox data-latex="{caution}"}
**NOTE TO INSTRUCTOR**

It may be more idiomatic in English to say "The key of the door of the house of the man". But it will be hard to explain to the student how the multiple "the's" in English are translated.

And in the next chapter, for simplicity, we will reserve "of" for quantities and materials.
:::


<!--chapter:end:017.Rmd-->

# The possessive (Part II: of)

In English we can use the word "of" in expressions like:

+ "a cup of water"
+ "the box of cereal"

In Arabic we again place the nouns together but now we don't reverse the order of the two nouns. And again, only the second noun gets [ال]{.ar} for "the". Here are the Arabic for the above examples:

|Arabic | English |
|:----------|:--------------|
|[كُوب-مَاء]{.ar}   |"a cup of water"    |
|[عُلْبَة-الحُبُوب]{.ar} |"the box of cereal"    |

Note that even the english was "**the box** of cereal", in Arabic we will but [ال]{.ar} with the last noun: [عُلْبَة-الحُبُوب]{.ar}

To summarize, in English if you have two nouns connected with "'s" or "of", in Arabic we write the expression the same way, but the order is different. But in both cases, the [ال]{.ar}, if any, is added to the last Arabic word.

+ "'s": reverse order
+ "of": keep same order

Translating from Arabic to English, sometimes you can use either "'s" or "of". For example, "the book of the man", and "the man's book" mean more or less the same thing. But to make it simple, we will use "of" for quantites (of foods for example) and materials.

So we will [كِتَاب الرَّجُل]{.ar} as "the man's book" and keep "of" for "a cup of water" or "a piece of cake" or "the ring of gold" etc.

::: {.infobox data-latex="{caution}"}
**NOTE TO INSTRUCTOR**

Consider [رأسُ رجلٍ كبيرٌ]{.ar}

An idiomatic English translation is "the big head of a man". The "the" is because a man has only one head. But in Arabic [رأس]{.ar} is technically indefinite. So inorder to simplify the student, we sacrifice idiom for simplicity and instruct the student to translate as "A man's big head". By the way, we're not teaching adjective's with idaafah just yet, but we're thinking ahead and trying to stay simple and consistent.
:::


<!--chapter:end:018.Rmd-->

# Attached pronouns for possessive

iIn this chapter we will learn how to say "my", "your", "his", and "her". In Arabic we express this by attaching a suffix to the last part of the noun. Examples:

|English | Arabic |
|:----------|:--------------|
|His book          |[كِتَابُهُ]{.ar} |
|Her book          |[كِتَابُهَا]{.ar} |
|Your^(boy)^ book  |[كِتَابُكَ]{.ar} |
|Your^(girl)^ book |[كِتَابُكِ]{.ar} |
|My book           |[كِتَابِي]{.ar} |

For now we will put a [Dammah]{.trn} before adding the suffix, except for "my".

For nouns that end with [ة]{.ar}, it is converted to a regular [ت]{.ar} when adding the suffix.

Let's see how to say these for the noun [حَقِيبَة]{.ar} "bag".

|English | Arabic |
|:----------|:--------------|
|His bag          |[حَقِيبَتُهُ]{.ar} |
|Her bag          |[حَقِيبَتُهَا]{.ar} |
|Your^(boy)^ bag  |[حَقِيبَتُكَ]{.ar} |
|Your^(girl)^ bag |[حَقِيبَتُكِ]{.ar} |
|My bag           |[حَقِيبَتِي]{.ar} |



<!--chapter:end:019.Rmd-->

