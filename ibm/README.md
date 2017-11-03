# Papers
## Probabilistic ontology based activity recognition in smart homes using Markov Logic Network
- Activities of Daily Living(ADL) are preferred for activity modeling for the reason that these activities help in defining normal scenarios within the smart home
- Event: atomic and indivisible in nature: ‘lying on the bed’, ‘sitting on a chair’ etc.
- simple activity is characterized by an ordered sequence of events ‘preparing meal’ involves the sequence ‘switching on stove’, ‘take pan’ etc
- Composite activity: Sequential, interleaved and concurrent
- the occupant’s need and preferences may change over time, for example the occupant may take bath for 20 min during summer but he might prefer to take a bath only for 10 min during winter
- The proposed activity recognition framework presented in this paper effectively tackles activity granularity, contextual knowledge, activity diversity through ontology model, while activity dynamics, data uncertainty are addressed through probabilistic reasoning over the represented domain ontology.
- Based on the type of sensors utilized for monitoring the occupants, the activity recognition is named as vision based or sensor based [Add Paper link]
- Data driven and Knowledge driven approaches
- Data driven ap- proach utilizes probabilistic and statistical machine learning strate- gies for the analysis and modeling sensor data. Knowledge driven paradigms utilize knowledge engineering and management tech- niques for activity modeling using domain information and artifi- cial intelligence based reasoning techniques for inferences.

