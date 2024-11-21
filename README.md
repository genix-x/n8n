# n8n
Workflow Seller Central Amazon

## Rev calculator Amazon

### /GET productmatch
https://sellercentral.amazon.fr/rcpublic/productmatch?searchKey=B0C3HCD34R&countryCode=FR&locale=fr-FR

```json
{
    "succeed": true,
    "data": {
        "countryCode": "FR",
        "merchantId": "PUBLIC",
        "searchKey": "B0C3HCD34R",
        "myProducts": {
            "totalProductCount": 0,
            "currentPage": 1,
            "products": []
        },
        "otherProducts": {
            "totalProductCount": 1,
            "currentPage": 1,
            "products": [
                {
                    "asin": "B0C3HCD34R",
                    "imageUrl": "https://m.media-amazon.com/images/I/41jcCpExIzL._SL120_.jpg",
                    "thumbStringUrl": "https://m.media-amazon.com/images/I/41jcCpExIzL._SL120_SL80_.jpg",
                    "gl": "gl_musical_instruments",
                    "title": "Soundcore by Anker Q20i Casque Bluetooth sans Fil avec réduction de Bruit Hybride Active, Casque Over-Ear, 40 Heures de Lecture en Mode ANC, Hi-Res Audio, Basses Profondes, Personnalisation Via App",
                    "weightUnit": "kilograms",
                    "weightUnitStringId": "SC_FBA_UnitOfMeasure_Kilograms_45299",
                    "weight": 0.0000,
                    "dimensionUnit": "centimeters",
                    "dimensionUnitStringId": "SC_FBA_UnitOfMeasure_Centimeters_39147",
                    "width": 0.0000,
                    "length": 0.0000,
                    "height": 0.0000,
                    "price": 0.0,
                    "link": "https://www.amazon.fr/gp/product/B0C3HCD34R/ref=xx_dp_cont_revecalc",
                    "isMyProduct": false,
                    "salesRank": 796,
                    "salesRankContextName": "High-Tech",
                    "customerReviewsCount": 14221,
                    "customerReviewsRating": "4,6 sur 5 étoiles",
                    "customerReviewsRatingfullStarCount": 4,
                    "customerReviewsRatingValue": 4.6,
                    "offerCount": 3
                }
            ]
        }
    }
}

```

### /GET getadditionalpronductinfo
https://sellercentral.amazon.fr/rcpublic/getadditionalpronductinfo?countryCode=FR&asin=B0C3HCD34R&fnsku=&searchType=GENERAL&locale=fr-FR

```json
{
  "succeed": true,
  "data": {
      "asin": "B0C3HCD34R",
      "soldBy": "AnkerDirect FR",
      "condition": "New",
      "shipsFrom": "Amazon",
      "price": {
          "amount": 45.99,
          "currency": "EUR"
      },
      "shipping": {
          "amount": 0.0,
          "currency": "EUR"
      }
  }
}
```


### /GET getprograms
https://sellercentral.amazon.fr/rcpublic/getprograms?countryCode=FR&mSku=&locale=fr-FR

```json
{
  "succeed": true,
  "programInfoList": [
      {
          "name": "MFN",
          "programStringIds": [
              "SC_FBA_Calc_program_mfn"
          ],
          "displayPriority": 0,
          "benefitsNotes": {
              "benefitsStringIds": [],
              "notesStringIds": []
          }
      },
      {
          "name": "Core",
          "programStringIds": [
              "SC_FBA_Calc_program_fba"
          ],
          "displayPriority": 1,
          "benefitsNotes": {
              "benefitsStringIds": [
                  "SC_FBA_Calc_program_fba_benefits1",
                  "SC_FBA_Calc_program_fba_benefits2",
                  "SC_FBA_Calc_program_fba_benefits3",
                  "SC_FBA_Calc_program_fba_benefits4"
              ],
              "notesStringIds": [
                  "SC_FBA_Calc_program_fba_notes"
              ]
          }
      },
      {
          "name": "EFN",
          "programStringIds": [
              "SC_FBA_Calc_program_efn"
          ],
          "displayPriority": 2,
          "benefitsNotes": {
              "benefitsStringIds": [
                  "SC_FBA_Calc_program_efn_benefits1",
                  "SC_FBA_Calc_program_efn_benefits2"
              ],
              "notesStringIds": [
                  "SC_FBA_Calc_program_efn_notes"
              ]
          }
      },
      {
          "name": "PanEU",
          "programStringIds": [
              "SC_FBA_Calc_program_paneu"
          ],
          "displayPriority": 3,
          "benefitsNotes": {
              "benefitsStringIds": [
                  "SC_FBA_Calc_program_paneu_benefits1",
                  "SC_FBA_Calc_program_paneu_benefits2",
                  "SC_FBA_Calc_program_paneu_benefits3"
              ],
              "notesStringIds": [
                  "SC_FBA_Calc_program_paneu_notes"
              ]
          }
      },
      {
          "name": "EURF",
          "programStringIds": [
              "SC_FBA_Calc_program_eurf"
          ],
          "displayPriority": 4,
          "benefitsNotes": {
              "benefitsStringIds": [
                  "SC_FBA_Calc_program_eurf_benefits1",
                  "SC_FBA_Calc_program_eurf_benefits2",
                  "SC_FBA_Calc_program_eurf_benefits3"
              ],
              "notesStringIds": [
                  "SC_FBA_Calc_program_eurf_notes"
              ]
          }
      }
  ]
}
```

