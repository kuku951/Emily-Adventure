# Emily-Adventure
It's a racing-car and adventure game based on Unity
使用軟體 Unity
使用程式語言 C#

## 遊戲簡介
在距離地球遙遠的碰瓷城市，生活著一位叫艾蜜莉的同學，在這座城市裡面還有著五位賽車訓練員，分別是碰瓷葛格、APPLE 、ARISA 、ERIKA以及KEVIN，艾蜜莉必須要透過幫助這五位訓練員完成任務、才能夠學習到駕駛賽車的技巧以致於通過最後的賽車關卡，快進入遊戲來幫助艾蜜莉吧!  
![image](https://user-images.githubusercontent.com/63222978/136793409-e7c03197-8528-4d76-ab8c-7e44678f85d3.png)
## 遊戲玩法
###### 碰瓷世界:
本遊戲一開始會先進入碰瓷世界中，碰瓷葛格會先與玩家對話，主角的移動方式是使用上下左右鍵(前進後退轉向)，在碰瓷世界中，必須完成每位NPC所請求的任務，而NPC就會教玩家賽車的技巧，最後再讓玩家去到碰瓷越野拉力賽在倒數計時的時間內完成賽道。
###### 碰瓷越野拉力賽:
在進入到碰瓷越野拉力賽後，會倒數計時兩分鐘，必須在兩分鐘內完成賽道，賽車的控制為:上下左右以及空白鍵(小剎車)，然後再一定速度的情況下把上鍵放開，用左右鍵去控制時會有拖飄的效果，如果要離開畫面必須按Esc鍵會跳出選單。
## 碰瓷世界工作流程圖
![1](https://user-images.githubusercontent.com/63222978/136793673-39b94583-c609-4278-be15-95119b4bc7a9.jpg)
## 碰瓷賽車工作流程圖
![2](https://user-images.githubusercontent.com/63222978/136793723-d8a8e3af-890a-407d-8265-f4b15ca978e1.jpg)
## 人物點擊對話
在人物上多建造一個click sprite再使用fungus->object click->say or menu點擊產生選單或對話框  
![image](https://user-images.githubusercontent.com/63222978/136793859-15a384f2-5f61-4697-b9d3-a9f35882051b.png)
![image](https://user-images.githubusercontent.com/63222978/136793873-0eebce73-cd06-44fd-970e-76640dbde293.png)
![image](https://user-images.githubusercontent.com/63222978/136793878-7a0a7163-5499-42c9-84bd-540070e0bb43.png)
## Menu點擊換場景
使用fungus->menu->load Scene點擊選單內容更換場景(必須先將場景加入scene in build裡面)  
![image](https://user-images.githubusercontent.com/63222978/136793959-e9f6e149-db66-4450-9ca6-b10315424f10.png)
## 小地圖建造
建造Canvas image預設UI mask不要讓圖跑出來再用fungus keypress->Set UI image讓人物按tab顯示小地圖，按0關閉小地圖  
![image](https://user-images.githubusercontent.com/63222978/136794024-1bd7141d-38d7-453a-9e04-d63310f4d08d.png)
![image](https://user-images.githubusercontent.com/63222978/136794033-347a60b4-9d9c-45a2-a2fb-513195a7cb75.png)
## 音樂播放
使用fungus->gamestarted->play music讓遊戲開始時撥放  
![image](https://user-images.githubusercontent.com/63222978/136794092-3008736e-1dda-4f9f-94e8-77d9d545f793.png)
## 賽車參數調整
使用Standard Assets 中的賽車之後更改參數包含大小(0.3)，steer helper(0)如果有設數字的時候都會常常卡牆，angular drag(5)角度阻力避免轉彎過快，drag(0.5)空氣阻力 因為車體變小空氣阻力也縮小，brake torque(20000)避免煞車沒力道，max steer angle(25)調整轉彎角度，最大速度改為150  
![image](https://user-images.githubusercontent.com/63222978/136794168-51247643-4a8a-42f2-b6bb-9866739ab6bf.png)
![image](https://user-images.githubusercontent.com/63222978/136794180-7b96086c-1f44-4e0e-a015-660c85a58649.png)
## 倒數計時器
使用兩個腳本來控制第一個控制3 2 1 start(start結束後前者會消失) 變成第二個控制倒數計時時間  
![image](https://user-images.githubusercontent.com/63222978/136794238-e4893e81-4ffa-4af9-b612-da8242ee3837.png)
![image](https://user-images.githubusercontent.com/63222978/136794245-64944702-640a-4913-93ae-2f7e1ae5d272.png)
## 倒數計時器code
使用兩個腳本來控制第一個控制3 2 1 start(start結束後前者會消失) 變成第二個控制倒數計時時間  
![image](https://user-images.githubusercontent.com/63222978/136794292-1016343c-d26e-4948-a724-e39ca684690d.png)
![image](https://user-images.githubusercontent.com/63222978/136794302-d513b31f-db38-4a44-b70e-113bf1bdd091.png)
## 越過終點線產生選單
再cube (隱藏)中使用fungus->trigger->menu越過終點線產生選單以及對話框  
![image](https://user-images.githubusercontent.com/63222978/136794342-8849994b-5a35-4059-9558-d15c5b53e2ce.png)
![image](https://user-images.githubusercontent.com/63222978/136794349-a34d1ac8-e328-4dfb-9dfd-10be59e182df.png)
![image](https://user-images.githubusercontent.com/63222978/136794362-dad9f964-cc1b-4fc6-89d8-505213e1e1f3.png)
## 配合螢幕位置輸出字樣位置
再Canvas中把scaler的UI Scale Mode調整成scale with screen size。
![image](https://user-images.githubusercontent.com/63222978/136794558-59b0edd5-14cd-4a76-acc7-582dcc0c7490.png)
























