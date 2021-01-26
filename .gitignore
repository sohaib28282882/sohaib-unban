import amino
client=amino.Client()

email=input ("Email: ")
password=input("Password: ")
client.login(email=email ,password=password)
print ("Done Loggining")

chatlink=input("A Chat Link From The Community: ")
chatinfo=client.get_from_code(chatlink)
chatId=chatinfo.objectId
comId=chatinfo.path[1:chatinfo.path.index('/')]
print (chatId)
print (comId)
subclient=amino.SubClient(comId=comId, profile=client.profile)

while True:
    usersId=subclient.get_all_users(type="banned", start=0, size=9000)
    user=usersId.profile.userId
    for userId in user:
        try:
            subclient.unban(userId=userId, reason="اللهم صلي وسلم على سيدنا محمد")
            print ("Done")
        except:
            pass
            print ("Faild")
