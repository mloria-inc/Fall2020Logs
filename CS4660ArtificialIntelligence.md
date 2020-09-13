# **AI Notes**


```Markdown
Format

### **Date**

##### **Time**

##### Note Subject
    * notes
        * more notes
            * even more notes
```

---

### **Date Month Year**

##### ***Time***

##### **Note Subject/Focus**

* notes
  * more notes
    * even more notes

---

### **13 August 2020**

##### ***1:27pm***

##### **Getting Ready for Fall2020**

* Professor : Stephanie August
* [Syllabus] : https://calstatela.instructure.com/courses/52369/pages/complete-course-syllabus-8-slash-21-slash-2020?module_item_id=2272570
* Textbook : No required text

### **12 September 2020**

##### ***8:00pm***

##### **Being a Fucking Procrastinator about School atm**

* Chapters
  * Artificial Intelligence and Agents
  * Agent Architectures and Hierarchical Control
  * Searching For Solutions
  * Reasoning with Constraints
  * Propositions and Inference
  * Planning with Certainty
  * Supervised Machine Learning
  * Reasoning with Uncertainty
  * Planning with Uncertainty
  * Learning with Uncertainty
  * Multiagent Systems
  * Learning to Act
  * Individuals and Relations
  * Ontologies Planning, Learning, and Probabilistic Reasoning
  * Retrospect and Prospect

* Preface
  * AI is the study of the design of intelligent computational agents
  * ai has a coherent formal theory 
  * everything should be made as simple as possible but not simpler
  * probabilistic and logical reasoning are complementary

![](ai.jpg)

  * figure 1 shows the topics covered in the book. the solid lines depict prerequisites. Often the prerequisite structure does not include all sub topics.

##### Chapter 1: Artificial Intelligence and Agents
* What is Artificial Intelligence
  * artificial intelligence or ai is the field that studies the synthesis and analysis of computational agents that act intelligently
  * an agent is something that acts in an environment; it does something. Agents include worms, dogs, thermostats, airplanes, robots, humans, companies, and countries
  * we are interested in what an agent does; that is how it acts. We judge an agent by its actions
  * an agent acts intelligently when
    * what it does is appropriate for its circumstances and its goals, taking into account the short term and long term consequences of its actions
    * it is flexible to changing environments and changing goals
    * it learns from experience 
    * it makes appropriate choices given its perceprual and computational limitations
  * a computational agent is an agent whose decisions about its actions can be explained in terms of computation
  * it is an open question whether all intelligent agents are computational
  * all agents are limited
  * agents can only observe everything about the world in very specialized domains where "the world" is very constrained
  * agents have finite memory 
  * agents in the real world do not have unlimited time to act
  * central goal is to understand the principles that make intelligent behavior possible in natural or artificial systems. this is done by
    * the analysis of natural and artificial agents
    * formulating and testing hypotheses about what it takes to construct intelligent agents 
    * designing, building, and experimenting with computational systems that perform tasks commonly viewed as requiring intelligence
* Artificial and Natural Intelligence
  * turing test consists of an imitation game where an interrogator can ask a witness, via a text interface, any question. If the interrogator cannot distinguish the witness from the human, the witness must be intelligent.
  * winograd schemas have the property that (a) humans can easily disambiguate them and (b) there is no simple grammatical or statistical test that could disambiguate them
  * reacquire that ability to do commonsense reasoning
  * it is instructive to consider where human intelligence comes from
    * biology
      * humans have evolved into adaptable animals that can survive in various habitats
    * culture
      * culture provides not only language, but also useful tools, useful concepts, and the wisdom that is passed from parents and teachers to children
    * lifelong learning
      * humans learn throughout their life and accumulate knowledge and skills
  * most interesting and useful intelligent agents learn to improve their behavior
* A Brief History of Artificial Intelligence
  * symbolic reasoning evolution
  * any effectively computable function can be carried out on a turing machine (and so also in the lambda calculus or any of the other equivalent formalisms)
  * in addition to work on high level symbolic reasoning, there was also much work on low level learning inspired by how neurons work
* Relationship to Other Disciplines 
  * synthetic psychology, experimental philosophy, or computational epistemology.
  * ai can be seen as a way to study the nature of knowledge and intelligence but with a more powerful experimental tool than was previously available
  * modern computers provide a way to construct the models about which philosophers have only been able to theorize
  * ai researchers can experiment with these models as opposed to just discussing their abstract properties
  * ai researchers are interested in testing general hypotheses about the nature of intelligence by building machines that are intelligent and that do not necessarily mimic humans or organizations
* Agents Situated in Environments
  * a coupling of perception, reasoning, and acting comprises an agent
  * robot; physical setting
  * expert system
  * software agent; purely computational

![](agent.jpg)

  * agents in terms of its inputs and outputs
  * what an agent does depends on: 
    * prior knowledge about the agent and the environment
    * history of interaction with the environment, which is composed of 
      * stimuli received from the current environment, which can include observations about the environment, as well as actions that the environment imposes on the agent and 
      * past experiences of previous actions and stimuli, or other data, from which can learn
    * goals that it must try to achieve or preferences over states of the world
    * abilities, the primitive actions the agent is capable of carrying out
  * an agent has some internal belief state that can encode beliefs about its environment, what it has learned, what it is trying to do, and what it intends to do. an agent updates this internal state based on stimuli. it used the belief state and stimuli to decide on its actions. much of this book is about what is inside this black box
  * if an agent does not have preferences, by definition it does not care what world state it ends up in, and so it does not matter to it what it does.
  * the reason to design an agent is to instill preferences in it - to make it prefer some world states and try to achieve them
  * an agent does not have to know its preferences explicitly
  * the preferences of an agent are often the preferences of the designer of the agent, but sometimes an agent can  acquire goals and preferences at run time
* Designing Agents
  * artificial agents are designed for particular tasks. researchers have not yet got to the stage of designing an agent for the task of surviving and reproducing in a natural environment
* Design Time, Offline and Online Computation
  * three aspects of computation that must be distinguished
    * the computation that goes into the design of the agent
    * the computation that the agent can do before it observes the world and needs to act
    * the computation that is done by the agent as it is acting
  * design time computation
    * the computation that is carried out to design the agent. it is carried out by the designer of the agent, not the agent itself
  * offline computation
    * the computation done by the agent before it has to act. it can include compilation and learning. offline an agent can take background knowledge and data and compile them into a usable form called knowledge base. background knowledge can be given either at design time or offline
  * online computation
    * is the computation done by the agent between observing the environment and acting in the environment. a piece of information obtained online is called an observation. an agent typically must use its knowledge base, its beliefs and its observations to determine what to do next
  * designing an agent that can adapt to complex environments and changing goals is a major challenge
  * the advantage of building agents for complex environments is that these are the types of environments in which humans live and where we want our agents to be
* Tasks
  * ai representation typically specifies what needs to be computed, not how it is to be computed.
  * much of ai reasoning involves searching through the space of possibilities to determine how to complete a task

![](tasks.jpg)

  * the general framework for solving tasks by a computer is given in figure 1.4. to solve a task, the designer of a system must:
    * determine what constitutes a solution
    * represent the task in a way a computer can reason about
    * use the computer to compute an output, which is answers presented to a user or actions to be carried out in the environment, and
    * interpret the output as a solution to the task
* Defining a Solution
  * 