---
layout: default
title: Biomedical knowledge representation and reasoning
date: 2017-12-03T17:54:59+00:00
author: Chongle Pan
parent: 2017 posts
grand_parent: Posts
---
## Artificial intelligence

Knowledge representation and reasoning is the basis of artificial intelligence (AI). For supervised classification problems, we can train a neural network to recognize cats in pictures. Here, the knowledge is represented in the neural network through training with many cat pictures and then the knowledge captured in the neural network can then be used for classification of new pictures (i.e. reasoning). Here, both the knowledge representation and the reasoning are basically black boxes to humans. The format of the knowledge representation determines the reasoning strategy. For example, the knowledge representation and reasoning are done differently using neural networks and decision trees, which impact their performances for different problems.

Another type of artificial intelligence is to make inferences based on direct knowledge and logic. For example, if an algorithm knows that a cat is a mammal and all mammals have vertebra, then it can infer that a cat has vertebra. More broadly, if an algorithm knows the symptoms of all diseases and it also knows the symptom of a particular patient, then it can make some inferences to diagnose the disease. Here, we particularly focus on this type of knowledge representation and reasoning.

## Knowledge representation formats

To design a format for knowledge representation, one has to balance the expressiveness of the format and the usefulness of it for reasoning (e.g. [neat vs scruffy](https://en.wikipedia.org/wiki/Neats_and_scruffies)). Knowledge representation is the means and reasoning is the ends. Below are a few major types of formats for knowledge representation.

### 1) First-order logic

[First-order logic](http://mathworld.wolfram.com/First-OrderLogic.html) is very formal and allows rigorous inferences and it has been used for theorem proving. First-order logic has been implemented in the [PROLOG](https://en.wikipedia.org/wiki/Prolog) programming language. But I think it lacks the expressiveness and flexibility needed for biomedical knowledge.

### 2) Semantic networks

Semantic networks represent knowledge in graphs using edges to represent relationships between different entities. Here is an example of [semantic networks from Wikipedia](https://en.wikipedia.org/wiki/Semantic_network).

![](https://upload.wikimedia.org/wikipedia/commons/thumb/6/67/Semantic_Net.svg/480px-Semantic_Net.svg.png) 

Semantic networks are typically represented as triples (i.e. subject–predicate–object). These triples basically define the edges in a semantic network. In the example, there is an edge represented by the triple of &#8220;cat (subject) is a (predicate) mammal (object)&#8221;. This format has been expanded to include a fourth element of named graph:  (subject) (predicate) (object) (graph name).

The advantages of using semantic networks to represent biomedical knowledge are that it has all the underlying technologies available to use. However, I think semantic network has two key disadvantages. First, consider the example about a particular cat called Furry: &#8220;Furry is a cat&#8221; and &#8220;a cat is a mammal&#8221;. Here, Furry is an instance of a class (Cat) and cat is a sub-class of another class (Mammal). In a semantic network, these are just laid out in a graph. Second, there is no encapsulation to simplify the graph. For example, we can say Furry is yellow and runs faster, but these relationships are all laid out with the other relationships. These issues makes semantic networks too complex and unstructured.

A related format is called conceptual graphs. Its main difference from semantic networks is that conceptual graphs represents the predicate as a node, instead of an edge. This allows representation of predicate involves more than two entities beyond subject and object. For example: John goes to Boston on a bus. This would be cumbersome to be captured in semantic networks using triples.

<img class="alignnone size-medium" src="http://rhizomik.net/html/~roberto/thesis/figures/ConceptualGraph.png" width="439" height="171" /> 

### 3) Frames / Object-oriented

The concept of [frames](https://en.wikipedia.org/wiki/Frame_(artificial_intelligence)) for knowledge representation was introduced in the [Minsky 1974](https://dspace.mit.edu/handle/1721.1/6089) paper.

In simple terms, frames to knowledge representation is basically equivalent to objects to object-oriented programming (See also [frame languages](https://en.wikipedia.org/wiki/Frame_language)).

<table style="height: 100px; width: 683px;">
  <tr>
    <td style="width: 135.383px;">
      Frame-based  representation
    </td>
    
    <td style="width: 123.617px;">
      Frames
    </td>
    
    <td style="width: 130px;">
      Slots
    </td>
    
    <td style="width: 130px;">
      Triggers
    </td>
    
    <td style="width: 130px;">
      Methods
    </td>
  </tr>
  
  <tr>
    <td style="width: 135.383px;">
      Object-oriented programming
    </td>
    
    <td style="width: 123.617px;">
      Classes / Instances
    </td>
    
    <td style="width: 130px;">
      Class variables
    </td>
    
    <td style="width: 130px;">
      Mutators and accessors
    </td>
    
    <td style="width: 130px;">
      Class functions
    </td>
  </tr>
</table>

It has a few significant advantage for biomedical knowledge presentation:

  1. Instantiation. It clearly differentiates between a class (enzyme) and an instance (alcohol dehydrogenase). In semantic networks, these two entities are linked by a predicate or an edge called &#8220;is a&#8221;, but it&#8217;s cumbersome to create thousands of instances of the class enzyme. This can be done in a straightfoward object-oriented manner.
  2. Inheritance. We can derive a new more specialized class to a more general class, for example, to derive the class of alcohol dehybrogenase from the class of dehydrogenase. This can be done with a &#8220;is a type of&#8221; predicate in semantic network, but again it&#8217;s convoluted with other relationships.
  3. Encapsulation. For example, all the information about an instance can be stored in one frame. For example, we can store the name, the Vmas, the substrate of an alcohol dehybrogenase together, instead of having many edges out of this instance to represent its properties.
  4. Nested representation. We can represent a frame inside a frame as containment in object-oriented programming.
  5. Representation of procedural knowledge. So far, we have been focused on declarative knowledge (what it is), but there are also procedural knowledge (how it is done). The methods in a frame can be used to represent procedural knowledge.

## Serialization of a frame-based knowledge graph

Unlike Prolog for first-order logic or RDF triples for semantic networks, none of the languages developed for frames (e.g. KL-ONE or KEE) is under active development or usage. However, frame-based knowledge representation is essentially object-oriented programming and data structure. We can implement the former using the technologies developed for latter.

I think frames can be [serialized](https://en.wikipedia.org/wiki/Serialization) as [JSONs](https://en.wikipedia.org/wiki/JSON)

<table style="height: 73px; width: 590.233px;">
  <tr>
    <td style="width: 117px;">
      Class
    </td>
    
    <td style="width: 117px;">
      Instances
    </td>
    
    <td style="width: 179px;">
      Member variables
    </td>
    
    <td style="width: 149.233px;">
      Member functions
    </td>
  </tr>
  
  <tr>
    <td style="width: 117px;">
      Schema
    </td>
    
    <td style="width: 117px;">
      JSON files
    </td>
    
    <td style="width: 179px;">
      Attribute–value pairs
    </td>
    
    <td style="width: 149.233px;">
      N/A
    </td>
  </tr>
</table>

More specifically, we can use [JSON Linked Data](https://en.wikipedia.org/wiki/JSON-LD) ([JSON-DL](http://www.linkeddatatools.com/introduction-json-ld)), which is also explained [here](http://www.seoskeptic.com/what-is-json-ld/) and [here](http://www.linkeddatatools.com/introduction-json-ld).

If the schema of JSON determines the structure of a class, The context in JSON-DL provides a namespace and the reference to an ontology system for the class.

It&#8217;s important to note that RDF is an abstract data model and JSON-DL is basically a new RDF serialisation, among other types of RDF serialisation including RDF/XML, Turtle, TriG, etc, (see some interesting discussion [here](http://manu.sporny.org/2014/json-ld-origins-2/)).

## Databases for a frame-based knowledge graph

After frames are serialized into JSONs, we would need a database to store and query these JSON files.

We need to have

  * Scalability. We need to think about designing for billions of small JSON files.
  * Efficient query. We need to be able to quickly traverse the cross-references among the JSON files when we explore the knowledge graph. We need to be able to efficiently select and filter JSON files based on multiple attributes.

We probably don&#8217;t need to have

  * modification of the data. We will primarily construct and modify our knowledge graph in the JSON files. We will then import JSON files in bulk into the database. So, we don&#8217;t need a strong capability for the database to support data manipulation.

Below are a few options for the database:

### Object-oriented databases.

Since we are basically manipulating frames as objects, it could fit the paradigm of object-oriented databases. But in practice, I don&#8217;t know of any widely used object-oriented database because of multiple issues.

### Graph databases

We will have a lot of relationships between different objects, which could be represented in graph databases (objects as nodes and references among them as edges). Neo4j could be used here.

### Document-oriented databases

These databases, such as MongoDB, are typically designed to store a large number of JSON files. Although they are flexible (don&#8217;t even require schema), they don&#8217;t allow efficient query (no free lunch), includes [these issues](http://www.sarahmei.com/blog/2013/11/11/why-you-should-never-use-mongodb/).

### Relational databases

It will take a significant amount of work to normalize our JSON data for relational databases. And relational databases can&#8217;t be scaled out as those NoSQL databases do.  However, Postgress has added native support for JSON, which may ease the normalization process and allow efficient query, as discussed [here](https://www.sisense.com/blog/postgres-vs-mongodb-for-storing-json-data/) and [here](https://blog.codeship.com/unleash-the-power-of-storing-json-in-postgres/) and [here](http://engineering.hipolabs.com/graphdb-to-postgresql/).

&nbsp;