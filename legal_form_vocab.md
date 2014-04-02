# Introduction

The **Legal Form Vocabulary** allows to describe legal forms such as the
[European SE](http://en.wikipedia.org/wiki/European_Company_Regulation)
or the
[German GmbH](http://en.wikipedia.org/wiki/Gesellschaft_mit_beschr%C3%A4nkter_Haftung)
whose status can be attained by a formal registration within a legislation and
make the registree a legal entity.

# Status of this Document

This vocabulary has been developed by
[n-fuse GmbH](http://www.n-fuse.de).

The vocabulary defined in this document is also available as RDF serialization
in these formats: [`RDF/XML`](legal_form_vocab.rdf) and
[`Turtle`](legal_form_vocab.ttl).

**How to contribute**

* Express legal forms in the terms of LFOV
* Map other ontologies to LFOV
* [Comment](https://github.com/n-fuse/legal-form-vocab/issues) on the
  specification
* [Change](https://github.com/n-fuse/legal-form-vocab/master/legal_form.md)
  the current draft

**Revision history**

{GIT_CHANGES}

# Namespaces

_This section is non-normative._

The namespace of the Legal Form vocabulary is
`https://github.com/n-fuse/legal-form-vocab#` and the preferred prefix is `lfov`.

A full set of namespaces and prefixes used in this document is shown in the
table below.

<table id="namespaces">
  <thead>
    <tr>
      <th>Prefix</th>
      <th>Namespace</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>rov</td>
      <td>http://www.w3.org/ns/regorg#</td>
    </tr>
    <tr>
      <td>org</td>
      <td>http://www.w3.org/ns/org#</td>
    </tr>
    <tr>
      <td>skos</td>
      <td>http://www.w3.org/2004/02/skos/core#</td>
    </tr>
    <tr>
      <td>xsd</td>
      <td>http://www.w3.org/2001/XMLSchema#</td>
    </tr>
  </tbody>
</table>


# Overview of the Vocabulary

_This section is non-normative._

The key class is `lfov:LegalForm` which represents a legal form whose status
can be attained by a formal registration process. The result of a successful
registration process is a legal entity taking such a legal form.
The properties of a legal form are defined by the legislative authorities
within its corresponding jurisdiction.
The vocabulary defines properties to formally describe
general aspects of a legal form – e.&nbsp;g. whether it is a commercial
or non-commercial one.

This vocabulary makes use of classes and properties from several
other vocabularies. Essential are the `org:classification` from
[The Organization Ontology](http://www.w3.org/TR/2014/REC-vocab-org-20140116/)
and the `skos:Concept` from the
[Simple Knowledge Organization System (SKOS)](http://www.w3.org/2009/08/skos-reference/skos.html).

## Vocabulary Index

<dl>
  <dt>Classes:</dt>
  <dd>
    <ul>
      <li>
        [lfov:LegalForm](LegalForm)
      </li>
    </ul>
  </dd>

  <dt>Properties:</dt>
  <dd>
    <ul>
      <li>
        [lfov:name](name)
      </li>
      <li>
        [lfov:acronym](acronym)
      </li>
      <li>
        [lfov:registrableIn](registrableIn)
      </li>
    </ul>
  </dd>
</dl>

# Example

_This section is non-normative._

The following is an example of a (real) legal form described using
the Legal Form vocabulary (in RDF/Turtle):



# Relationship with the Registered Organization Vocabulary

_This section is non-normative._

Individuals of the class `lfov:LegalForm` are intended to be values of
the `rov:orgType` property. Therefore, it is typed as `rdfs:Class`
and `skos:Concept`.

# Vocabulary Definitions

The classes and properties are described in the following sub-sections.

## The Legal Form Class

<table>
  <thead>
    <tr>
      <th>Class</th>
      <th>Notes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td class="code">lfov:LegalForm</td>
      <td>
        Type
        <code>rdfs:Class</code> and
        <code>skos:Concept</code>
      </td>
    </tr>
  </tbody>
</table>

The Legal Form class is central to the vocabulary. It represents a legal form
whose status can be attained by a formal registration within a legislation and
make the registree a legal entity. Such legal forms may range from
a sole trader (which must be registered in some jurisdictions) or a publicly
traded company.

## Properties


### TEST

sdfsdf

    "gn": "http://www.geonames.org/ontology#",

# Conformance

As well as sections marked as non-normative, all authoring guidelines,
diagrams, examples, and notes in this specification are non-normative.
Everything else in this specification is normative.

The key words
<em title="must" class="rfc2119">must</em>,
<em title="must not" class="rfc2119">must not</em>,
<em title="required" class="rfc2119">required</em>,
<em title="should" class="rfc2119">should</em>,
<em title="should not" class="rfc2119">should not</em>,
<em title="recommended" class="rfc2119">recommended</em>,
<em title="may" class="rfc2119">may</em>, and
<em title="optional" class="rfc2119">optional</em>
in this specification are to be interpreted as described in
[RFC2119](http://www.ietf.org/rfc/rfc2119.txt).

A data interchange, however that interchange occurs, is conformant with the
Legal Form vocabulary if:

- it uses the terms (classes and properties) in a way consistent with their
  semantics as declared in this specification;
- it does not use terms from other vocabularies instead of ones defined in this
  vocabulary that could reasonably be used.

A conforming data interchange:

- <em class="rfc2119">may</em> include terms from other vocabularies;
- <em class="rfc2119">may</em> use only a subset of Legal Form vocabulary
  terms.

A Legal Form application profile is a specification for data
interchange that adds additional constraints. Such additional
constraints in a profile may include:

- a minimum set of required terms;
- classes and properties for additional terms not covered in the Legal Form vocabulary;
- controlled vocabularies or URI sets as acceptable values for properties;

The Legal Form vocabulary is technology-neutral and a publisher may use
any of the terms defined in this document encoded in any technology
although RDF and XML are preferred.
