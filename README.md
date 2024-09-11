This is the Template for Translating Noble Fates into another Language. New strings will be added here when the game receives updates.

# Official Translations
The Official Translations are Forks from this repository. They'll be Synced when new strings are added.

# Contributing to an Official Translation
Fork the translation's repository.

Sync when new strings are added to add them to your translation (recommend using Branch -> Update from upstream/main in Github windows client). 

Create Pull Requests with your changes. 

Key Contributors have the opportunity to earn the ability to Moderate the Fork for that language.

# Creating a new Translation
Fork this repository. 

Sync when new strings are added to add them to your translation (recommend using Branch -> Update from upstream/main in Github windows client). 

Unofficial Translations have the opportunity to become Official with sufficient completeness - reach out if you think yours qualifies.

# Testing a Translation
You can Test changes to a translation by adding it as a local mod.

Create a new folder under ```%AppData%\..\LocalLow\Xobermon, LLC\Noble Fates\Mods``` with the name you'd like.

Drop the game.loc file into that folder.

Add a Localization.octdat file with the following contents to replace an existing translation:
```
{
    id Oct.Localization.Languages.<language name here>
    type LocalizationLanguage
    appendonly
    
    files = 
    [
        $clear
        \game.loc
    ]
}
```

Or this, if it's a new one:
```
{
    id Oct.Localization.Manager
    type LocalizationManager
    appendonly
    
    localizedLanguages = 
    [
        <language name here>
    ]
}
{
    id Oct.Localization.Languages.<language name here>
    type LocalizationLanguage
    
    name = <language name here>
    
    files = 
    [
        \game.loc
    ]
}
```

When you run the game, the language should show up in the Language menu and your translations should take effect when you switch to that language.

Additional Notes on Creating a Mod are here: https://noblefates.userecho.com/knowledge-bases/2/articles/746-modding-noble-fates

# Translation Mods
Translation Mods that add new languages or extend existing ones are supported. Create a mod using the steps above under Testing a Translation, only adding a new Language instead of extending an existing one.

When satisfied, feel free to upload your mod to the Workshop from the Mod Menu in-game.

# Help
The best place to get help is on the Offical Noble Fates Discord: ```https://discord.gg/HeAaQcS```

# loc File Format
The loc File Format is a custom text format used for Noble Fates Translations.

## Single String Format
```
\\\\
\\
\\  Translation Notes
\\
\\	Key=Raw (English)
\\
\\\\
Key=Translation
```

## String Pool Format
```
\\\\
\\
\\  Translation Notes
\\
\\	Key+=Raw (English) 1
\\	Key+=Raw (English) 2
\\
\\\\
Key+=Translation 1
Key+=Translation 2
Key+=Translation 3
```

## Comments
Anything after a \\ on a given line is considered a comment, and is ignored by the game.

## Notes
Strings that are Untranslated will return the English Version. String Pools support any number of translations greater than 0. If no translations are provided, the English strings will be used. Blank Translations are treated as no translation.

If the English string doesn't contain a variable and it isn't listed in the Translation Notes, then it probably isn't available. Do what you can with what's available.

Generally, we do not translate unit abbreviations in the game - so p (Prestige), t (Trait Points), c (Coins), y (Yir), d (Day), h (Hour), m (Minute), n (Nutrition) are intentionally left untranslated.

The game has grammatical issues in English via limitations of its technology and attempts at humor. These are intentional, and it's likely that there will be more or less of them in each language. When writing text, we prioritize information delivery and tone over grammatical correctness.

.Advanced Strings signify places where we've made advances in the tech under the hood to allow for more nuance in translations. Generally these will be marked Optional and the strings they replace are marked Deprecated. It's only necessary to translate the Optional or Deprecated string and its children. We prefer using the .Advanced version for all new translations.

### .con Function
.con is a Conjugation function that conjugates between 1st, 2nd, and 3rd person depending on who the speaker and listener are relative to the character. These can be nested.

### .mf/.mfn Functions
These functions allow the substitution of Masculine, Feminine, or Neutral variants of Text based on the gender of the character (or string) before them.

# Closing
As always, feel free to reach out with issues. We're happy to help!


