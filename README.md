# Individual Preferences Vocabulary

The `vocabulary.yml` document in this repo defines a vocabulary for expressing
an individual's preferences, including third-party-verified contact information
(email address, phone number, mailing address) and self-attested accessibility
preferences (font size, live captions, voice control, high contrast, color
filters, dark mode, and more).

The vocabulary defines two credential types:

- **`PreferencesCredential`** — a self-issued credential carrying self-asserted
  contact and accessibility preferences.
- **`VerifiedPreferencesCredential`** — a third-party-issued credential
  attesting verified contact information or accessibility preferences.

The `vocabulary.yml` document is intended to be used with the
[yml2vocab](https://github.com/w3c/yml2vocab?tab=readme-ov-file) tool from
the W3C.

## Usage

Run the following to generate the ontology description in HTML, JSON-LD,
and Turtle (`.ttl`).

```sh
npm run build
```

The output will result in...
* `dist/index.html` - the Ontology in HTML and usage documentation
* `dist/vocabulary.context.jsonld` - the latest JSON-LD context file
* `vocabulary.jsonld` - the Ontology in JSON-LD
* `vocabulary.ttl` - the Ontology in Turtle

The Ontology files can be used by modeling tools as needed. Additionally, the
JSON-LD context file can be used during testing.

## Releasing

Once the vocabulary/ontology and context file are ready for more permanence, the
following command can be used to create a release:

```sh
$ npm run release -- v1rc1
```

This will result in a `dist/contexts/v1rc1.jsonld` file.