## Sensor-Based Activity Recognition
- comprehensive survey of current state of art in sensor-based activity
recognition
- 1) to choose and deploy appropriate sensors to objects and environments
in order to monitor and capture a user’s behavior along
with the state change of the environment; 2) to collect, store, and
process perceived information through data analysis techniques
and/or knowledge representation formalisms at appropriate levels
of abstraction; 3) to create computational activity models in
a way that allows software systems/agents to conduct reasoning
and manipulation; and 4) to select or develop reasoning algorithms
to infer activities from sensor data.
- This approach, which was later dubbed as the “dense sensing”
approach, performs activity recognition through the inference
of user–object interactions[48], [63]. The approach is particular
suitable to deal with activities that involve a number of objects
within an environment, or instrumental activities of daily living
(ADL) [46], [47].smart home-based assistive living, such as the EU’s
AAL program [49].
- Pantelopoulos and Bourbakis [59] present a survey on wearable
systems for monitoring and early diagnosis for the elderly.
- As
such, dense sensing-based activity monitoring has been widely
adopted in AAL, via the smart home paradigm [46], [47], [50],
[52]–[56], [81].
- Patterson et al. [78] performed fine-grained activity
recognition (i.e., not just recognizing that a person is cooking
but determining what they are cooking) by aggregating abstract
object usage. Hodges and Pollack [79] proposed to identify individuals
from their behavior based on their interaction with
the objects they use in performing daily activities. Buettner
et al. [80] recognize indoor daily activities by using an RFID
sensor network
- Data-driven activity modeling can be classified into two main
categories: generative and discriminative.
- Generative:
- HMM [Video Lecture on HMM](https://www.youtube.com/watch?v=9dp4whVQv5s)
- DBN dynamic Bayesian networks [Video Lecture on DBN] (https://www.youtube.com/watch?v=Qh2hFKHOwPU)
- Wilson and Atkeson use DBNs to simultaneously track persons
and model their activities from a variety of simple sensors
(motion detectors, pressure sensors, switches, etc.) [82]. DBNs
were also used in the iSTRETCH system, a haptic robotic device
to assist a person with stroke rehabilitation [160].
- Discriminative:
- decision tree outperform Nearest Neighbour but are brittle
- SVM
- Brdiczka
et al. [91] where a model of situations is learned automatically
from data by first learning roles of various entities using SVMs
and labeled training data, then using unsupervised clustering to
build ‘situations’ or relations between entities, which are then
labeled and further refined by end users.
- A Conditional Random Field (CRF) is a more flexible alternative to the HMM that addresses
such practical requirements. It is a discriminative and generative
probabilistic model that represents the dependence of a hidden
variable y on an observed variable x [154].
- CRFs are applied to the problem of activity
recognition in [155] where they are compared with HMMs, but
only in a simple simulated domain. Liao et al. use hierarchical
CRFs for modeling activities based on GPS data [156]. Hu
and Yang use skip-chain CRFs, an extension in which multiple
chains interact in a manner reminiscent of the CHMM, to model
concurrent and interleaving goals [135], a challenging problem
for activity recognition. Mahdaviani and Choudhury show how
semisupervised CRFs can be used to learn activity models from
wearable sensor data [157].
-Knowledge Driven
- knowledge-driven activity recognition is founded
upon the observations that most activities, in particular, routine
ADL and working, take place in a relatively specific circumstance
of time, location, and space.
- Mining based approach
- given a set of activities,
the approach seeks to discover from the text corpuses a set of
objects used for each activity and extract object usage information
to derive their associated usage probabilities.
- A mining-based approach consists of a sequence of distinct
tasks. First, it needs to identify activities of concern and relevant
sources that describe these activities. Second, it uses various
methods, predominantly information retrieval and analysis
techniques, to retrieve activity definitions from specific sources
and extract phrases that describe the objects used during the
performance of the activity. Then, algorithms, predominantly
probabilistic and statistic analysis methods such as cooccurrences
and association, are used to estimate the object-usage
probabilities. Finally, the mined object and usage information
are used to create activity models, such as an HMM, that can be
used further for activity recognition.
-Perkowitz
et al. [105] proposed the idea of mining the web for largescale
activity modeling. used to construct DBN models
through sequentialMonte Carlo approximation. 
- Wyatt et al. [106] followed Perkowitz’s approach by mining
the web to create DBN activity models. To cover the wide variety
of activity definition sources, they mined the web in a more discriminative
way in a wider scope. They did this by building a
specialized genre classifier trained and tested with a large number
of labeled web pages. To enhance model applicability, they
used the mined models as base activity models and, then, exploited
the Viterbi algorithm and maximum likelihood to learn
customized activity parameters from unsegmented, unlabeled
sensor data.
- Tapia et al. [107]
proposed to extract collections of synonymous words for the
functionally similar objects automatically from WordNet,
- Mining-based approaches are similar to data-driven approaches
in that they all adopt probabilistic or statistical activity
modeling and recognition. However, they are different from
each other in the way the parameters of the activity models
are decided. The mining-based approaches make use of publically
available data sources avoiding the “cold start” problem.”
Nevertheless, they areweak in dealingwith idiosyncrasies of activities.
On other hand, data-driven approaches have the strength
of generating personalized activity models, but they suffer from
issues such as “cold start” and model reusability for different
users.
- Logic-Based Approach
- the
first step is to carry out knowledge acquisition, which involves
eliciting knowledge from various knowledge sources such as
domain experts and activity manuals. The second step is to
use various knowledge modeling techniques and tools to build
reusable activity structures. This will be followed by a domain
formalization process in which all entities, events, and temporal
and spatial states pertaining to activities, along with axioms and
rules, are formally specified and represented using representation
formalism. This process, usually, generates the domain
theory. The following step will be the development of a reasoning
engine in terms of knowledge representation formalisms to support inference. 
In addition, a number of supportive system
components will be developed, which are responsible for aggregating
and transforming sensor data into logical terms and
formula.With all functional components in place, activity recognition
proceeds by passing the logical representation of sensor
data onto the reasoning engine. The engine performs logical
reasoning, e.g., deduction, abduction, or induction, against the
domain theory. The reasoning will extract a minimal set of covering
models of interpretation from the activity models based
on a set of observed actions, which could semantically explain
the observations.
- Kautz et al. [110] adopted first-order axioms to build a library
of hierarchical plans.
- Bouchard and
Giroux. [112] borrow the idea of plan recognition and apply it to
activity recognition.
- Logic-based approaches are totally different from data-driven
approaches in the way activities are modeled and the mechanisms
activities are recognized. They do not require preexisting
large-scale dataset, and activity modeling and recognition
are semantically clear and elegant in computational reasoning.
It is easy to incorporate domain knowledge and heuristics for
activity models and data fusion. The weakness of logical approaches
is their inability or inherent infeasibility to represent
fuzziness and uncertainty, even though there are recent works
trying to integrate fuzzy logics into the logical approaches. Another
drawback is that logical activity models are viewed as
one-size-fits-all, inflexible for adaption to different users’ activity
habits.
- Ontology based
- In the dense sensing-based activity recognition community,
ontologies have been utilized to construct reliable activity models.
Such models are able to match different object names with
a term in an ontology that is related to a particular activity. For
example, a mug sensor event could be substituted by a cup event
in the activity model “MakeTea” as mug and cup can both be
used for the “MakeTea” activity. This is particularly useful to
address model incompleteness and multiple representations
- Latfi et al. [123] propose an ontological
architecture of a telehealth-based smart home aiming at
high-level intelligent applications for elderly persons suffering
from loss of cognitive autonomy. Michael et al. [124] developed
an ontology-centered design approach to create a reliable and
scalable ambient middleware. Chen et al. [125] pioneered the
notion of semantic smart homes in an attempt to leverage the
full potential of semantic technologies in the entire lifecycle
of assistive living, i.e., from data modeling, content generation,
activity representation, processing techniques, and technologies
to assist with the provision and deployment
- Compared with data-driven and mining-based approaches,
ontology-based approaches offer several compelling features:
First, ontological ADL models can capture and encode rich domain
knowledge and heuristics in a machine understandable
and processable way. This enables knowledge-based intelligent
processing at a higher degree of automation. Second, DL-based
descriptive reasoning along a time line can support incremental
progressive activity recognition and assistance as an ADL
unfolds. The two levels of abstraction in activity modeling, concepts
and instances, also allow coarse-grained and fine-grained
activity assistance. Third, as the ADL profile of an inhabitant
is essentially a set of instances of ADL concepts, it provides an
easy and flexible way to capture a user’s activity preferences
and styles, thus, facilitating personalized ADL assistance. Finally,
the unified modeling, representation and reasoning for
ADL modeling, recognition, and assistance, makes it natural
and straightforward to support the integration and interoperability
between contextual information and ADL recognition.
This will support systematic coordinated system development
by making use of seamless integration and synergy of a wide
range of data and technologies.
- DISCUSSION ON ACTIVITY RECOGNITION
- Activity Recognition Approach Comparison
- Cook [132] created a single benchmark dataset that contains
11 separate sensor event datasets collected from seven physical
testbeds.
- Activity Sensing and Activity Recognition
- Liao et al. [156] use continuous
2-D GPS data as input to a CRF. One solution to adapt activity
models to sensor types is to include all available sensors in a
discriminative or generative model, and allow the model itself
to choose the most effective ones for any given situation. This
is known as sensor selection or active sensing [133].
- EMERGING TRENDS AND DIRECTIONS
- Complex Activity Recognition single user
- Wu et al. [134] proposed an algorithm using factorial
CRF (FCRF) to recognize multiple concurrent activities
- Hu and Yang [135]
proposed a two-level probabilistic and goal-correlation framework
that deals with both concurrent and interleaving goals
from observed activity sequences.
- Modayil et al. [136] introduced interleaved HMMs to model
both interactivity and intraactivity dynamics
- Gu et al. [87] proposed an emerging patternbased
approach to sequential, interleaved and concurrent activity
recognition.
- Complex Activity Recognition multiple user
- Lin and Fu [144]
proposed a layered model to learn multiple users’ activity preferences
- Wang et al. [145] used CHMMs to recognize multiuser
activities
- Singla et al. [146] proposed a single
HMM model for two residents.
- Hoey
and Grzes [147] present a multilevel DBN model
- Scalability
- Chen and Nugent [126] developed activity
ontologies
- Okeyo
et al. [167] extended this idea by developing learning algorithms
- Abnormal Activity Recognition


## A survey on wearable systems for monitoring and early diagnosis for the elderly [59]
survey-health-sensors

## Activity knowledge transfer in smart environments
knowledge-transfer-smart-homes

## Recognizing Daily Activities with RFID-Based Sensors
daily-rfid

## An ‘Object-Use Fingerprint’: The Use of Electronic Sensors for Human Identification
sensor-human-identification

## Fine-Grained Activity Recognition by Aggregating Abstract Object Usage
fine-grained-object
