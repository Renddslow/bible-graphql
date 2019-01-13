# Bible GraphQL

The Bible GraphQL API is designed to be everything I personally look for in a Bible API, with intent to use this as the basis for a simple (but advanced) Bible reader.

## What I want from a reader

- I want to be able to long-press/highlight a word and see information about the word inline (Greek/Hebrew, Transliteration, Strong's Number, Parsing/Conjugation).
- I want to be able to be able to do a word-study side-by-side with the passage I'm reading.
- I want to be able to select a character's name (e.g. Moses) and see a list of all the places that character played a role in the Biblical story. This would include Abram matching up with all Abraham stories.
- I want to be able to access commentary directly from the passage I'm reading.
- I want to be able to annotate books and sermons that make reference to a particular passage and easily find/purchase them from the reader.
- I want the data to Open Source and open to contribution.
- I want the reader to seamlessly convert between versed and unversed.
- I want a simple clean UI that is responsive and mobile first.
- I want to be able to track Biblical themes throughout the Bible without necessarily needing to do a word study.

## The problems with existing services/API's

- API's nearly all return the data as plain text or as some form of XML/HTML which make programmatic parsing messy.
- Most readers are cluttered and difficult to navigate.
- Most readers make it difficult to do things inline or in parallel to what you're currently reading.
- While there are plenty of beautiful readers out there, a la [ReadScripture](https://www.readscripture.org/) and [YouVersion](https://www.youversion.com/), few have the advanced tooling needed for sermon prep and word studies.
- The more advanced readers typically are not mobile friendly/responsive, and if they are, they lack tooling on a smaller screen.

## Pipeline

The plan is to start with the GraphQL API using the ASV or one of it's Public Domain heirs ([Josh Duff](https://github.com/TehShrike) has already done an excellent job converting the [World English Bible to JSON](https://github.com/TehShrike/world-english-bible)).

### Phase 0
1. Build out the GraphQL schema to support Verses, Characters, and Words
2. Import a version of the Bible and connect Verses queries to it.

### Phase 1
1. Apply for a DBL Card.
2. Import Strong's Concordance [TODO: Reference two sources for the Hebrew and Greek XML lexicons].
3. Map Strong's numbers to English words in current version.
4. Connect the Words queries.
5. Build contribution portal of some kind to continue work on mapping Strong's as well as mapping Character's to verses.


