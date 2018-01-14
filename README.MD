A visualization of the cleaned AB data is shown at http://thanhleviet.github.io/ab-bidding.html

1. The raw data were download from:
  + Year 2015-2016:
    + http://vinapharm.com.vn/index.php/news/1088/Tong-hop-ket-qua-trung-thau-cua-cac-Benh-vien-Trung-uong,-So-Y-te-cac-tinh-thanh-pho,-Benh-vien-da-khoa-tinh,-thanh-pho-nam-2016-(29-12-2016).html
  + Year 2016-2017:
    + http://www.dav.gov.vn/Default.aspx?action=detail&newsid=1577&type=3
    + http://www.dav.gov.vn/Default.aspx?action=detail&type=3&newsid=1576
  
2. Meta Data and Data Cleaning: 
  + The data includes bidding price for 3 years: 2015, 2016, 2107. The original are in excel format. There are mainly following columns:
Active_Ingredient; Concentration; Drug Name; License_Code (Of the bidder ?); Form; Manufaturer; Origin of Drug (Made_In); Minimum Unit; Quantity; Price per unit with VAT; Total Price; Bidder; Hospital/Department; Group of Drug; Year.
  + Many identical records were found (rows with the same value in the columns: Year, Active Ingredient, Concentration, License Code, Form, Manufacturer; Origin of Drug, Quantity, Total Price, Bidder, Hospital/Department) for the year 2016 in both the 2 periods. I suspected they were duplicated. Thus, these identical records were removed, only one unique left. As I'm interested in antibiotics bidding price, I just focused on cleaning data for AB records, which were stored in ad.rds or ad.csv files.
  + Antibiotic active ingredient were matched with a list of antibiotics at http://www.emedexpert.com/lists/antibiotics.shtml
