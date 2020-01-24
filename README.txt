HOW TO RUN:

bash get_wiki_corpus_main.sh [language] [category] [output dir] [recurs: T/F] [max articles]

	1: language: target language/language of desired category. Language should be written in English.
		e.g.: "French", "Spanish"
	2: category: category to be retrieved from Wikipedia in target language, not English. In quotes if several words. 
		e.g.: "Physique" for FR, "Physics" for EN
	3: output dir: output directory where the final extracted articles will be placed. In quotes if several words.
	4: recurs: TRUE if want to recursively go into all found subcategories and retrieve articles there
	       	FALSE if only want to retrieve articles in the stated category (no recursion)
	
	if 4 = TRUE, specify 5 (or set 5 to FALSE)
	5: max articles: max number of articles to retrieve. Will retrieve them starting from the "root" category (or FALSE)

EXAMPLE:
	bash get_wiki_corpus_recurs.sh french "Traitement en maladie infectieuse" output_maladie true 2000

FILES GENERATED:
	- dir [output dir]/: all extracted articles 
	- wget_logfile: log file for wget command
	
WIKIEXTRACTOR:
	using WikiExtractor.py script by https://github.com/attardi/wikiextractor 
