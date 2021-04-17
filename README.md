import amino,random,time,os
from gtts import gTTS

device=input("hallo give me your \nparallel space device id : ")
	
ff='{\\"device_id\\": \\"'+device+'\\", \\"device_id_sig\\": \\"AaauX/ZA2gM3ozqk1U5j6ek89SMu\\", \\"user_agent\\": \\"Dalvik/2.1.0 (Linux; U; Android 7.1; LG-UK495 Build/MRA58K; com.narvii.amino.master/3.3.33180)\\"}'
os.system("printf \""+ff+"\">device.json")
clint=amino.Client()
clint.login(email=input('\003[1;32mEnter Email  ⟩⟩⟩⟩  '),password=input('\003[1;32mEnter Password  ⟩⟩⟩⟩  '))
os.system('clear')
	
print ("Done Loggining")

u=clint.get_from_code('http://aminoapps.com/p/2ww994')

sub=amino.SubClient(comId=u.path[1:u.path.index('/')],profile=clint.profile)
clint.join_community(comId=u.path[1:u.path.index('/')])
sub.join_chat(chatId=u.objectId)
sub.send_message(chatId=u.objectId,message='تم تفعيل البوت')
sp1="منيوك"
sp2="انعل"
sp3="امك"
sp4="طيز"
sp5="كحبه"
sp6="اشك"
sp7="عاهر"
sp8="نيك"
sp9="اذبحك"
sp10="اهكرك"
sp11="انا هكر"
sp12="ابوك"
sp13="منيوك"
sp14="انعل"
sp15="امك"
sp16="طيز"
sp17="كحبه"
sp18="اشك"
sp19="عاهر"
sp20="نيك"
sp21="اذبحك"
sp22="اهكرك"
sp23="انا هكر"
sp24="ابوك"
sp25="طيز"
sp26="كحبه"
sp27="اشك"
sp28="عاهر"
sp29="نيك"
sp30="اذبحك"
@clint.event("on_text_message")
def on_text_message(data):
	content = data.message.content 
	if content.startswith("!ping"):
		clint.start_vc(comId=u.path[1:u.path.index('/')],chatId=data.message.chatId)
	if content.startswith('!global'):
		xx=content
		xx=xx.split('ht')[1]
		xx=clint.get_from_code('ht'+xx).objectId
		sub.send_message(chatId=data.message.chatId,message='Ndc://g/user-profile/'+xx)
	if content.startswith('!message'):
		sub.send_message(message=content.replace('!message',''),chatId=data.message.chatId)
	if content.startswith("!prank"):
		sub.send_coins(transactionId=clint.get_wallet_history(start=0,size=1).transanctionId[0],chatId=data.message.chatId,coins=500)
	if content.startswith('!private'):
		try:
			sub.start_chat(userId=data.message.author.userId,message='لقد قمت بطلب المساعده الرجاء الانتظار الى ان ياتي المالك')
		except:
			sub.send_message(message='حدث خطأ يبدو انك قمت باغلاق الدردشة الخاصه',chatId=data.message.chatId)
	if content.startswith('!report'):
		sub.start_chat(userId=data.message.author.userId,message='لقد اردت الابلاغ عن احد ما تفضل وقم بالابلاغ')
	if 'سب' in content:
		sub.send_message(chatId=data.message.chatId,message='يرجى ايعاز بلاغك ببعض الصور الى قدوم المالك')
	if 'http' in content and not content.startswith('!'):
		try:
			sub.delete_message(chatId=data.message.chatId,messageId=data.message.messageId)
			sub.kick(chatId=data.message.chatId,userId=data.message.author.userId,allowRejoin=True)
			sub.send_message(chatId=data.message.chatId,message='يمنع ارسال روابط',mentionUserIds=data.message.author.userId)
		except:
			pass
	if '!math' in content:
		list=[1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23]
		list1=['*','/','+','-']
		c1=random.choice(list)
		c2=random.choice(list1)
		c3=random.choice(list)
		c4=random.choice(list1)
		c5=random.choice(list)
		c6=str(c1)+str(c2)+str(c3)+str(c4)+str(5)
		sub.send_message(chatId=data.message.chatId,message=c6)
	if 'كس' in content:
		sub.delete_message(chatId=data.message.chatId,messageId=data.message.messageId)
		sub.kick(chatId=data.message.chatId,userId=data.message.author.userId)
	if sp1 in content:
		sub.delete_message(chatId=data.message.chatId,messageId=data.message.messageId)
		sub.kick(chatId=data.message.chatId,userId=data.message.author.userId)
	if sp2 in content:
		sub.delete_message(chatId=data.message.chatId,messageId=data.message.messageId)
		sub.kick(chatId=data.message.chatId,userId=data.message.author.userId)
	if sp3 in content:
		sub.delete_message(chatId=data.message.chatId,messageId=data.message.messageId)
		sub.kick(chatId=data.message.chatId,userId=data.message.author.userId)
	if sp4 in content:
		sub.delete_message(chatId=data.message.chatId,messageId=data.message.messageId)
		sub.kick(chatId=data.message.chatId,userId=data.message.author.userId)
	if sp5 in content:
		sub.delete_message(chatId=data.message.chatId,messageId=data.message.messageId)
		sub.kick(chatId=data.message.chatId,userId=data.message.author.userId)
	if sp6 in content:
		sub.delete_message(chatId=data.message.chatId,messageId=data.message.messageId)
		sub.kick(chatId=data.message.chatId,userId=data.message.author.userId)
	if sp7 in content:
		sub.delete_message(chatId=data.message.chatId,messageId=data.message.messageId)
		sub.kick(chatId=data.message.chatId,userId=data.message.author.userId)
	if sp8 in content:
		sub.delete_message(chatId=data.message.chatId,messageId=data.message.messageId)
		sub.kick(chatId=data.message.chatId,userId=data.message.author.userId)
	if sp9 in content:
		sub.delete_message(chatId=data.message.chatId,messageId=data.message.messageId)
		sub.kick(chatId=data.message.chatId,userId=data.message.author.userId)
	if sp10 in content:
		sub.delete_message(chatId=data.message.chatId,messageId=data.message.messageId)
		sub.kick(chatId=data.message.chatId,userId=data.message.author.userId)
	if sp11 in content:
		sub.delete_message(chatId=data.message.chatId,messageId=data.message.messageId)
		sub.kick(chatId=data.message.chatId,userId=data.message.author.userId)
	if sp12 in content:
		sub.delete_message(chatId=data.message.chatId,messageId=data.message.messageId)
		sub.kick(chatId=data.message.chatId,userId=data.message.author.userId)
		if sp13 in content:
			sub.delete_message(chatId=data.message.chatId,messageId=data.message.messageId)
		sub.kick(chatId=data.message.chatId,userId=data.message.author.userId)
	if sp14 in content:
		sub.delete_message(chatId=data.message.chatId,messageId=data.message.messageId)
		sub.kick(chatId=data.message.chatId,userId=data.message.author.userId)
	if sp15 in content:
		sub.delete_message(chatId=data.message.chatId,messageId=data.message.messageId)
		sub.kick(chatId=data.message.chatId,userId=data.message.author.userId)
	if sp16 in content:
		sub.delete_message(chatId=data.message.chatId,messageId=data.message.messageId)
		sub.kick(chatId=data.message.chatId,userId=data.message.author.userId)
	if sp17 in content:
		sub.delete_message(chatId=data.message.chatId,messageId=data.message.messageId)
		sub.kick(chatId=data.message.chatId,userId=data.message.author.userId)
	if sp18 in content:
		sub.delete_message(chatId=data.message.chatId,messageId=data.message.messageId)
		sub.kick(chatId=data.message.chatId,userId=data.message.author.userId)
	if sp19 in content:
		sub.delete_message(chatId=data.message.chatId,messageId=data.message.messageId)
		sub.kick(chatId=data.message.chatId,userId=data.message.author.userId)
	if sp20 in content:
		sub.delete_message(chatId=data.message.chatId,messageId=data.message.messageId)
		sub.kick(chatId=data.message.chatId,userId=data.message.author.userId)
	if sp21 in content:
		sub.delete_message(chatId=data.message.chatId,messageId=data.message.messageId)
		sub.kick(chatId=data.message.chatId,userId=data.message.author.userId)
	if sp22 in content:
		sub.delete_message(chatId=data.message.chatId,messageId=data.message.messageId)
		sub.kick(chatId=data.message.chatId,userId=data.message.author.userId)
	if sp23 in content:
		sub.delete_message(chatId=data.message.chatId,messageId=data.message.messageId)
		sub.kick(chatId=data.message.chatId,userId=data.message.author.userId)
	if sp24 in content:
		sub.delete_message(chatId=data.message.chatId,messageId=data.message.messageId)
		sub.kick(chatId=data.message.chatId,userId=data.message.author.userId)
	if sp25 in content:
		sub.delete_message(chatId=data.message.chatId,messageId=data.message.messageId)
		sub.kick(chatId=data.message.chatId,userId=data.message.author.userId)
	if sp26 in content:
		sub.delete_message(chatId=data.message.chatId,messageId=data.message.messageId)
		sub.kick(chatId=data.message.chatId,userId=data.message.author.userId)
	if sp27 in content:
		sub.delete_message(chatId=data.message.chatId,messageId=data.message.messageId)
		sub.kick(chatId=data.message.chatId,userId=data.message.author.userId)
	if sp28 in content:
		sub.delete_message(chatId=data.message.chatId,messageId=data.message.messageId)
		sub.kick(chatId=data.message.chatId,userId=data.message.author.userId)
	if sp29 in content:
		sub.delete_message(chatId=data.message.chatId,messageId=data.message.messageId)
		sub.kick(chatId=data.message.chatId,userId=data.message.author.userId)
	if sp30 in content:
		sub.delete_message(chatId=data.message.chatId,messageId=data.message.messageId)
		sub.kick(chatId=data.message.chatId,userId=data.message.author.userId)
	if content == "حجرة":
		list2=["حجره","ورقه","مقص"]
		cc=random.choice(list2)
		sub.send_message(chatId=data.message.chatId,message='اخترت\n'+cc,replyTo=data.message.messageId)
	if content == "حجره":
		list2=["حجره","ورقه","مقص"]
		cc=random.choice(list2)
		sub.send_message(chatId=data.message.chatId,message='اخترت\n'+cc,replyTo=data.message.messageId)
	if content == "مقص":
		list2=["حجره","ورقه","مقص"]
		cc=random.choice(list2)
		sub.send_message(chatId=data.message.chatId,message='اخترت\n'+cc,replyTo=data.message.messageId)
	if content=="ورقه" :
		list2=["حجره","ورقه","مقص"]
		cc=random.choice(list2)
		sub.send_message(chatId=data.message.chatId,message='اخترت\n'+cc,replyTo=data.message.messageId)
	if content=="ورقة" :
		list2=["حجره","ورقه","مقص"]
		cc=random.choice(list2)
		sub.send_message(chatId=data.message.chatId,message='اخترت\n'+cc,replyTo=data.message.messageId)
	if content.startswith("!tell"):
		texxxt=content.replace('!tell','')
		lan="ar"
		name="sssss.mp3"
		gTTS(text=texxxt,lang=lan,slow=False).save(name)
		with open(name,"rb") as fff:
			sub.send_message(chatId=data.message.chatId,file=fff,fileType="audio")
			os.remove(name)
	if "!help" in content:
		xxxxx='''
[C]اهلا بك لقد طلبت المساعده سوف اقوم باعطائك الاوامر
[C]يجب وضع ( ! ) قبل كل أمر
[C]كمثال ( !hi )
[C]تنويه الرجاء استبدال ( - ) بـ( ! )
[CU]ما هي أوامر البوت
[C]- global : يقوم بإحضار رابط امينو لشخص
[C]- ping : يقوم بفتح محادثه صوتيه
[C]- message : يرسل رسالة بما تريد
[C]- tell : يرسل رسالة صوتيه بما تريد
[C]- private : لياتي إلى الدردشة الخاصه
[C]- report : لياتي إلى الدردشة الخاصه أيضا ويستلم بلاغك
[C]- prank : يقوم بمزحه صغيره
[C]- math : مسأله رياضيه
[C]اوامر بدون ( ! )
[C]تنويه ؛ الرجاء استبدال - بلا شيء
[C]- حجره
[C]- حجرة
[C]- ورقة
[C]- ورقة
[C]- مقص'''
		sub.send_message(chatId=data.message.chatId,message=xxxxx)
@clint.event("on_group_member_join")
def on_group_member_join(data):
	sub.send_message(chatId=data.message.chatId,message="انرتنا")
@clint.event("on_group_member_leave")
def on_group_member_leave(data):
	sub.send_message(chatId=data.message.chatId,message="الى اللقاء")
@clint.event("on_chat_tip")
def on_chat_tip(data):
	sub.send_message(chatId=data.message.chatId,message="شكرا لك على التبرع")
