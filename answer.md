# 第2次練習題目-隨堂-QZ2
>
>學號：113111117 
><br />
>姓名：官益正
><br />
>作業撰寫時間：180 (mins，包含程式撰寫時間，換成自己的)
><br />
>最後撰寫文件日期：2026/10/29 (換成自己的)
>

1. (需截圖說明，並且需截圖執行結果)

Ans:
程式碼：

using UnityEngine;                  // 引用 Unity 的基本功能
using UnityEngine.InputSystem;       // 引用新版輸入系統

// 建立名為 PlayerController 的玩家控制器類別
// MonoBehaviour 讓這個類別可以作為 Unity 遊戲物件的元件
public class PlayerController : MonoBehaviour
{
    // Update() 在遊戲執行期間會持續被 Unity 呼叫
    void Update()
    {
        // 取得目前的鍵盤裝置，並存入 keyboard 變數
        Keyboard keyboard = Keyboard.current;

        // 確認鍵盤存在，而且玩家在這一幀剛按下 W 鍵
        if (keyboard != null && keyboard.wKey.wasPressedThisFrame)
        {
            // 在 Unity Console 印出玩家按下 W 鍵的訊息
            Debug.Log("玩家按了 W 鍵！");
        }
    }
}

![有人按了w](image.png)


2. (需截圖說明，並且需截圖執行結果)

Ans:
程式碼：

using UnityEngine;                  // 引用 Unity 基本功能，例如 Debug.Log()
using UnityEngine.InputSystem;       // 引用新版輸入系統，用來接收鍵盤輸入

// 建立 PlayerController 類別，繼承 MonoBehaviour
// 讓這個腳本可以掛在 Unity 的遊戲物件上
public class PlayerController : MonoBehaviour
{
    // Start() 是 Unity 的生命週期函式
    // 遊戲物件啟用後，在第一次執行 Update() 前呼叫一次
    void Start()
    {
        // 目前不需要在遊戲開始時執行其他程式
    }

    // Update() 在遊戲執行期間每一幀都會執行
    // 用來持續檢查玩家是否按下鍵盤按鍵
    void Update()
    {
        // 取得目前的鍵盤裝置，並存入 keyboard 變數
        Keyboard keyboard = Keyboard.current;

        // 如果目前沒有可用的鍵盤，就結束這次 Update()
        if (keyboard == null)
        {
            return;
        }

        // ---------- 偵測 W 鍵 ----------
        // wKey 代表鍵盤上的 W 鍵
        // isPressed 用來判斷 W 鍵目前是否處於按下狀態
        if (keyboard.wKey.isPressed)
        {
            // 當 W 鍵被按住時，在 Console 印出訊息
            Debug.Log("玩家按了 W 鍵！");
        }

        // ---------- 偵測 A 鍵 ----------
        // aKey 代表鍵盤上的 A 鍵
        // isPressed 用來判斷 A 鍵目前是否處於按下狀態
        if (keyboard.aKey.isPressed)
        {
            // 當 A 鍵被按住時，在 Console 印出訊息
            Debug.Log("玩家按了 A 鍵！");
        }

        // ---------- 偵測 S 鍵 ----------
        // sKey 代表鍵盤上的 S 鍵
        // isPressed 用來判斷 S 鍵目前是否處於按下狀態
        if (keyboard.sKey.isPressed)
        {
            // 當 S 鍵被按住時，在 Console 印出訊息
            Debug.Log("玩家按了 S 鍵！");
        }

        // ---------- 偵測 D 鍵 ----------
        // dKey 代表鍵盤上的 D 鍵
        // isPressed 用來判斷 D 鍵目前是否處於按下狀態
        if (keyboard.dKey.isPressed)
        {
            // 當 D 鍵被按住時，在 Console 印出訊息
            Debug.Log("玩家按了 D 鍵！");
        }
    }
}

![有人按了s](image-1.png)
![有人按了a](image-2.png)
![有人按了d](image-3.png)


## 其他

心得：為甚麼unity開c#那麼難開，我沒有買課本，所以網路上找要怎麼開。