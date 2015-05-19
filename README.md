linked-vocabulary-api
=====================
[![Build Status](https://travis-ci.org/tetherless-world/linked-vocabulary-api.svg?branch=master)](https://travis-ci.org/tetherless-world/linked-vocabulary-api)

Linked Data API Specification for publishing SKOS vocabulary linked data on the web

## The API

| Description  | Endpoint Template |
| ------------- | ------------- |
| *get list of all terms from all vocabularies published by service* | ``GET /terms`` |
| *get vocabulary resource*  | ``GET /vocab/{vocab_id}``  |
| *get vocabulary term*  | ``GET /vocab/{vocab_id}/term/{term_id}``  |
| *get list of all terms in the specified vocabulary* | ``GET /vocab/{vocab_id}/terms`` |
| *get list of all top terms in the specified vocabulary* | `` GET /vocab/{vocab_id}/topTerms`` |
| *get list of all terms narrower than the specified term* | ``GET /vocab/{vocab_id}/term/{term_id}/narrower`` |
| *get list of all terms broader than the specified term* | ``GET /vocab/{vocab_id}/term/{term_id}/broader`` |
| *get list of all terms related to specified term* | ``GET /vocab/{vocab_id}/term/{term_id}/related`` |
| *get list of all terms narrower transitive than the specified term* | ``GET /vocab/{vocab_id}/term/{term_id}/narrowerTransitive`` |
| *get list of all terms broader transitive than the specified term* | ``GET /vocab/{vocab_id}/term/{term_id}/broaderTransitive`` |
| *get list of all terms in vocabulary with a label that contains the specified text* | ``GET /vocab/{vocab_id}/terms?anyLabelContains={text}`` |
| *get list of all terms that are a close match to the specified term and are in a vocabulary with the specified label* | ``GET /vocab/{vocab_id}/term/{term_id}/closeMatch?inScheme.prefLabel={name}`` |

### Property Filtering

The client may specify what properties to include in the response with the ``_properties`` query parameter.  Properties are referenced by name in a comma-delimited list.

**example**
``GET /terms?_properties=prefLabel,altLabel``

### List Pagination

Lists responses are paginated by default.  The client can use the ``_page`` and ``_pageSize`` query attributes to control pagination parameters.

**example**
``GET /terms?_page=2&_pageSize=25``
