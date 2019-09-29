# TARUN
SMART ATTENDANCE
Our idea was the smart attendance we firstly create a QR code for every students in the class and the attendence for the students will be given by scaning the particular QR code of the students in the teachers phone then the attendance of the students will be updated in the XLsheet which was in the portal and also the students can see their attendance in that XLsheet and not only in this form this idea is also used in the collage mess in this when the student shows the QR code then it will scan his name and prints in XLsheet and then he will get his plate  

function doGet(e){
  var ss = SpreadsheetApp.openByUrl("URL of the spreed sheet");
  var sheet = ss.getSheetByName("Sheet1");

  insert(e,sheet);

}

function doPost(e){
  var ss = SpreadsheetApp.openByUrl("URL of the spreed sheet");
  var sheet = ss.getSheetByName("Sheet1");

  insert(e,sheet);

}



function insert(e,sheet)
{
  var sdata = e.parameter.sdata;
 
  var date = new Date()
 
  sheet.appendRow([date,sdata]);
 }