### /POST getfees
https://sellercentral.amazon.fr/rcpublic/getfees?countryCode=FR&locale=fr-FR

```json
{
  "succeed": true,
  "data": {
      "countryCode": "FR",
      "merchantId": "A3CC1LTAV5LCJW",
      "asin": "B0C3HCD34R",
      "inventoryUnitInfo": {},
      "programFeeResultMap": {
          "Core#0": {
              "otherCost": {
                  "vatRate": 0.2,
                  "vatAmount": {
                      "amount": 7.665,
                      "currency": "EUR"
                  }
              },
              "perUnitPeakStorageFee": {
                  "feeAmount": {
                      "amount": 0.12192,
                      "currency": "EUR"
                  },
                  "promotionAmount": {
                      "amount": 0.0,
                      "currency": "EUR"
                  },
                  "taxAmount": {
                      "amount": 0.0,
                      "currency": "EUR"
                  },
                  "total": {
                      "amount": 0.12192,
                      "currency": "EUR"
                  },
                  "id": "FBAStorageFee",
                  "feeNameStringId": "FS-StorageFee-FullName",
                  "timeOfFeesEstimate": 1732128778.578635433,
                  "componentFees": [
                      {
                          "feeAmount": {
                              "amount": 0.0,
                              "currency": "EUR"
                          },
                          "promotionAmount": {
                              "amount": 0.0,
                              "currency": "EUR"
                          },
                          "taxAmount": {
                              "amount": 0.0,
                              "currency": "EUR"
                          },
                          "total": {
                              "amount": 0.0,
                              "currency": "EUR"
                          },
                          "feeNameStringId": "UtilizationSurchargeFee",
                          "timeOfFeesEstimate": 1732128778.578635433
                      },
                      {
                          "feeAmount": {
                              "amount": 0.12192,
                              "currency": "EUR"
                          },
                          "promotionAmount": {
                              "amount": 0.0,
                              "currency": "EUR"
                          },
                          "taxAmount": {
                              "amount": 0.0,
                              "currency": "EUR"
                          },
                          "total": {
                              "amount": 0.12192,
                              "currency": "EUR"
                          },
                          "feeNameStringId": "BaseFee",
                          "timeOfFeesEstimate": 1732128778.578635433
                      }
                  ]
              },
              "perUnitNonPeakStorageFee": {
                  "feeAmount": {
                      "amount": 0.07926,
                      "currency": "EUR"
                  },
                  "promotionAmount": {
                      "amount": 0.0,
                      "currency": "EUR"
                  },
                  "taxAmount": {
                      "amount": 0.0,
                      "currency": "EUR"
                  },
                  "total": {
                      "amount": 0.07926,
                      "currency": "EUR"
                  },
                  "id": "FBAStorageFee",
                  "feeNameStringId": "FS-StorageFee-FullName",
                  "timeOfFeesEstimate": 1740077578.578000000,
                  "componentFees": [
                      {
                          "feeAmount": {
                              "amount": 0.0,
                              "currency": "EUR"
                          },
                          "promotionAmount": {
                              "amount": 0.0,
                              "currency": "EUR"
                          },
                          "taxAmount": {
                              "amount": 0.0,
                              "currency": "EUR"
                          },
                          "total": {
                              "amount": 0.0,
                              "currency": "EUR"
                          },
                          "feeNameStringId": "UtilizationSurchargeFee",
                          "timeOfFeesEstimate": 1740077578.578000000
                      },
                      {
                          "feeAmount": {
                              "amount": 0.07926,
                              "currency": "EUR"
                          },
                          "promotionAmount": {
                              "amount": 0.0,
                              "currency": "EUR"
                          },
                          "taxAmount": {
                              "amount": 0.0,
                              "currency": "EUR"
                          },
                          "total": {
                              "amount": 0.07926,
                              "currency": "EUR"
                          },
                          "feeNameStringId": "BaseFee",
                          "timeOfFeesEstimate": 1740077578.578000000
                      }
                  ]
              },
              "otherFeeInfoMap": {
                  "BubblewrapFee": {
                      "feeAmount": {
                          "amount": 0.75,
                          "currency": "EUR"
                      },
                      "promotionAmount": {
                          "amount": 0.0,
                          "currency": "EUR"
                      },
                      "taxAmount": {
                          "amount": 0.0,
                          "currency": "EUR"
                      },
                      "total": {
                          "amount": 0.75,
                          "currency": "EUR"
                      },
                      "id": "BubblewrapFee",
                      "feeNameStringId": "BubblewrapFee",
                      "timeOfFeesEstimate": 1732128778.578635433
                  },
                  "FulfillmentFee": {
                      "feeAmount": {
                          "amount": 5.85,
                          "currency": "EUR"
                      },
                      "promotionAmount": {
                          "amount": 0.0,
                          "currency": "EUR"
                      },
                      "taxAmount": {
                          "amount": 0.0,
                          "currency": "EUR"
                      },
                      "total": {
                          "amount": 5.85,
                          "currency": "EUR"
                      },
                      "id": "FulfillmentFee",
                      "feeNameStringId": "FS-FBAPerUnitFulfillmentFee-FullName",
                      "timeOfFeesEstimate": 1732128778.578635433
                  },
                  "ReferralFee": {
                      "feeAmount": {
                          "amount": 6.9,
                          "currency": "EUR"
                      },
                      "promotionAmount": {
                          "amount": 0.0,
                          "currency": "EUR"
                      },
                      "taxAmount": {
                          "amount": 0.0,
                          "currency": "EUR"
                      },
                      "total": {
                          "amount": 6.9,
                          "currency": "EUR"
                      },
                      "id": "ReferralFee",
                      "feeNameStringId": "FS-Commission-FullName",
                      "timeOfFeesEstimate": 1732128778.578635433
                  },
                  "LabelingFee": {
                      "feeAmount": {
                          "amount": 0.45,
                          "currency": "EUR"
                      },
                      "promotionAmount": {
                          "amount": 0.0,
                          "currency": "EUR"
                      },
                      "taxAmount": {
                          "amount": 0.0,
                          "currency": "EUR"
                      },
                      "total": {
                          "amount": 0.45,
                          "currency": "EUR"
                      },
                      "id": "LabelingFee",
                      "feeNameStringId": "LabelingFee",
                      "timeOfFeesEstimate": 1732128778.578635433
                  },
                  "PolybaggingFee": {
                      "feeAmount": {
                          "amount": 0.5,
                          "currency": "EUR"
                      },
                      "promotionAmount": {
                          "amount": 0.0,
                          "currency": "EUR"
                      },
                      "taxAmount": {
                          "amount": 0.0,
                          "currency": "EUR"
                      },
                      "total": {
                          "amount": 0.5,
                          "currency": "EUR"
                      },
                      "id": "PolybaggingFee",
                      "feeNameStringId": "PolybaggingFee",
                      "timeOfFeesEstimate": 1732128778.578635433
                  },
                  "DigitalServicesFee": {
                      "feeAmount": {
                          "amount": 0.42,
                          "currency": "EUR"
                      },
                      "promotionAmount": {
                          "amount": 0.0,
                          "currency": "EUR"
                      },
                      "taxAmount": {
                          "amount": 0.0,
                          "currency": "EUR"
                      },
                      "total": {
                          "amount": 0.42,
                          "currency": "EUR"
                      },
                      "id": "DigitalServicesFee",
                      "feeNameStringId": "FS-DigitalServicesFee-FullName",
                      "timeOfFeesEstimate": 1732128778.578635433
                  },
                  "FixedClosingFee": {
                      "feeAmount": {
                          "amount": 0.99,
                          "currency": "EUR"
                      },
                      "promotionAmount": {
                          "amount": 0.0,
                          "currency": "EUR"
                      },
                      "taxAmount": {
                          "amount": 0.0,
                          "currency": "EUR"
                      },
                      "total": {
                          "amount": 0.99,
                          "currency": "EUR"
                      },
                      "id": "FixedClosingFee",
                      "feeNameStringId": "FS-FixedClosingFee-FullName",
                      "timeOfFeesEstimate": 1732128778.578635433
                  },
                  "OpaqueBaggingFee": {
                      "feeAmount": {
                          "amount": 0.41,
                          "currency": "EUR"
                      },
                      "promotionAmount": {
                          "amount": 0.0,
                          "currency": "EUR"
                      },
                      "taxAmount": {
                          "amount": 0.0,
                          "currency": "EUR"
                      },
                      "total": {
                          "amount": 0.41,
                          "currency": "EUR"
                      },
                      "id": "OpaqueBaggingFee",
                      "feeNameStringId": "OpaqueBaggingFee",
                      "timeOfFeesEstimate": 1732128778.578635433
                  },
                  "VariableClosingFee": {
                      "feeAmount": {
                          "amount": 0.0,
                          "currency": "EUR"
                      },
                      "promotionAmount": {
                          "amount": 0.0,
                          "currency": "EUR"
                      },
                      "taxAmount": {
                          "amount": 0.0,
                          "currency": "EUR"
                      },
                      "total": {
                          "amount": 0.0,
                          "currency": "EUR"
                      },
                      "id": "VariableClosingFee",
                      "feeNameStringId": "FS-VariableClosingFee-FullName",
                      "timeOfFeesEstimate": 1732128778.578635433
                  },
                  "TapingFee": {
                      "feeAmount": {
                          "amount": 0.45,
                          "currency": "EUR"
                      },
                      "promotionAmount": {
                          "amount": 0.0,
                          "currency": "EUR"
                      },
                      "taxAmount": {
                          "amount": 0.0,
                          "currency": "EUR"
                      },
                      "total": {
                          "amount": 0.45,
                          "currency": "EUR"
                      },
                      "id": "TapingFee",
                      "feeNameStringId": "TapingFee",
                      "timeOfFeesEstimate": 1732128778.578635433
                  }
              },
              "futureFeeInfoMap": {}
          },
          "MFN#1": {
              "otherCost": {
                  "vatRate": 0.2,
                  "vatAmount": {
                      "amount": 7.665,
                      "currency": "EUR"
                  }
              },
              "otherFeeInfoMap": {
                  "FixedClosingFee": {
                      "feeAmount": {
                          "amount": 0.99,
                          "currency": "EUR"
                      },
                      "promotionAmount": {
                          "amount": 0.0,
                          "currency": "EUR"
                      },
                      "taxAmount": {
                          "amount": 0.0,
                          "currency": "EUR"
                      },
                      "total": {
                          "amount": 0.99,
                          "currency": "EUR"
                      },
                      "id": "FixedClosingFee",
                      "feeNameStringId": "FS-FixedClosingFee-FullName",
                      "timeOfFeesEstimate": 1732128778.578635433
                  },
                  "ReferralFee": {
                      "feeAmount": {
                          "amount": 6.9,
                          "currency": "EUR"
                      },
                      "promotionAmount": {
                          "amount": 0.0,
                          "currency": "EUR"
                      },
                      "taxAmount": {
                          "amount": 0.0,
                          "currency": "EUR"
                      },
                      "total": {
                          "amount": 6.9,
                          "currency": "EUR"
                      },
                      "id": "ReferralFee",
                      "feeNameStringId": "FS-Commission-FullName",
                      "timeOfFeesEstimate": 1732128778.578635433
                  },
                  "VariableClosingFee": {
                      "feeAmount": {
                          "amount": 0.0,
                          "currency": "EUR"
                      },
                      "promotionAmount": {
                          "amount": 0.0,
                          "currency": "EUR"
                      },
                      "taxAmount": {
                          "amount": 0.0,
                          "currency": "EUR"
                      },
                      "total": {
                          "amount": 0.0,
                          "currency": "EUR"
                      },
                      "id": "VariableClosingFee",
                      "feeNameStringId": "FS-VariableClosingFee-FullName",
                      "timeOfFeesEstimate": 1732128778.578635433
                  },
                  "DigitalServicesFee": {
                      "feeAmount": {
                          "amount": 0.24,
                          "currency": "EUR"
                      },
                      "promotionAmount": {
                          "amount": 0.0,
                          "currency": "EUR"
                      },
                      "taxAmount": {
                          "amount": 0.0,
                          "currency": "EUR"
                      },
                      "total": {
                          "amount": 0.24,
                          "currency": "EUR"
                      },
                      "id": "DigitalServicesFee",
                      "feeNameStringId": "FS-DigitalServicesFee-FullName",
                      "timeOfFeesEstimate": 1732128778.578635433
                  }
              },
              "futureFeeInfoMap": {}
          }
      }
  }
}
```
