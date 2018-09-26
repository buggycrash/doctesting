
# Applying new IPs to an existing Security Group


![](NetSec_media/43888b6d01202ba09668f1745077ac5e.png)

Login to UE2S AWS (TTE-DEV) and click EC2

![](NetSec_media/7fc406e6a4c4976f750c57c65bd917b1.png)

Click Instances

![](NetSec_media/b4fe66e5e01d13b72081dfda1b140625.png)

Search for your instance in the list, and click the radio button beside it. This
example uses “DAX-Vanilla”

![](NetSec_media/ba93cc380343b1ffa00202afffede292.png)

At the bottom, click on the desired security group, beside “Security groups”. Do
not modify “default”.

![](NetSec_media/fda9dda1725939201476e1b582668774.png)

Click Inbound

![](NetSec_media/5e6be97305544c7005ca49a5cb34bf9c.png)

Click Edit

![](NetSec_media/6bfdd30bcec5c7711851e1c820915388.png)

Click Add Rule

![](NetSec_media/76a35151cfd241340056b933921b045b.png)

Use the dropdown in the Type column on the left to select RDP, HTTPS, SSH, or
whatever service you need. You can also select Custom if you need to allow a
non-Standard port.

![](NetSec_media/0c269cf1619bab65ca2981bcbc274810.png)

In the Source column, use the dropdown to select My IP. This will automatically
select the IP you are using at the time. To add more IPs, click Add Rule again,
then in the Source column choose Custom and enter individual IPs, or a range of
IPs. You can add as many as you need, but are **strongly suggested to specify
IPs, rather than leaving open to the world / anywhere / 0.0.0.0. Leaving it
open, especially with a Windows host, will almost guarantee it gets attacked.**

![](NetSec_media/f262674c6c0fb041a1183af5f34414cb.png)

Click Save at the bottom right when you have added all the necessary IPs.

![](NetSec_media/ea7f97547a2d3d5bc3241db3429b634b.png)

Launch Remote Desktop, (or Putty / SSH) and access your host as you have before.

\*\*\*\*Note: IPs are often dynamic, sometimes changing from day to day, so if
you attempt RDP/SSH and cannot connect, you may need to update the IP list with
your new/current IP.
