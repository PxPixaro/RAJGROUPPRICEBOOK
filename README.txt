# Price Book Folder Structure

## Folder Structure

price_book/
├── index.html
├── data/
│   ├── pricebook.csv
│   └── customers.csv
├── assets/
│   ├── logo/
│   │   └── logo.png
│   └── product-images/
│       ├── KX525.jpg
│       ├── BR1001.jpg
│       └── PARTNO.jpg
└── pdf-templates/
    └── your-sample-template.xlsx

## Pricebook CSV headers

Brand, Segment, VehicleBrand, Model, PartNo, Description, Standard Packing, Packing Size, Rate, MRP, GST, HSN

VehicleBrand और Model में comma separated values allowed हैं:
MARUTI,CHEVROLET,MAHINDRA
SWIFT,BEAT,BOLERO,EECO,INNOVA

## Product Images

Product image filename exact PartNo जैसा रखें:

PartNo: KX525
Image: assets/product-images/KX525.jpg

PartNo: BR1001
Image: assets/product-images/BR1001.jpg

## Customer CSV headers

Customer Name, City, Mobile

## Auto-load setup

index.html में यह line true करें:

const AUTO_LOAD_FROM_FOLDER = true;

फिर folder को hosting पर upload करें या local server से चलाएँ.

Local server command:
python -m http.server 8000

फिर browser में open करें:
http://localhost:8000

Direct file double-click करके open करेंगे तो browser security के कारण CSV auto-load block हो सकता है.
उस case में upload buttons से files manually upload करें.
