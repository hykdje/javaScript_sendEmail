function sendEmail(){
 MailApp.sendEmail("Email@email.com", "Hello", "Email body");
}


function createEmailTrigger(){
  
  ScriptApp.newTrigger('sendEmail')
  .timeBased()
  .onWeekDay(ScriptApp.WeekDay.SATURDAY)
  .create();
}
