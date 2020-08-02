# hangman
import random
import time

hanger = ['''
                 _____
                |     |
                      |
                      |
                      |
                      |
                     _|_''', '''
                 _____
                |     |
                O     |
                      |
                      |
                     _|_''', '''
                 _____
                |     |
                O     |
                |     |
                      |
                     _|_''', '''
                 _____
                |     |
                O     |
                |     |
                |     |
                     _|_''', '''
                 _____
                |     |
                O     |
               /|     |
                |     |
                     _|_''', ''' 
                 _____
                |     |
                O     |
               /|\    |
                |     |
                     _|_''', '''
                 _____
                |     |
                O     |
               /|\    |
                |     |
               /     _|_''', '''
                 _____
                |     |
                O     |
               /|\    |
                |     |
               / \   _|_''', '''
       ☆ ☆ ☆ ☆ ☆ ☆ ☆ ☆ ☆ ☆ ☆ ☆
       ☆ ☆ ☆ ☆ ☆ ☆ ☆ ☆ ☆ ☆ ☆ ☆    

                    \O/      
          ~WINNER~   |   ~WINNER~        
                     |    
                    / \ 

       ☆ ☆ ☆ ☆ ☆ ☆ ☆ ☆ ☆ ☆ ☆ ☆
       ☆ ☆ ☆ ☆ ☆ ☆ ☆ ☆ ☆ ☆ ☆ ☆''']
k = 1
time.sleep(1)
while k < 10:
    load = '\n' * 18 + '\t' * 9 + '>' * k + '\n' + '\t' * 9 + ' PENGUINS AND OTHER BIRDS ARE LOADING...' + '\n' * 18
    time.sleep(0.25)
    k += 1
    print(load)
time.sleep(1)
mainscreen = '\t' * 9 + 'WELCOME TO HANGMAN! \n' + '\t' * 9 + hanger[-2] + '\n' + '''
Guess the word letter by letter, to free the innocent man  and win the game!
Also you will help a penguin far away if you win!
Get ready!!'''
try:
    if loop != 3:
        loop = 0
except:
    loop = 0
