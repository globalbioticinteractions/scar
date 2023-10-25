[![GloBI Review by Elton](../../actions/workflows/review.yml/badge.svg)](../../actions/workflows/review.yml) [![GloBI](https://api.globalbioticinteractions.org/interaction.svg?accordingTo=globi:globalbioticinteractions/scar&refutes=true&refutes=false)](https://globalbioticinteractions.org/?accordingTo=globi:globalbioticinteractions/scar)

Configuration to help Global Biotic Interactions (GloBI, https://globalbioticinteractions.org) index: 

Scientific Committee on Antarctic Research. (2023). SCAR Southern Ocean Diet and Energetics Database (2023-04-04) [Data set]. Zenodo. https://doi.org/10.5281/zenodo.7796465 hash://md5/e41e29d8fb3c2d731f292ec08798cf6b hash://md5/05abf23c0b9e5f4bc721ff407455af0a hash://sha256/7a344b858ab8d1daeca1da49843e8bf957f1116ff9e10a29176ab5c02cb49bef 

## Provenance 

This dataset was packaged using [Preston](https://github.com/bio-guoda/preston) to help make the data citable and verifiable. 

The following commands were executed to generate this package: 

```bash
# capture the zip files available via Zenodo
preston track\
 --algo md5\
 https://zenodo.org/records/7796465/files/SCAR_Diet_Energetics.zip

# capture and run a program to extract the diet data from the zip file
cat extract-diet.sh\
 | preston bash --algo md5

# make an alias for the produced diet dataset
preston alias\
 --algo md5\
 'urn:example:scar_diet.csv'\
 hash://md5/e9039d2e531908e901901684f30adc9e

# put the content on the file system in a named file
preston cat\
 hash://md5/e9039d2e531908e901901684f30adc9e\
 > scar_diet.csv
```

The resulting data package produced the following results:

```
preston head\ 
 --algo md5
```

yields

```
hash://md5/e41e29d8fb3c2d731f292ec08798cf6b
```

```
preston history\
 --algo md5\
 --anchor hash://md5/e41e29d8fb3c2d731f292ec08798cf6b
```

yields

```
<hash://md5/e41e29d8fb3c2d731f292ec08798cf6b> <http://www.w3.org/ns/prov#wasDerivedFrom> <hash://md5/51f70adb9c91b2da122f9d4346771e30> .
<hash://md5/51f70adb9c91b2da122f9d4346771e30> <http://www.w3.org/ns/prov#wasDerivedFrom> <hash://md5/1650cbf81e07c4918d2448b332d3548a> .
<hash://md5/1650cbf81e07c4918d2448b332d3548a> <http://www.w3.org/ns/prov#wasDerivedFrom> <hash://md5/7679be7f82aa33e468683b87a45ad656> .
<urn:uuid:0659a54f-b713-4f86-a917-5be166a14110> <http://purl.org/pav/hasVersion> <hash://md5/7679be7f82aa33e468683b87a45ad656> .
```

```
preston ls\
 --algo md5\
 --anchor hash://md5/e41e29d8fb3c2d731f292ec08798cf6b
```

```
<https://preston.guoda.bio> <http://www.w3.org/1999/02/22-rdf-syntax-ns#type> <http://www.w3.org/ns/prov#SoftwareAgent> <urn:uuid:6b99bd1d-d2ca-4ba3-91a5-474f4e5da160> .
<https://preston.guoda.bio> <http://www.w3.org/1999/02/22-rdf-syntax-ns#type> <http://www.w3.org/ns/prov#Agent> <urn:uuid:6b99bd1d-d2ca-4ba3-91a5-474f4e5da160> .
<https://preston.guoda.bio> <http://purl.org/dc/terms/description> "Preston is a software program that finds, archives and provides access to biodiversity datasets."@en <urn:uuid:6b99bd1d-d2ca-4ba3-91a5-474f4e5da160> .
<urn:uuid:6b99bd1d-d2ca-4ba3-91a5-474f4e5da160> <http://www.w3.org/1999/02/22-rdf-syntax-ns#type> <http://www.w3.org/ns/prov#Activity> <urn:uuid:6b99bd1d-d2ca-4ba3-91a5-474f4e5da160> .
<urn:uuid:6b99bd1d-d2ca-4ba3-91a5-474f4e5da160> <http://purl.org/dc/terms/description> "An activity that assigns an alias to a content hash"@en <urn:uuid:6b99bd1d-d2ca-4ba3-91a5-474f4e5da160> .
<urn:uuid:6b99bd1d-d2ca-4ba3-91a5-474f4e5da160> <http://www.w3.org/ns/prov#startedAtTime> "2023-10-24T23:16:12.093Z"^^<http://www.w3.org/2001/XMLSchema#dateTime> <urn:uuid:6b99bd1d-d2ca-4ba3-91a5-474f4e5da160> .
<urn:uuid:6b99bd1d-d2ca-4ba3-91a5-474f4e5da160> <http://www.w3.org/ns/prov#wasStartedBy> <https://preston.guoda.bio> <urn:uuid:6b99bd1d-d2ca-4ba3-91a5-474f4e5da160> .
<https://doi.org/10.5281/zenodo.1410543> <http://www.w3.org/ns/prov#usedBy> <urn:uuid:6b99bd1d-d2ca-4ba3-91a5-474f4e5da160> <urn:uuid:6b99bd1d-d2ca-4ba3-91a5-474f4e5da160> .
<https://doi.org/10.5281/zenodo.1410543> <http://www.w3.org/1999/02/22-rdf-syntax-ns#type> <http://purl.org/dc/dcmitype/Software> <urn:uuid:6b99bd1d-d2ca-4ba3-91a5-474f4e5da160> .
<https://doi.org/10.5281/zenodo.1410543> <http://purl.org/dc/terms/bibliographicCitation> "Jorrit Poelen, Icaro Alzuru, & Michael Elliott. 2021. Preston: a biodiversity dataset tracker (Version 0.7.6-SNAPSHOT) [Software]. Zenodo. http://doi.org/10.5281/zenodo.1410543"@en <urn:uuid:6b99bd1d-d2ca-4ba3-91a5-474f4e5da160> .
<urn:uuid:0659a54f-b713-4f86-a917-5be166a14110> <http://www.w3.org/1999/02/22-rdf-syntax-ns#type> <http://www.w3.org/ns/prov#Entity> <urn:uuid:6b99bd1d-d2ca-4ba3-91a5-474f4e5da160> .
<urn:uuid:0659a54f-b713-4f86-a917-5be166a14110> <http://purl.org/dc/terms/description> "A biodiversity dataset graph archive."@en <urn:uuid:6b99bd1d-d2ca-4ba3-91a5-474f4e5da160> .
<hash://md5/51f70adb9c91b2da122f9d4346771e30> <http://www.w3.org/ns/prov#usedBy> <urn:uuid:6b99bd1d-d2ca-4ba3-91a5-474f4e5da160> <urn:uuid:6b99bd1d-d2ca-4ba3-91a5-474f4e5da160> .
<urn:example:scar_diet.csv> <http://purl.org/pav/hasVersion> <hash://md5/e9039d2e531908e901901684f30adc9e> <urn:uuid:6b99bd1d-d2ca-4ba3-91a5-474f4e5da160> .
<https://preston.guoda.bio> <http://www.w3.org/1999/02/22-rdf-syntax-ns#type> <http://www.w3.org/ns/prov#SoftwareAgent> <urn:uuid:6117d2bd-6250-4e87-af09-c315b258959f> .
<https://preston.guoda.bio> <http://www.w3.org/1999/02/22-rdf-syntax-ns#type> <http://www.w3.org/ns/prov#Agent> <urn:uuid:6117d2bd-6250-4e87-af09-c315b258959f> .
<https://preston.guoda.bio> <http://purl.org/dc/terms/description> "Preston is a software program that finds, archives and provides access to biodiversity datasets."@en <urn:uuid:6117d2bd-6250-4e87-af09-c315b258959f> .
<urn:uuid:6117d2bd-6250-4e87-af09-c315b258959f> <http://www.w3.org/1999/02/22-rdf-syntax-ns#type> <http://www.w3.org/ns/prov#Activity> <urn:uuid:6117d2bd-6250-4e87-af09-c315b258959f> .
<urn:uuid:6117d2bd-6250-4e87-af09-c315b258959f> <http://purl.org/dc/terms/description> "Executes script and captures stdout"@en <urn:uuid:6117d2bd-6250-4e87-af09-c315b258959f> .
<urn:uuid:6117d2bd-6250-4e87-af09-c315b258959f> <http://www.w3.org/ns/prov#startedAtTime> "2023-10-24T23:09:23.539Z"^^<http://www.w3.org/2001/XMLSchema#dateTime> <urn:uuid:6117d2bd-6250-4e87-af09-c315b258959f> .
<urn:uuid:6117d2bd-6250-4e87-af09-c315b258959f> <http://www.w3.org/ns/prov#wasStartedBy> <https://preston.guoda.bio> <urn:uuid:6117d2bd-6250-4e87-af09-c315b258959f> .
<https://doi.org/10.5281/zenodo.1410543> <http://www.w3.org/ns/prov#usedBy> <urn:uuid:6117d2bd-6250-4e87-af09-c315b258959f> <urn:uuid:6117d2bd-6250-4e87-af09-c315b258959f> .
<https://doi.org/10.5281/zenodo.1410543> <http://www.w3.org/1999/02/22-rdf-syntax-ns#type> <http://purl.org/dc/dcmitype/Software> <urn:uuid:6117d2bd-6250-4e87-af09-c315b258959f> .
<https://doi.org/10.5281/zenodo.1410543> <http://purl.org/dc/terms/bibliographicCitation> "Jorrit Poelen, Icaro Alzuru, & Michael Elliott. 2021. Preston: a biodiversity dataset tracker (Version 0.7.6-SNAPSHOT) [Software]. Zenodo. http://doi.org/10.5281/zenodo.1410543"@en <urn:uuid:6117d2bd-6250-4e87-af09-c315b258959f> .
<urn:uuid:0659a54f-b713-4f86-a917-5be166a14110> <http://www.w3.org/1999/02/22-rdf-syntax-ns#type> <http://www.w3.org/ns/prov#Entity> <urn:uuid:6117d2bd-6250-4e87-af09-c315b258959f> .
<urn:uuid:0659a54f-b713-4f86-a917-5be166a14110> <http://purl.org/dc/terms/description> "A biodiversity dataset graph archive."@en <urn:uuid:6117d2bd-6250-4e87-af09-c315b258959f> .
<hash://md5/1650cbf81e07c4918d2448b332d3548a> <http://www.w3.org/ns/prov#usedBy> <urn:uuid:6117d2bd-6250-4e87-af09-c315b258959f> <urn:uuid:6117d2bd-6250-4e87-af09-c315b258959f> .
<hash://md5/fda1a6b58c296272924325659a4c328f> <http://purl.org/dc/elements/1.1/format> "text/x-shellscript" .
<urn:uuid:6117d2bd-6250-4e87-af09-c315b258959f> <http://www.w3.org/ns/prov#used> <hash://md5/fda1a6b58c296272924325659a4c328f> .
<urn:uuid:6e31b395-d882-404e-ab40-64858929460e> <http://www.w3.org/ns/prov#wasGeneratedBy> <urn:uuid:6117d2bd-6250-4e87-af09-c315b258959f> .
<hash://md5/e9039d2e531908e901901684f30adc9e> <http://www.w3.org/ns/prov#wasGeneratedBy> <urn:uuid:5c60cce9-d3cd-42c2-9724-e19064b8f8a1> <urn:uuid:5c60cce9-d3cd-42c2-9724-e19064b8f8a1> .
<hash://md5/e9039d2e531908e901901684f30adc9e> <http://www.w3.org/ns/prov#qualifiedGeneration> <urn:uuid:5c60cce9-d3cd-42c2-9724-e19064b8f8a1> <urn:uuid:5c60cce9-d3cd-42c2-9724-e19064b8f8a1> .
<urn:uuid:5c60cce9-d3cd-42c2-9724-e19064b8f8a1> <http://www.w3.org/ns/prov#generatedAtTime> "2023-10-24T23:09:24.323Z"^^<http://www.w3.org/2001/XMLSchema#dateTime> <urn:uuid:5c60cce9-d3cd-42c2-9724-e19064b8f8a1> .
<urn:uuid:5c60cce9-d3cd-42c2-9724-e19064b8f8a1> <http://www.w3.org/1999/02/22-rdf-syntax-ns#type> <http://www.w3.org/ns/prov#Generation> <urn:uuid:5c60cce9-d3cd-42c2-9724-e19064b8f8a1> .
<urn:uuid:5c60cce9-d3cd-42c2-9724-e19064b8f8a1> <http://www.w3.org/ns/prov#used> <urn:uuid:6e31b395-d882-404e-ab40-64858929460e> <urn:uuid:5c60cce9-d3cd-42c2-9724-e19064b8f8a1> .
<urn:uuid:6e31b395-d882-404e-ab40-64858929460e> <http://purl.org/pav/hasVersion> <hash://md5/e9039d2e531908e901901684f30adc9e> <urn:uuid:5c60cce9-d3cd-42c2-9724-e19064b8f8a1> .
<https://preston.guoda.bio> <http://www.w3.org/1999/02/22-rdf-syntax-ns#type> <http://www.w3.org/ns/prov#SoftwareAgent> <urn:uuid:45db912d-226d-45e2-9ca1-e2e3f9898859> .
<https://preston.guoda.bio> <http://www.w3.org/1999/02/22-rdf-syntax-ns#type> <http://www.w3.org/ns/prov#Agent> <urn:uuid:45db912d-226d-45e2-9ca1-e2e3f9898859> .
<https://preston.guoda.bio> <http://purl.org/dc/terms/description> "Preston is a software program that finds, archives and provides access to biodiversity datasets."@en <urn:uuid:45db912d-226d-45e2-9ca1-e2e3f9898859> .
<urn:uuid:45db912d-226d-45e2-9ca1-e2e3f9898859> <http://www.w3.org/1999/02/22-rdf-syntax-ns#type> <http://www.w3.org/ns/prov#Activity> <urn:uuid:45db912d-226d-45e2-9ca1-e2e3f9898859> .
<urn:uuid:45db912d-226d-45e2-9ca1-e2e3f9898859> <http://purl.org/dc/terms/description> "A crawl event that discovers biodiversity archives."@en <urn:uuid:45db912d-226d-45e2-9ca1-e2e3f9898859> .
<urn:uuid:45db912d-226d-45e2-9ca1-e2e3f9898859> <http://www.w3.org/ns/prov#startedAtTime> "2023-10-24T23:08:19.603Z"^^<http://www.w3.org/2001/XMLSchema#dateTime> <urn:uuid:45db912d-226d-45e2-9ca1-e2e3f9898859> .
<urn:uuid:45db912d-226d-45e2-9ca1-e2e3f9898859> <http://www.w3.org/ns/prov#wasStartedBy> <https://preston.guoda.bio> <urn:uuid:45db912d-226d-45e2-9ca1-e2e3f9898859> .
<https://doi.org/10.5281/zenodo.1410543> <http://www.w3.org/ns/prov#usedBy> <urn:uuid:45db912d-226d-45e2-9ca1-e2e3f9898859> <urn:uuid:45db912d-226d-45e2-9ca1-e2e3f9898859> .
<https://doi.org/10.5281/zenodo.1410543> <http://www.w3.org/1999/02/22-rdf-syntax-ns#type> <http://purl.org/dc/dcmitype/Software> <urn:uuid:45db912d-226d-45e2-9ca1-e2e3f9898859> .
<https://doi.org/10.5281/zenodo.1410543> <http://purl.org/dc/terms/bibliographicCitation> "Jorrit Poelen, Icaro Alzuru, & Michael Elliott. 2021. Preston: a biodiversity dataset tracker (Version 0.7.6-SNAPSHOT) [Software]. Zenodo. http://doi.org/10.5281/zenodo.1410543"@en <urn:uuid:45db912d-226d-45e2-9ca1-e2e3f9898859> .
<urn:uuid:0659a54f-b713-4f86-a917-5be166a14110> <http://www.w3.org/1999/02/22-rdf-syntax-ns#type> <http://www.w3.org/ns/prov#Entity> <urn:uuid:45db912d-226d-45e2-9ca1-e2e3f9898859> .
<urn:uuid:0659a54f-b713-4f86-a917-5be166a14110> <http://purl.org/dc/terms/description> "A biodiversity dataset graph archive."@en <urn:uuid:45db912d-226d-45e2-9ca1-e2e3f9898859> .
<hash://md5/7679be7f82aa33e468683b87a45ad656> <http://www.w3.org/ns/prov#usedBy> <urn:uuid:45db912d-226d-45e2-9ca1-e2e3f9898859> <urn:uuid:45db912d-226d-45e2-9ca1-e2e3f9898859> .
<hash://md5/fda1a6b58c296272924325659a4c328f> <http://www.w3.org/ns/prov#wasGeneratedBy> <urn:uuid:249c6164-4042-4e82-8bab-10fae8505ace> <urn:uuid:249c6164-4042-4e82-8bab-10fae8505ace> .
<hash://md5/fda1a6b58c296272924325659a4c328f> <http://www.w3.org/ns/prov#qualifiedGeneration> <urn:uuid:249c6164-4042-4e82-8bab-10fae8505ace> <urn:uuid:249c6164-4042-4e82-8bab-10fae8505ace> .
<urn:uuid:249c6164-4042-4e82-8bab-10fae8505ace> <http://www.w3.org/ns/prov#generatedAtTime> "2023-10-24T23:08:19.669Z"^^<http://www.w3.org/2001/XMLSchema#dateTime> <urn:uuid:249c6164-4042-4e82-8bab-10fae8505ace> .
<urn:uuid:249c6164-4042-4e82-8bab-10fae8505ace> <http://www.w3.org/1999/02/22-rdf-syntax-ns#type> <http://www.w3.org/ns/prov#Generation> <urn:uuid:249c6164-4042-4e82-8bab-10fae8505ace> .
<urn:uuid:249c6164-4042-4e82-8bab-10fae8505ace> <http://www.w3.org/ns/prov#wasInformedBy> <urn:uuid:45db912d-226d-45e2-9ca1-e2e3f9898859> <urn:uuid:249c6164-4042-4e82-8bab-10fae8505ace> .
<urn:uuid:249c6164-4042-4e82-8bab-10fae8505ace> <http://www.w3.org/ns/prov#used> <urn:uuid:8bbdc61f-5708-4245-9465-03c3374eed64> <urn:uuid:249c6164-4042-4e82-8bab-10fae8505ace> .
<urn:uuid:8bbdc61f-5708-4245-9465-03c3374eed64> <http://purl.org/pav/hasVersion> <hash://md5/fda1a6b58c296272924325659a4c328f> <urn:uuid:249c6164-4042-4e82-8bab-10fae8505ace> .
<https://preston.guoda.bio> <http://www.w3.org/1999/02/22-rdf-syntax-ns#type> <http://www.w3.org/ns/prov#SoftwareAgent> <urn:uuid:0e49506c-4e79-4bbd-a99e-e4ca99938e03> .
<https://preston.guoda.bio> <http://www.w3.org/1999/02/22-rdf-syntax-ns#type> <http://www.w3.org/ns/prov#Agent> <urn:uuid:0e49506c-4e79-4bbd-a99e-e4ca99938e03> .
<https://preston.guoda.bio> <http://purl.org/dc/terms/description> "Preston is a software program that finds, archives and provides access to biodiversity datasets."@en <urn:uuid:0e49506c-4e79-4bbd-a99e-e4ca99938e03> .
<urn:uuid:0e49506c-4e79-4bbd-a99e-e4ca99938e03> <http://www.w3.org/1999/02/22-rdf-syntax-ns#type> <http://www.w3.org/ns/prov#Activity> <urn:uuid:0e49506c-4e79-4bbd-a99e-e4ca99938e03> .
<urn:uuid:0e49506c-4e79-4bbd-a99e-e4ca99938e03> <http://purl.org/dc/terms/description> "A crawl event that discovers biodiversity archives."@en <urn:uuid:0e49506c-4e79-4bbd-a99e-e4ca99938e03> .
<urn:uuid:0e49506c-4e79-4bbd-a99e-e4ca99938e03> <http://www.w3.org/ns/prov#startedAtTime> "2023-10-24T22:48:00.288Z"^^<http://www.w3.org/2001/XMLSchema#dateTime> <urn:uuid:0e49506c-4e79-4bbd-a99e-e4ca99938e03> .
<urn:uuid:0e49506c-4e79-4bbd-a99e-e4ca99938e03> <http://www.w3.org/ns/prov#wasStartedBy> <https://preston.guoda.bio> <urn:uuid:0e49506c-4e79-4bbd-a99e-e4ca99938e03> .
<https://doi.org/10.5281/zenodo.1410543> <http://www.w3.org/ns/prov#usedBy> <urn:uuid:0e49506c-4e79-4bbd-a99e-e4ca99938e03> <urn:uuid:0e49506c-4e79-4bbd-a99e-e4ca99938e03> .
<https://doi.org/10.5281/zenodo.1410543> <http://www.w3.org/1999/02/22-rdf-syntax-ns#type> <http://purl.org/dc/dcmitype/Software> <urn:uuid:0e49506c-4e79-4bbd-a99e-e4ca99938e03> .
<https://doi.org/10.5281/zenodo.1410543> <http://purl.org/dc/terms/bibliographicCitation> "Jorrit Poelen, Icaro Alzuru, & Michael Elliott. 2021. Preston: a biodiversity dataset tracker (Version 0.7.6-SNAPSHOT) [Software]. Zenodo. http://doi.org/10.5281/zenodo.1410543"@en <urn:uuid:0e49506c-4e79-4bbd-a99e-e4ca99938e03> .
<urn:uuid:0659a54f-b713-4f86-a917-5be166a14110> <http://www.w3.org/1999/02/22-rdf-syntax-ns#type> <http://www.w3.org/ns/prov#Entity> <urn:uuid:0e49506c-4e79-4bbd-a99e-e4ca99938e03> .
<urn:uuid:0659a54f-b713-4f86-a917-5be166a14110> <http://purl.org/dc/terms/description> "A biodiversity dataset graph archive."@en <urn:uuid:0e49506c-4e79-4bbd-a99e-e4ca99938e03> .
<hash://md5/05abf23c0b9e5f4bc721ff407455af0a> <http://www.w3.org/ns/prov#wasGeneratedBy> <urn:uuid:c5a0c4d2-f047-4a12-a002-872e024c928f> <urn:uuid:c5a0c4d2-f047-4a12-a002-872e024c928f> .
<hash://md5/05abf23c0b9e5f4bc721ff407455af0a> <http://www.w3.org/ns/prov#qualifiedGeneration> <urn:uuid:c5a0c4d2-f047-4a12-a002-872e024c928f> <urn:uuid:c5a0c4d2-f047-4a12-a002-872e024c928f> .
<urn:uuid:c5a0c4d2-f047-4a12-a002-872e024c928f> <http://www.w3.org/ns/prov#generatedAtTime> "2023-10-24T22:48:07.807Z"^^<http://www.w3.org/2001/XMLSchema#dateTime> <urn:uuid:c5a0c4d2-f047-4a12-a002-872e024c928f> .
<urn:uuid:c5a0c4d2-f047-4a12-a002-872e024c928f> <http://www.w3.org/1999/02/22-rdf-syntax-ns#type> <http://www.w3.org/ns/prov#Generation> <urn:uuid:c5a0c4d2-f047-4a12-a002-872e024c928f> .
<urn:uuid:c5a0c4d2-f047-4a12-a002-872e024c928f> <http://www.w3.org/ns/prov#wasInformedBy> <urn:uuid:0e49506c-4e79-4bbd-a99e-e4ca99938e03> <urn:uuid:c5a0c4d2-f047-4a12-a002-872e024c928f> .
<urn:uuid:c5a0c4d2-f047-4a12-a002-872e024c928f> <http://www.w3.org/ns/prov#used> <https://zenodo.org/records/7796465/files/SCAR_Diet_Energetics.zip> <urn:uuid:c5a0c4d2-f047-4a12-a002-872e024c928f> .
<https://zenodo.org/records/7796465/files/SCAR_Diet_Energetics.zip> <http://purl.org/pav/hasVersion> <hash://md5/05abf23c0b9e5f4bc721ff407455af0a> <urn:uuid:c5a0c4d2-f047-4a12-a002-872e024c928f> .
```
