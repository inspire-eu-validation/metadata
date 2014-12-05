# Raw notes from the MD & NS validation workshop

The following notes for metadata TG requirements were taken down during the workshop in Ispra 2nd & 3rd Dec 2014.

## TG Requirements 1 & 2

Check that the hierarchyLevel element is there. Combine Req 1 with TG Req 2.
Value must be one of the options in Req 2.

Note to the TG development: add a new explicit requirement for using the XML encoding defined in ISO 19139

## TG Requirements 3 & 4

Maybe combine Req 3 & 4 (data & service).
Check if the values of all the Resource Locators structure are a valid URLs.
Each URL must resolve to return a document: return "ok" and length > 0, do not try to parse the returned document
Authentication/authorization/redirection?
Break down into two tests: parse the URL (validity) and resolve it, but require both to pass

## TG Requirements 5 & 6

Combine Reqs 5 & 6.

Two options:

* if the type if MD_identifier it must have the code.
* if the type is RS_Identifier it must have the code. If the codeSpace is also given, it must not be empty.

Requirement wording feedback to TG?

## TG Requirement 7

Test only applied to services.

If it operatesOn element is there check that

* the href attribute is there,
* the URL is resolvable,
* the returned (resolved) fragment should(must?) resolve to the MD_Metadata element

Thijs: Maybe this is more easily tested from the service side?

This test should be part of the NS interoperability tests.

## TG Requirements 16 & 17

Not possible to automatically check if the given keywords originate from a Controlled Vocabulary.
However, it's a reasonable requirement for the data providers to check that they include a
valid reference to the thesaurus or ontology if the keyword they use originates from such a
vocabulary.

Maybe a manual tests?
