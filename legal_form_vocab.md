# Introduction

The **Legal Form Vocabulary** vocabulary defined in
[RDFS](http://en.wikipedia.org/wiki/RDF_Schema)
allows to describe legal forms under which individuals or organizations
carry on some kind of economic, charitable or in other ways beneficial
activity.
This includes but is not limited to forms of the private law such as the
[European SE](http://en.wikipedia.org/wiki/European_Company_Regulation)
or the
[German GmbH](http://en.wikipedia.org/wiki/Gesellschaft_mit_beschr%C3%A4nkter_Haftung);
But also cooperatives, associations or forms of the public law.
The status of a legal form is usually gained by some formal registration
within a jurisdiction but this is not always the case.

The vocabulary is available in the following serializations:

- [JSON-LD](legal_form_vocab.jsonld) (source)
- [RDF/XM](legal_form_vocab.rdf)
- [Turtle](legal_form_vocab.ttl)

# Status of this Document

This vocabulary has been developed by
[n-fuse GmbH](http://www.n-fuse.de) and is intended for public use.

We consider the overall status experimental but it may already be used
productively.

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
`https://w3id.org/legal_form#` and the preferred prefix is `lfov`.

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

The key class is `lfov:LegalForm` which represents a legal form.
The exact properties of a legal form are defined by the legislative authorities
within its corresponding jurisdiction.
This vocabulary defines properties to formally describe
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
        [lfov:legislation](legislation)
      </li>
    </ul>
  </dd>
</dl>

# Example

_This section is non-normative._

The following is an example of a (real) legal form described using
the Legal Form vocabulary (in JSON-LD):

    {
      "@type": "https://w3id.org/legal_form#LegalForm",
      "@id": "indivbiz",
      "name": {
        "de": "Einzelunternehmen",
        "en-US": "Sole Proprietorship",
        "en-GB": "Sole Trader"
      },
      "legislation": "http://sws.geonames.org/2921044/",
      "limitedLiability": false
    }


# Relationship with the Registered Organization Vocabulary

_This section is non-normative._

Individuals of the class `lfov:LegalForm` are intended to be objects of
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

The Legal Form class is central to the vocabulary; It represents a legal form.

## Properties

### name

<table>
  <thead>
    <tr>
      <th>Property</th>
      <th>Domain</th>
      <th>Range</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <code>
          lfov:name<br>
          rdfs:subPropertyOf<br>
          skos:prefLabel
        </code>
      </td>
      <td>
        <code>lfov:LegalForm</code>
      </td>
      <td>
        <code>rdf:langString</code>
      </td>
    </tr>
  </tbody>
</table>

The name defined by law.

### acronym

<table>
  <thead>
    <tr>
      <th>Property</th>
      <th>Domain</th>
      <th>Range</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <code>
          lfov:acronym<br>
          rdfs:subPropertyOf<br>
          skos:altLabel
        </code>
      </td>
      <td>
        <code>lfov:LegalForm</code>
      </td>
      <td>
        <code>rdf:langString</code>
      </td>
    </tr>
  </tbody>
</table>

The acronym defined by law.

### legislation

<table>
  <thead>
    <tr>
      <th>Property</th>
      <th>Domain</th>
      <th>Range</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <code>
          lfov:legislation
        </code>
      </td>
      <td>
        <code>lfov:LegalForm</code>
      </td>
      <td>
        <code></code>
      </td>
    </tr>
  </tbody>
</table>

Legislation (e. g. a country or a union thereof), in which this legal
form is defined.

### limitedLiability

<table>
  <thead>
    <tr>
      <th>Property</th>
      <th>Domain</th>
      <th>Range</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <code>
          lfov:limitedLiability
        </code>
      </td>
      <td>
        <code>lfov:LegalForm</code>
      </td>
      <td>
        <code>xsd:boolean</code>
      </td>
    </tr>
  </tbody>
</table>

The owners or members of the legal entity are not personally liable for
the company's debts.

### shared

<table>
  <thead>
    <tr>
      <th>Property</th>
      <th>Domain</th>
      <th>Range</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <code>
          lfov:shared
        </code>
      </td>
      <td>
        <code>lfov:LegalForm</code>
      </td>
      <td>
        <code>xsd:boolean</code>
      </td>
    </tr>
  </tbody>
</table>

Defines whether the capital or the ownership itself is divided into shares.


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
