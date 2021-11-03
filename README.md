#只需要把MailSystem类导入即可
from mail_system import MailSystem

mailSever = MailSystem()

yourName = "Your Name

recipientName = "Ricipitor Name"

recipientMailAddress = "Ricipitor Mail"

mailTitle = "2021年11月03日 通知公告(测试)"

mailContent = f"""

<p>{recipientName},你好:</p>

<p style="text-indent:2em;">你关注的网站已经更新，请及时查看。</p>
"""

mailSever.createMail(mailTitle,mailContent)

mailSever.addSendInfo(yourName,recipientName,recipientMailAddress)

mailSever.sendMail()
