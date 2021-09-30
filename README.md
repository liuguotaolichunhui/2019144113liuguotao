# 2019144113liuguotao
#coding:gb2312
#coding
import smtplib
from email.mime.text import MIMEText
msg_from='2026995734qq.com'
passwd='eostowolbqcheehg'
msg_to='57820048@qq.com'

subject="2019144113liuguotao.TEST"
cont:UTF-8ent="Campus network(Public)ip:220.164.161.127    (individual)ip:10.101.68.65    Mobile network(Public)ip:172.69.22.118  (individual)ip:10.104.9.176"
msg=MIMEText(content)
msg['Subjest']=subject
msg['From']=msg_from
msg['To']=msg_to
try:
    s=smtplib.SMTP_SSL("smtp.qq.com",465)
    s.login(msg_from,passwd)
    s.sendmail(msg_from,msg_to,msg.as_string())
    print("bingo")
except(s.SMTPException,e):
    print("ohh no!")
finally:
    s.quit()
