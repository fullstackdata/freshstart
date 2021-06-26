# IAM Policy Document
## RECAP

Key|Example
---|--------
<b>R</b> Resource| EC2 <br/>
<b>E</b> Effect| Allow or Deny <br/>
<b>C</b> Conditions| StringEquals Resource Tag<br/>
<b>A</b> Actions| ec2:AttachVolume, ec2:DetachVolume<br/>
<b>P</b> Policiy Variables (optional)| ${aws:username}<br/>

### Least Previlege
  * Access Advisor
    * See permissions granted and when they were last used, remove policies unused over a long period of time
  * Access Analyzer
    * Resources shared with external entities

### Explicit DENY >>>> ALLOW
  * Assures security and overwriting by other policies
  * Necessitates the need on <b>NOTACTION</b> for certain users like PowerUserAccess

