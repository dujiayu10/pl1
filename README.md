# pl1
def ask_player(lists):
    i = 0
    while i < 3:
        count = 0
        while count < 3:
            temp = []
            print(lists[count])
            answer = input("上面面是否有你选的数字（y/n）：")
            if answer == 'y':
                if count == 0:
                    temp.append(lists[count + 1])
                    temp.append(lists[count])
                    temp.append(lists[count + 2])
                elif count == 1:
                    temp.append(lists[count - 1])
                    temp.append(lists[count])
                    temp.append(lists[count + 1])
                elif count == 2:
                    temp.append(lists[count - 2])
                    temp.append(lists[count])
                    temp.append(lists[count - 1])
                # 重新发牌
                shuffle_card(temp, lists)
                break
            count += 1
        i += 1