while loop == 0:
    print('\n' * 18)
    print(mainscreen)
    strt = input("Start game?(Y/N):" + '\n' * 18)
    if strt in ["N", "n", "no", "NO", "No", "nO"]:
        print('\n' * 18)
        print("Goodbye!")
        print('\n' * 18)
        time.sleep(1)
        loop = 2
    else:
        loop = 1
        n = int(input('\n' * 18 + '''Sooooooooo lets start
What mode would you like to play?
1)Enter '1' for casual gamemode,
2)Enter '0' for timed gamemode and rember if you do a number different than 1 or 0 then it will be the number of seconds you have.
        ''' + '\n' * 18))
        if n == 1:
            n = ""
        elif n == 0:
            n = 60

    while loop == 1:
        word_list = '''anarchy mechaniapple bananna jalapeno metaphor couch habanero pepper walking dead oakdog genocide esterification
                     nut nuts peanut dayman hangman hangmanxenophobia looney atrocious asparagus detergent delinquent stature entrepreuner vegan zoo
                     rhetorical cathedral horse basketball telepathy malignant pepperoni tremendous tree barn chicken television phone chair
                     quarantine basketball trampoline tutorial umbrella trunks water ultraviolet infrared supersonic scrumptious
                     elevated escalate lament incorrigible switch cackle gaggle gargle table cat bate abnormal abode abrupt accelerate acclaim acknowledge acquire aspire acrid addict adjacent admonish affliction agitate ajar akin allege annihilate anonymous antagonize apathy arbitrate
astute authentic avert bellow beseech bestow bewilder bigot blatant bleak braggart brawl emblem endure ensure enthrall epidemic erode exuburant epilogue fanthom feud figment firebrand flabbergast flagrant flaw
fruitless gaudy geography vague lax obscure frog pen gratify gravity grim grimy gruel grueesome haggle headlong docile oblivious homage homicide hospitable hurtle owl turtle snow fox chess coins
spider robot history technology universe telecopes asssult bolster defective
hybrid overwhelm pamper patronize peevish pelt pending percevied illiterate obnoxious oration zen orthodox december light words tax trees wright mulch vanish prefix
german america practce frezing perjury permanent persist perturb pique pluck poised ponder potential predatory presume preview prior prowess radiant random ant water
hydrogen helium lithum  yittrium praseodymium rant recede reprimand resume retort robust rupture browse bystander candid canine canny capricious capsize sudden casual
casualty catastrophe cate book unknown format a i malware cater chorus citrus clamber climax nestling comprimise concur magpie confront congested conjure abate consult
carrupt counterfeit covet customary debut decreased dependent dispondent detach devour dishearten dismal dismantle impede implore incredible incredulous infamous
infuriate insinuate intense intenseified inundate irate lavish legacy legitimate lethal loath lurk magnetic mirth quench magnitude pineapple tigers tiger kingfisher
kingfishers penguin penguins quail quails gynmoserms angiosperms gamma epiderms pennsylvania cuticle geometry 
finces herons wans greebes abruptly absurd abyss affix askew
avenue awkward axiom azure bagpipes bandwagon banjo bayou beekeeper bikini blitz blizzard boggle bookworm boxcar boxful buckaroo buffalo buffoon buxom buzzard buzzing buzzwords caliph cobweb cockiness croquet
crypt curacao cycle daiquiri dirndl disavow dizzying duplex dwarves embezzle ensemble equip espionage euouae exodus faking fishhook fixable fjord flapjack flopping
fluffiness flyby foxglove frazzled frizzled fuchsia funny gabby galaxy galvanize gazebo giaour gizmo glowworm glyph gnarly gnostic gossip grogginess haiku haphazard
hyphen iatrogenic icebox injury ivory ivy jackpot jaundice jawbreaker jaywalk jazziest jazzy jelly jigsaw jinx jiujitsu jockey jogging joking jovial joyful juicy jukebox
jumbo kayak kazoo keyhole khaki kilobyte kiosk kitsch kiwifruit klutz knapsack larynx lengths lucky luxury lymph marquis matrix megahertz microwave mnemonic mystify naphtha
nightclub nowadays numbskull nymph onyx ovary oxidize oxygen pajama peekaboo phlegm pixel pizazz pneumonia polka pshaw psyche puppy puzzling puzzle quartz queue quips quixotic quiz
quizzes quorum razzmatazz rhubarb rhythm rickshaw schnapps scratch shiv snazzy sphinx spritz squawk staff strength strengths stretch stronghold stymied subway swivel syndrome thriftless thumbscrew
topaz transcript transgress transplant triphthong twelfth twelfths unknown unworthy unzip uptown vaporize vixen vodka voodoo vortex voyeurism walkway waltz wave wavy waxy wellspring wheezy whiskey
whizzing whomever wimpy witchcraft wizard woozy wristwatch wyvern xylophone yachtsman yippee yoked youthful yummy zephyr zigzag zigzagging zilch zipper zodiac zombie
 aberration conciliatory incessant abstract contract incidental
accolade copious incite accommodate	cordial incorrigible aesthetic dearth indict affinity debilitate indoctrinate altercation decadence insurgent ameliorate deference intangible amicable delineate judicious
anarchy	deprecate lavish anomaly despot listless appall devious meager archaic didactic meander arduous disparage negligent articulate dissonance obliterate duplicity ponderous authoritarian edifice preclude aversion effervescent prerequisite biased egregious proximity brevity elusive rectify cajole equivocal rescind
callous erroneous resolution capitulate exemplary rigorous catalyst expedient scrutinize catharsis extraneous substantiate caustic formidable surmise censure	frivolous tirade
chastise  turbulence clamor haphazard unimpeachable coalesce heretic unobtrusive cognizant hindrance usurp commiserate hypocrisy vacillate composure iconoclast whimsical
accommodate jewellery leisure misspell neighbour intelligence pronunciation handkerchief logorrhea chiaroscurist acknowledgement prognostication antepenultimate acclimatizationpseudopseudohypoparathyroidism floccinaucinihilipilification antidisestablishmentarianism
honorificabilitudinitatibus thyroparathyroidectomized dichlorodifluoromethane incomprehensibilities pneumonoultramicroscopicsilicovolcanoconiosis 
yellow-billed-cuckoo - coccyzus-americanus yellow-crowned-night-heron nyctanassa-violacea yellow-rumped-cacique cacicus-cela xanthic xanthippe xanthocarpous xanthochroia
compartmentalization hyperlipoproteinemia semiautobiographical
ABANDONMENTS ABANDONWARES ABBREVIATING ABBREVIATION ABBREVIATORS ABBREVIATORY ABBREVIATURE ABECEDARIANS ABERRATIONAL ABHORRENCIES ABIOTROPHIES ABIRRITATING 
ABJECTNESSES ABLACTATIONS ABNORMALISMS ABOLISHMENTS ABOLITIONARY ABOLITIONISM ABOLITIONIST ABOMINATIONS ABORIGINALLY ABORTIONISTS ABORTIVENESS ABRACADABRAS
ABRASIVENESS ABRIDGEMENTS ABRUPTNESSES ABSCONDENCES ABSENTEEISMS ABSENTMINDED ABSINTHIATED ABSOLUTENESS ABSOLUTISING ABSOLUTISTIC ABSOLUTIZING ABSORBANCIES 
ABSORBENCIES ABSORPTANCES ABSORPTIVITY ABSQUATULATE ABSTEMIOUSLY ABSTINENCIES ABSTRACTABLE ABSTRACTEDLY ABSTRACTIONS ABSTRACTIVES ABSTRACTNESS ABSTRICTIONS 
ABSTRUSENESS ABSTRUSITIES ABSURDNESSES ACADEMICALLY ACADEMICIANS ACADEMICISMS ACANTHACEOUS ACARIDOMATIA ACARODOMATIA ACAROLOGISTS ACAROPHILIES ACATALECTICS 
ACATALEPSIES ACATALEPTICS ACCELERANDOS ACCELERATING ACCELERATION ACCELERATIVE ACCELERATORS ACCELERATORY ACCENTUALITY ACCENTUATING ACCENTUATION ACCEPTANCIES
ACCEPTATIONS ACCESSIONING ACCESSORISED ACCESSORISES ACCESSORIZED ACCESSORIZES ACCIACCATURA ACCIACCATURE ACCIDENTALLY ACCIPITRINES ACCLAMATIONS ACCLIMATABLE
ACCLIMATIONS ACCLIMATISED ACCLIMATISER ACCLIMATISES ACCLIMATIZED ACCLIMATIZER ACCLIMATIZES ACCOMMODABLE ACCOMMODATED ACCOMMODATES ACCOMMODATOR ACCOMPANIERS 
ACCOMPANISTS ACCOMPANYING ACCOMPANYIST ACCOMPLISHED ACCOMPLISHER ACCOMPLISHES ACCORDANCIES ACCORDIONIST ACCOUCHEMENT ACCOUCHEUSES ACCOUPLEMENT ACCOUTERMENT
ACCOUTREMENT ACCREDITABLE ACCRESCENCES ACCRETIONARY ACCULTURATED ACCULTURATES ACCUMBENCIES ACCUMULATING ACCUMULATION ACCUMULATIVE ACCUMULATORS ACCURATENESS
ACCURSEDNESS ACCUSATIVELY ACCUSATORIAL ACCUSTREMENT ACETALDEHYDE ACETANILIDES ACETONAEMIAS ACETONITRILE ACETYLATIONS ACHAENOCARPS ACHIEVEMENTS ACHLAMYDEOUS 
ACHLORHYDRIA ACHLORHYDRIC ACHROMATISED ACHROMATISES ACHROMATISMS ACHROMATIZED ACHROMATIZES ACIDANTHERAS ACIDIMETRIES ACIDOPHILOUS ACIDULATIONS ACKNOWLEDGED 
ACKNOWLEDGER ACKNOWLEDGES ACOLOUTHITES ACOLOUTHOSES ACOUSTICALLY ACOUSTICIANS ACQUAINTANCE ACQUIESCENCE ACQUIESCENTS ACQUIREMENTS ACQUISITIONS ACQUITTANCED 
ACQUITTANCES ACRIFLAVINES ACROAMATICAL ACROCENTRICS ACROCYANOSES ACROCYANOSIS ACROGENOUSLY ACROMEGALICS ACROMEGALIES ACRONYCHALLY ACRONYMANIAS ACROPHONETIC 
ACROSTICALLY ACTABILITIES ACTINOMETERS ACTINOMETRIC ACTINOMORPHY ACTINOMYCETE ACTINOMYCINS ACTIVENESSES ACUMINATIONS ACUPRESSURES ACUPUNCTURAL ACUPUNCTURES 
ADAPTABILITY ADAPTATIONAL ADAPTIVENESS ADAPTIVITIES ADDICTEDNESS ADDITIONALLY ADDITIVITIES ADENECTOMIES ADENOPATHIES ADENOVIRUSES ADEQUATENESS ADHESIVENESS 
ADIAPHORISMS ADIAPHORISTS ADJECTIVALLY ADJOURNMENTS ADJUDGEMENTS ADJUDICATING ADJUDICATION ADJUDICATIVE ADJUDICATORS ADJUDICATORY ADJUNCTIVELY ADJUSTMENTAL
ADMINICULATE ADMINISTERED ADMINISTRANT ADMINISTRATE ADMIRABILITY ADMIRALSHIPS ADMONISHMENT ADMONITORILY ADOLESCENCES ADOLESCENTLY ADOPTABILITY ADOPTIANISMS
ADOPTIANISTS ADOPTIONISMS ADOPTIONISTS ADORABLENESS ADRENOCHROME ADROITNESSES ADSCITITIOUS ADSCRIPTIONS ADULARESCENT ADULTERATING ADULTERATION ADULTERATORS
ADULTERESSES ADULTERISING ADULTERIZING ADULTEROUSLY ADULTESCENTS ADUMBRATIONS ADVANCEMENTS ADVANTAGEOUS ADVENTITIOUS ADVENTUREFUL ADVENTURISMS ADVENTURISTS 
ADVERBIALISE ADVERBIALIZE ADVERSATIVES ADVERTENCIES ADVERTISINGS ADVERTORIALS ADVISABILITY ADVISERSHIPS AECIDIOSPORE AECIDOSPORES AEOLOTROPIES AERIFICATION 
AEROBICISING AEROBICIZING AEROBRAKINGS AERODONETICS AERODYNAMICS AEROEMBOLISM AEROGRAPHIES AEROMAGNETIC AEROMECHANIC AEROMEDICINE AERONAUTICAL AERONEUROSES 
AERONEUROSIS AEROPLANKTON AEROSIDERITE AEROSOLISING AEROSOLIZING AEROSTATICAL AEROSTATIONS AEROTROPISMS AESTHESIOGEN AESTHETICIAN AESTHETICISE AESTHETICISM 
AESTHETICIST AESTHETICIZE AESTIVATIONS AETHEREALITY AETHRIOSCOPE AETIOLOGICAL AETIOLOGISTS AFFABILITIES AFFECTATIONS AFFECTEDNESS AFFECTIONATE AFFECTIONING 
AFFICIONADOS AFFILIATIONS AFFIRMATIONS AFFIRMATIVES AFFLICTIVELY AFFLUENTIALS AFFLUENTNESS AFFORCEMENTS AFFORESTABLE AFFRANCHISED AFFRANCHISES AFFRICATIONS 
AFFRICATIVES AFFRIGHTEDLY AFFRIGHTENED AFFRIGHTMENT AFFRONTINGLY AFORETHOUGHT AFTERBURNERS AFTERBURNING AFTEREFFECTS AFTERGRASSES AFTERGROWTHS AFTERMARKETS
AFTERSUPPERS AFTERTHOUGHT AGALMATOLITE AGAMOGENESES AGAMOGENESIS AGAMOGENETIC AGAPANTHUSES AGARICACEOUS AGATHODAIMON AGENTIVITIES AGGLOMERATED AGGLOMERATES 
AGGLUTINABLE AGGLUTINANTS AGGLUTINATED AGGLUTINATES AGGLUTINOGEN AGGRADATIONS AGGRANDISERS AGGRANDISING AGGRANDIZERS AGGRANDIZING AGGRAVATIONS AGGREGATIONS
AGGRESSIVELY AGGRESSIVITY AGGRIEVEMENT AGNOIOLOGIES AGNOSTICISMS AGORAPHOBIAS AGORAPHOBICS AGRANULOCYTE AGRARIANISMS AGREEABILITY AGRIBUSINESS AGRICHEMICAL 
AGRICULTURAL AGRICULTURES AGRIPRODUCTS AGRITOURISMS AGRITOURISTS AGROBUSINESS AGROCHEMICAL AGROFORESTER AGROFORESTRY AGROINDUSTRY AGROSTEMMATA AGROTOURISMS
AGROTOURISTS AGUARDIENTES AICHMOPHOBIA AIGUILLETTES AILOUROPHILE AILOUROPHOBE AILUROPHILES AILUROPHILIA AILUROPHILIC AILUROPHOBES AILUROPHOBIA AILUROPHOBIC 
AIRCRAFTSMAN AIRCRAFTSMEN AIRFREIGHTED AIRTIGHTNESS AIRWORTHIEST AKOLOUTHOSES ALBUMBLATTER ALBUMENISING ALBUMENIZING ALBUMINISING ALBUMINIZING ALBUMINURIAS
ALCHEMICALLY
'''.split()
        guessed_letters = []
        if n != "":
            print('\n' * 18)
            print("You have", n, "seconds!" + '\n' * 18)
            time.sleep(0.75)
        begin = time.time()


        def get_word():
            the_word = random.choice(word_list)
            return the_word


        word = get_word()
        word = word.upper()
        blanks = '-' * len(word)
        wrong = -1
        right = []


        def get_guess():
            print()
            if n != "":
                print("Seconds Left:", n - (int(time.time() - begin)))
            print()
            print()
            guess = input("Guess A Letter Or geuss a dash aka -or ': " + '\n' * 18)
            guess = guess.upper()
            print()
            if guess in guessed_letters:
                print("" + guess + " Has Already Been Chosen, Try Again")
                print(hanger[wrong + 1])
                get_guess()
            elif len(guess) != 1:
                print("Pick One Letter At A Time")
                print(hanger[wrong + 1])
                get_guess()
            elif guess not in 'ABCDEFGHIJKLMNOPQRSTUVWXYZ-''':
                print("Only Pick Letters")
                print(hanger[wrong + 1])
                get_guess()
            else:
                guessed_letters.append(guess)
            return guess


        running = True
        while running == True:
            if n != "":
                if (n - (int(time.time() - begin))) < 0:
                    running = False
                    print(hanger[wrong + 1])
                    print("Time's up!")
                    print("The word was: ", word)
                    print('\n' * 18)
                    time.sleep(1)
                    loop = 0
                    break
            right = []
            for i in range(len(word)):
                if word[i] in guessed_letters:
                    blanks = blanks[:i] + word[i] + blanks[i + 1:]
                    right.append(i)

            if wrong < 5:
                print('\n' * 18)
                print(hanger[wrong + 1])
            else:
                print('\n' * 18)
                print(hanger[wrong + 1])
                print("Oops! The word was: ", word)
                print("But you did well")
                print("And better luck next time.")
                print()
                print()
                print()
                running = False
                loop = 0
                break

            if len(right) == len(word):
                print('\n' * 18)
                print()
                print()
                print("\t\t", word)
                print(hanger[7])
                time.sleep(2)
                loop = 0
                running = False
                break

            print()
            print()
            print("         " + blanks + "")
            print()
            print()
            print("         ", end=' ')

            for i in range(len(guessed_letters)):
                print("", end='')
                print(guessed_letters[i], end='')

            guess = get_guess()
            if not guess in word:
                wrong = wrong + 1
        if running == False:
            response = input("Continue? (Y/N):" + '\n' * 18)
            print('\n' * 18)
            if response in ["N", "n", "no", "NO", "No", "nO"]:
                print('\n' * 18)
                print("Goodbye!")
                print('\n' * 18)
                time.sleep(1)
                loop = 2
            else:
                break
if loop == 2:
    exit()
