# SensEval/Semeval participant systems
Output of all the systems participating in the previous SensEval/SemEval WSD task in XML format (also the gold keys)

#Introduction

In this repository you can find the output from the participants in the last SensEval/SemEval competitions in XML format (also the gold
keys are included). These tasks are included:

* SensEval-2 all words task
* SensEval-3 all words task
* SemEval2007 task 17 all words
* SemEval2010 task 12 specific domain all words WSD task
* SemEval2013 task 17 all words task

#The format

There is one xml file for each competition and one error file with participants that providing invalid tokens. The XML format
follows this structure:
```xml
<test_tokens corpus='Corpus identifier'>
  <token doc_id="document_id" token_id="token_id">
    <gold_keys>
      <key value="val1"/>
      <key value="val2"/>         
      ...
    </gold_keys>
    <systems>
      <system id="system identifier">
        <answer value="val1" confidence='value'/>
        <answer value="val2"/>
 	...
      </system>
      <system id="system identifier2">          
        <answer value="val1" confidence='value'/>
        <answer value="val2"/>              
      </system>
      ...
  </token>
</test_tokens>
```

So, there is one `token` element for every test token, with the document and token identifier. Then a subelement
`gold_keys` store all the valid keys for this token. In the subelement `systems` we will find all the answers provided
by the different systems. The confidence attribute is optional and it is not always included.

#TODO

* SemEval2013-task12: Add wikipedia and babelnet

#Contact#
* Ruben Izquierdo
* Vrije University of Amsterdam
* ruben.izquierdobevia@vu.nl  rubensanvi@gmail.com
* http://rubenizquierdobevia.com/