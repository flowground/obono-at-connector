# ![LOGO](logo.png) obono RKSV **flow**ground Connector

## Description

A generated **flow**ground connector for the obono RKSV API (version 1.3.4.0).

Generated from: https://api.apis.guru/v2/specs/obono.at/1.3.4.0/swagger.json<br/>
Generated at: 2019-05-07T17:43:22+03:00

## API Description

Provides a RESTful API for interacting with virtual cash registers and creating receipts that are conform with the Registrierkassensicherheitsverordnung (RKSV).

You may find our [automatically generated clients](./clients) for various programming languages and environments helpful...


## Authorization

Supported authorization schemes:
- Basic Authentication
- API Key
## Actions

### Request a JWT access token using your obono username and password.

*Tags:* `auth`

### Retrieves a particular `Beleg` from the "Datenerfassungsprotokoll".

*Tags:* `beleg`

#### Input Parameters
* `belegUuid` - _required_ - The `_uuid` of the `Beleg` to fetch.

### get_export_csv_registrierkassen__registrierkasseUuid__belege

*Tags:* `export`

#### Input Parameters
* `registrierkasseUuid` - _required_ - The `_uuid` of the `Registrierkasse` to export.
* `before` - _optional_ - Only return results that were saved before the specified date-time string (i.e., anything that `Date.parse()` can parse).
* `after` - _optional_ - Only return results that were saved after the specified date-time string (i.e., anything that `Date.parse()` can parse).
* `posten` - _optional_ - Export `Posten` instead of `Belegdaten`.

### get_export_dep131_registrierkassen__registrierkasseUuid__belege

*Tags:* `export`

#### Input Parameters
* `registrierkasseUuid` - _required_ - The `_uuid` of the `Registrierkasse` to export.
* `before` - _optional_ - Only return results that were saved before the specified date-time string (i.e., anything that `Date.parse()` can parse).
* `after` - _optional_ - Only return results that were saved after the specified date-time string (i.e., anything that `Date.parse()` can parse).

### get_export_dep7_registrierkassen__registrierkasseUuid__belege

*Tags:* `export`

#### Input Parameters
* `registrierkasseUuid` - _required_ - The `_uuid` of the `Registrierkasse` to export.
* `before` - _optional_ - Only return results that were saved before the specified date-time string (i.e., anything that `Date.parse()` can parse).
* `after` - _optional_ - Only return results that were saved after the specified date-time string (i.e., anything that `Date.parse()` can parse).

### get_export_html_belege__belegUuid_

*Tags:* `export`

#### Input Parameters
* `belegUuid` - _required_ - The `_uuid` of a particular `Beleg` to export.

### get_export_pdf_belege__belegUuid_

*Tags:* `export`

#### Input Parameters
* `belegUuid` - _required_ - The `_uuid` of a particular `Beleg` to export.

### get_export_qr_belege__belegUuid_

*Tags:* `export`

#### Input Parameters
* `belegUuid` - _required_ - The `_uuid` of a particular `Beleg` to export.

### get_export_thermal_print_belege__belegUuid_

*Tags:* `export`

#### Input Parameters
* `belegUuid` - _required_ - The `_uuid` of a particular `Beleg` to export.
* `qr` - _optional_ - Should the RKSV QR code should be rendered?
* `width` - _optional_ - Number of characters per line.
* `dialect` - _optional_ - The thermal printer dialect.
    Possible values: esc, star.
* `encoding` - _optional_ - The encoding of the binary data.
    Possible values: raw, base64.

### get_export_xls_registrierkassen__registrierkasseUuid__belege

*Tags:* `export`

#### Input Parameters
* `registrierkasseUuid` - _required_ - The `_uuid` of the `Registrierkasse` to export.
* `before` - _optional_ - Only return results that were saved before the specified date-time string (i.e., anything that `Date.parse()` can parse).
* `after` - _optional_ - Only return results that were saved after the specified date-time string (i.e., anything that `Date.parse()` can parse).

### Returns information about a particular `Registrierkasse`.

*Tags:* `registrierkasse`

#### Input Parameters
* `registrierkasseUuid` - _required_ - The `_uuid` of a particular `Registrierkasse` to fetch.

### Generates an `Abschlussbeleg`.

*Tags:* `beleg`

#### Input Parameters
* `registrierkasseUuid` - _required_ - The `_uuid` of the `Registrierkasse` to retrieve the `Beleg` collection.

### Retrieves the `Beleg` collection from the "Datenerfassungsprotokoll".

*Tags:* `beleg`

#### Input Parameters
* `registrierkasseUuid` - _required_ - The `_uuid` of the `Registrierkasse` to retrieve the `Beleg` collection.
* `format` - _required_ - Determines the format of the `Beleg` collection.
    Possible values: export, beleg, uuidlist.
* `order` - _optional_ - Determines the sorting order.
    Possible values: asc, desc.
* `limit` - _optional_ - Limits the number of returned results.
* `offset` - _optional_ - Skips the specified number of results from the result set.
* `before` - _optional_ - Only return results that where saved before the specified date-time string (i.e., anything that `Date.parse()` can parse).
* `after` - _optional_ - Only return results that where saved after the specified date-time string (i.e., anything that `Date.parse()` can parse).
* `gte` - _optional_ - Only return results that have at least a particular `Belegnummer`.
* `lte` - _optional_ - Only return results that have at most a particular `Belegnummer`.

### Retrieves a particular `Beleg` from the "Datenerfassungsprotokoll".

*Tags:* `beleg`

#### Input Parameters
* `registrierkasseUuid` - _required_ - The `_uuid` of the `Registrierkasse` that contains the requested `Beleg`.
* `belegUuid` - _required_ - The `_uuid` of the `Beleg` to fetch.

### Signs a receipt and stores it in the "Datenerfassungsprotokoll".

*Tags:* `beleg`

#### Input Parameters
* `registrierkasseUuid` - _required_ - The `_uuid` of the `Registrierkasse` to use for signing data.
* `belegUuid` - _required_ - The `_uuid` of the `Beleg` to store.

### Generates a DEP file.

*Tags:* `registrierkasse`

#### Input Parameters
* `registrierkasseUuid` - _required_ - The `_uuid` of the `Registrierkasse` to retrieve the DEP file.

### Returns a list of `Monatsbelege`.

*Tags:* `monatsbelege`

#### Input Parameters
* `registrierkasseUuid` - _required_ - The `_uuid` of the `Registrierkasse`.
* `year` - _optional_
* `month` - _optional_

## License

**flow**ground :- Telekom iPaaS / obono-at-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
