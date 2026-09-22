# SEC Form 4 Research Starter Kit

A practical, source-first workflow for researching insider transactions reported on SEC Form 4.

This repository is for financial researchers, journalists, developers, and investors who want to inspect public ownership-change filings without treating a single filing as a guaranteed trading signal.

## What this covers

- How to distinguish the transaction date from the filing date
- How to read common Form 4 transaction codes such as `P`, `S`, `A`, `M`, `F`, `G`, and `J`
- Which fields to record when building a reproducible research table
- How to check direct versus indirect ownership
- Why footnotes, related rows, and Rule 10b5-1 plans can change the context
- How to return to the original SEC filing before publishing an interpretation

## A source-first workflow

1. Start with the issuer, reporting owner, and accession number.
2. Record the transaction date and filing date separately.
3. Identify the security, transaction code, shares, price, and acquired/disposed direction.
4. Check whether ownership is direct or indirect and read any nature-of-ownership text.
5. Read the footnotes and the other rows in the same filing.
6. Compare the event with prior filings only after the individual filing is understood.
7. Keep the filing fact separate from any research interpretation.
8. Link to the original SEC filing in notes, articles, or datasets.

## Suggested research table

| Field | Why it matters |
| --- | --- |
| Issuer name and ticker | Prevents symbol or issuer mix-ups |
| Reporting owner and role | Gives the filing human and corporate context |
| Transaction date | Dates the reported ownership change |
| Filing date | Dates when the disclosure became public |
| Form 4 accession number | Provides a stable source reference |
| Security and security type | Separates common stock from derivative or other securities |
| Transaction code | Describes the reported event; do not collapse every code into “buy” or “sell” |
| Shares and price | Supports a reproducible value calculation where applicable |
| Direct / indirect ownership | Shows whether the filer owns the securities directly or through another entity |
| Footnotes and related rows | Can explain plans, weighted-average prices, taxes, awards, or other context |
| Original SEC URL | Lets another researcher verify the record |

## Common code reminders

The code is a starting point, not a complete explanation of economic intent.

| Code | Plain-language reminder |
| --- | --- |
| `P` | Reported purchase or other acquisition in the filing context |
| `S` | Reported sale or other disposition in the filing context |
| `A` | Reported acquisition such as an award or grant, depending on the filing details |
| `M` | Reported exercise or conversion of a derivative security |
| `F` | Reported payment or withholding-related disposition in the filing context |
| `G` | Reported gift or transfer in the filing context |
| `J` | Other transaction; read the transaction description and footnotes |

Always verify the exact code description, table, footnotes, and ownership details in the original filing. This table is an orientation aid, not a substitute for SEC filing instructions.

## Research tools

The official source remains the SEC filing. For a searchable interface that organizes stored Form 4 records by ticker, company, reporting owner, date, transaction code, and filing accession, see [Form4Beacon](https://form4beacon.com/).

Form4Beacon links back to the original SEC filing where available. It is intended to make public disclosure data easier to inspect, not to provide investment advice or predict future stock performance.

## Reproducibility checklist

Before sharing a claim based on an insider transaction, confirm that your notes contain:

- The SEC filing URL or accession number
- Issuer and ticker mapping
- Reporting owner and role exactly as reported
- Transaction date and filing date
- Code, shares, price, and value calculation
- Direct or indirect ownership
- Relevant footnotes and related transaction rows
- A clear distinction between the filing fact and your interpretation

## Example wording for a research note

> According to the Form 4 filed on `[filing date]`, `[reporting owner]`, identified as `[role]`, reported a `[transaction description]` in `[issuer]` on `[transaction date]`. The filing reports `[shares]` shares at `[price]` under transaction code `[code]`. The filing and footnotes should be reviewed before drawing any conclusion about intent or market impact.

## Limitations

Form 4 filings are public disclosures, but they may be delayed, incomplete, amended, or contain filer errors. A transaction can have many explanations, including compensation, tax obligations, diversification, gifts, derivative exercises, or a pre-arranged trading plan. Historical insider activity does not establish future stock performance.

This repository is educational and does not provide investment, legal, tax, or accounting advice. Verify important information against the original SEC filing and applicable SEC guidance.

## Contributing

Contributions are welcome when they improve source accuracy, explain filing structure, add reproducible examples, or clarify a limitation. Please include the primary SEC source for changes to code definitions or filing interpretation.

Please do not submit promotional link lists, unsupported trading claims, or datasets without source and date information.

## License

Add a repository license before publishing if you want others to reuse or modify your original text or code. SEC filings and linked third-party materials remain subject to their respective terms.
