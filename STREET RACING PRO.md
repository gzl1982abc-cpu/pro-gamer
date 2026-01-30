# STREET RACING PRO - 產品需求文檔 (PRD)

## 一、專案概述
- **專案名稱**：STREET RACING PRO
- **一句話描述**：一款具有技能系統、多樣化障礙物和炫酷特效的HTML5街頭賽車遊戲
- **版本**：1.0

## 二、問題與目標

### 問題陳述
傳統的網頁賽車遊戲缺乏深度的技能系統和視覺特效，導致遊戲體驗單調，玩家留存率低。需要一款結合策略性技能使用、豐富視覺效果和挑戰性關卡設計的現代化賽車遊戲。

### 目標
- 創造一款具有深度技能系統的賽車遊戲
- 提供流暢的遊戲體驗和炫酷的視覺特效
- 實現多樣化的障礙物和遊戲機制
- 確保跨平台兼容性（桌面和移動設備）

## 三、目標用戶

### 用戶特徵
- 年齡：12-35歲
- 喜歡休閒競速遊戲
- 有一定遊戲經驗，熟悉觸屏/鍵盤操作
- 喜歡具有挑戰性和成就感的遊戲
- 偏好視覺效果豐富的遊戲體驗

### 用戶需求
1. 需要簡單直觀的操作方式
2. 希望有明確的技能按鈕和反饋
3. 期望清晰的障礙物識別和躲避機制
4. 追求高分和成就系統
5. 喜歡炫酷的視覺特效和動畫

## 四、用戶故事

- **用戶故事1**：作為一名休閒玩家，我想要使用明確的技能按鈕來釋放特殊技能，以便在緊急情況下躲避障礙物或加速超越對手。

- **用戶故事2**：作為一名競技玩家，我想要收集金币和道具來提升我的遊戲表現，以便獲得更高的分數和排名。

- **用戶故事3**：作為一名視覺愛好者，我想要體驗炫酷的粒子特效和爆炸動畫，以便享受沉浸式的遊戲體驗。

- **用戶故事4**：作為一名移動端玩家，我想要使用觸屏按鈕來控制賽車，以便在手機上也能流暢遊玩。

- **用戶故事5**：作為一名成就追求者，我想要看到我的最高分和最高速度統計，以便挑戰自我和分享成就。

## 五、功能需求與驗收標準

### 功能1：玩家控制系統
- **描述**：玩家可以通過鍵盤或觸屏按鈕控制賽車左右移動和加速
- **驗收標準**：
  - Given 玩家在遊戲中
  - When 按下左方向鍵或左側觸屏按鈕
  - Then 賽車應向左移動並略微傾斜
  
  - Given 玩家在遊戲中
  - When 按下右方向鍵或右側觸屏按鈕
  - Then 賽車應向右移動並略微傾斜
  
  - Given 玩家在遊戲中
  - When 按下空格鍵或持續按住加速
  - Then 賽車應加速前進

### 功能2：技能系統
- **描述**：玩家可以使用三種特殊技能：氮氣加速、能量護盾、超級飄移
- **驗收標準**：
  - Given 玩家的氮氣槽充能達到30%以上且技能不在冷卻中
  - When 點擊NITRO技能按鈕或按下1鍵
  - Then 賽車速度提升80%，持續3秒，並產生藍色粒子特效
  
  - Given 玩家的護盾技能不在冷卻中
  - When 點擊SHIELD技能按鈕或按下2鍵
  - Then 賽車獲得5秒無敵狀態，碰撞時產生爆炸特效
  
  - Given 玩家的飄移技能不在冷卻中
  - When 點擊DRIFT技能按鈕或按下3鍵
  - Then 賽車轉向速度提升80%，持續3秒

### 功能3：障礙物系統
- **描述**：遊戲中會隨機生成四種不同類型的障礙物
- **驗收標準**：
  - Given 遊戲進行中
  - When 障礙物進入屏幕
  - Then 應顯示清晰的車輛形象（普通轎車、卡車、警車、摩托車）
  
  - Given 玩家賽車與障礙物發生碰撞
  - When 玩家沒有激活護盾
  - Then 遊戲應結束並顯示遊戲結束界面
  
  - Given 玩家賽車與障礙物發生碰撞
  - When 玩家激活了護盾
  - Then 障礙物應被摧毀，玩家獲得200分，護盾消失

### 功能4：收集系統
- **描述**：玩家可以收集金币和特殊道具
- **驗收標準**：
  - Given 金币出現在道路上
  - When 玩家賽車觸碰到金币
  - Then 金币消失，玩家獲得100分，氮氣槽增加3%
  
  - Given 氮氣道具出現在道路上
  - When 玩家賽車觸碰到氮氣道具
  - Then 道具消失，玩家氮氣槽增加40%
  
  - Given 護盾道具出現在道路上
  - When 玩家賽車觸碰到護盾道具
  - Then 道具消失，玩家立即激活5秒護盾

### 功能5：視覺特效系統
- **描述**：遊戲包含多種視覺特效增強體驗
- **驗收標準**：
  - Given 玩家激活氮氣加速
  - When 技能生效時
  - Then 應產生藍色粒子特效從車尾噴射
  
  - Given 玩家碰撞障礙物（有護盾）
  - When 碰撞發生時
  - Then 應產生爆炸特效和碎片
  
  - Given 玩家收集道具或金币
  - When 收集成功時
  - Then 應產生對應顏色的粒子收集特效

### 功能6：統計與UI系統
- **描述**：實時顯示遊戲統計信息
- **驗收標準**：
  - Given 遊戲進行中
  - When 玩家移動時
  - Then 頂部應實時顯示當前分數和速度
  
  - Given 遊戲進行中
  - When 氮氣槽充能時
  - Then 底部氮氣槽應實時更新充能進度
  
  - Given 遊戲結束
  - When 顯示遊戲結束界面
  - Then 應顯示最終分數和最高速度記錄

## 六、技術約束

### 必須遵守
- 使用純HTML5、CSS3、JavaScript（無外部框架）
- 所有資源內嵌，無外部依賴
- 代碼結構清晰，模塊化設計
- 性能優化，確保60FPS流暢運行

### 兼容性要求
- 支持現代瀏覽器（Chrome, Firefox, Safari, Edge）
- 支持桌面端（鍵盤控制）
- 支持移動端（觸屏控制）
- 響應式設計，適配不同屏幕尺寸

### 不要做
- 不要使用Flash或其他已淘汰技術
- 不要依賴外部API或服務
- 不要包含音頻（除非用戶後續要求）
- 不要使用過於複雜的物理引擎

## 七、現有代碼
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>STREET RACING PRO</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            background: linear-gradient(135deg, #1a1a2e, #16213e);
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            overflow: hidden;
            color: white;
        }

        .game-container {
            position: relative;
            width: 480px;
            height: 760px;
            overflow: hidden;
            border-radius: 20px;
            box-shadow: 0 0 40px rgba(0, 206, 209, 0.7);
            background: rgba(15, 15, 30, 0.95);
            border: 3px solid rgba(100, 200, 255, 0.3);
        }

        .road {
            position: absolute;
            width: 100%;
            height: 100%;
            background: linear-gradient(to bottom, #2c2c4a 0%, #1a1a2e 100%);
            overflow: hidden;
        }

        .road-markings {
            position: absolute;
            width: 100%;
            height: 100%;
        }

        .road-marking {
            position: absolute;
            width: 12px;
            height: 60px;
            background: linear-gradient(to bottom, rgba(255, 255, 255, 0.9), rgba(255, 255, 255, 0.3));
            left: 50%;
            transform: translateX(-50%);
            border-radius: 3px;
            box-shadow: 0 0 10px rgba(255, 255, 255, 0.6);
        }

        .side-line {
            position: absolute;
            width: 6px;
            height: 100%;
            background: linear-gradient(to bottom, rgba(100, 200, 255, 0.7), rgba(100, 200, 255, 0.3));
            box-shadow: 0 0 15px rgba(100, 200, 255, 0.5);
        }

        .side-line.left {
            left: 40px;
        }

        .side-line.right {
            right: 40px;
        }

        .player-car {
            position: absolute;
            width: 60px;
            height: 100px;
            background: linear-gradient(135deg, #ff4d94, #ff1a75);
            border-radius: 15px 15px 10px 10px;
            bottom: 150px;
            left: 50%;
            transform: translateX(-50%);
            box-shadow: 
                0 0 30px rgba(255, 26, 117, 0.8),
                inset 0 0 15px rgba(255, 255, 255, 0.2);
            z-index: 100;
            transition: transform 0.1s ease;
        }

        .car-window {
            position: absolute;
            width: 40px;
            height: 25px;
            background: linear-gradient(135deg, #0a0a1a, #1a1a2e);
            top: 15px;
            left: 50%;
            transform: translateX(-50%);
            border-radius: 5px 5px 0 0;
            border: 2px solid rgba(255, 255, 255, 0.1);
        }

        .car-light {
            position: absolute;
            width: 10px;
            height: 12px;
            background: linear-gradient(135deg, #ffeb3b, #ffc107);
            bottom: 8px;
            border-radius: 2px;
            box-shadow: 0 0 15px #ffeb3b;
        }

        .car-light.left {
            left: 12px;
        }

        .car-light.right {
            right: 12px;
        }

        .car-exhaust {
            position: absolute;
            width: 12px;
            height: 8px;
            background: linear-gradient(135deg, #ff5252, #ff1744);
            bottom: -3px;
            left: 50%;
            transform: translateX(-50%);
            border-radius: 3px;
            box-shadow: 0 0 15px rgba(255, 26, 26, 0.8);
        }

        /* 重新设计障碍物 - 更清晰的车辆形象 */
        .obstacle {
            position: absolute;
            border-radius: 12px;
            z-index: 50;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.5);
            overflow: hidden;
        }

        .obstacle-car {
            width: 50px;
            height: 80px;
            background: linear-gradient(135deg, #3498db, #2980b9);
            display: flex;
            flex-direction: column;
        }

        .obstacle-car-top {
            height: 30px;
            background: linear-gradient(135deg, #2c3e50, #1a1a2e);
        }

        .obstacle-car-bottom {
            height: 50px;
            background: linear-gradient(135deg, #3498db, #2980b9);
        }

        .obstacle-truck {
            width: 70px;
            height: 90px;
            background: linear-gradient(135deg, #2ecc71, #27ae60);
            display: flex;
            flex-direction: column;
        }

        .obstacle-truck-cab {
            height: 40px;
            background: linear-gradient(135deg, #27ae60, #219653);
        }

        .obstacle-truck-body {
            height: 50px;
            background: linear-gradient(135deg, #2ecc71, #27ae60);
        }

        .obstacle-police {
            width: 55px;
            height: 85px;
            background: linear-gradient(135deg, #9b59b6, #8e44ad);
            display: flex;
            flex-direction: column;
        }

        .obstacle-police-top {
            height: 35px;
            background: linear-gradient(135deg, #8e44ad, #7d3c98);
        }

        .obstacle-police-bottom {
            height: 50px;
            background: linear-gradient(135deg, #9b59b6, #8e44ad);
            position: relative;
        }

        .police-light {
            position: absolute;
            top: 5px;
            left: 50%;
            transform: translateX(-50%);
            width: 30px;
            height: 10px;
            background: linear-gradient(90deg, #ff5252, #ffeb3b, #2196f3);
            border-radius: 5px;
            animation: policeLight 0.5s infinite alternate;
        }

        .obstacle-motorcycle {
            width: 30px;
            height: 60px;
            background: linear-gradient(135deg, #e74c3c, #c0392b);
            display: flex;
            flex-direction: column;
        }

        .motorcycle-seat {
            height: 20px;
            background: linear-gradient(135deg, #c0392b, #a93226);
        }

        .motorcycle-body {
            height: 40px;
            background: linear-gradient(135deg, #e74c3c, #c0392b);
        }

        .coin {
            position: absolute;
            width: 25px;
            height: 25px;
            background: radial-gradient(circle, #ffd700, #ffaa00);
            border-radius: 50%;
            z-index: 40;
            box-shadow: 0 0 20px rgba(255, 215, 0, 0.8);
            animation: coinSpin 1s infinite linear;
        }

        .nitro-powerup {
            position: absolute;
            width: 35px;
            height: 35px;
            background: radial-gradient(circle, #00ffff, #00bfff);
            border-radius: 50%;
            z-index: 40;
            box-shadow: 0 0 25px rgba(0, 255, 255, 0.9);
            animation: pulse 1.5s infinite alternate;
        }

        .shield-powerup {
            position: absolute;
            width: 35px;
            height: 35px;
            background: radial-gradient(circle, #4caf50, #2e7d32);
            border-radius: 50%;
            z-index: 40;
            box-shadow: 0 0 25px rgba(76, 175, 80, 0.9);
            animation: shieldPulse 2s infinite alternate;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .shield-powerup::before {
            content: '';
            position: absolute;
            width: 25px;
            height: 25px;
            background: rgba(255, 255, 255, 0.8);
            border-radius: 50%;
        }

        .particle {
            position: absolute;
            width: 8px;
            height: 8px;
            border-radius: 50%;
            z-index: 200;
            pointer-events: none;
        }

        .explosion {
            position: absolute;
            width: 100px;
            height: 100px;
            background: radial-gradient(circle, #ff5252, #ff1744, transparent);
            border-radius: 50%;
            z-index: 300;
            opacity: 1;
            transform: scale(0);
            animation: explosion 0.5s forwards;
        }

        /* 顶部UI - 简洁设计 */
        .top-ui {
            position: absolute;
            top: 20px;
            left: 0;
            width: 100%;
            padding: 0 20px;
            z-index: 200;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .score-display {
            font-size: 24px;
            font-weight: bold;
            color: #ffeb3b;
            text-shadow: 0 0 10px rgba(255, 235, 59, 0.7);
            font-family: 'Courier New', monospace;
        }

        .speed-display {
            font-size: 20px;
            font-weight: bold;
            color: #00ffff;
            text-shadow: 0 0 10px rgba(0, 255, 255, 0.7);
        }

        /* 技能栏 - 底部固定，更加明确 */
        .skills-bar {
            position: absolute;
            bottom: 120px;
            left: 0;
            width: 100%;
            display: flex;
            justify-content: center;
            gap: 25px;
            z-index: 250;
            padding: 0 20px;
        }

        .skill-slot {
            position: relative;
            width: 70px;
            height: 70px;
            background: rgba(30, 30, 50, 0.8);
            border: 2px solid rgba(100, 200, 255, 0.5);
            border-radius: 18px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
        }

        .skill-slot:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.4);
            border-color: rgba(150, 220, 255, 0.8);
        }

        .skill-slot:active {
            transform: translateY(1px);
        }

        .skill-slot.inactive {
            opacity: 0.6;
            cursor: not-allowed;
        }

        .skill-icon {
            font-size: 28px;
            margin-bottom: 5px;
        }

        .skill-nitro .skill-icon { color: #00ffff; }
        .skill-shield .skill-icon { color: #4caf50; }
        .skill-drift .skill-icon { color: #ffeb3b; }

        .skill-name {
            font-size: 10px;
            font-weight: bold;
            color: #a0a0c0;
            text-align: center;
        }

        .skill-cooldown {
            position: absolute;
            bottom: 3px;
            left: 0;
            width: 100%;
            text-align: center;
            font-size: 12px;
            color: #ff5252;
            font-weight: bold;
            text-shadow: 0 0 5px rgba(255, 82, 82, 0.8);
        }

        .skill-charge {
            position: absolute;
            bottom: 0;
            left: 0;
            height: 4px;
            background: linear-gradient(90deg, #00ffff, #4caf50);
            border-radius: 0 0 16px 16px;
            transition: width 0.3s ease;
        }

        /* 氮气槽 - 重新设计位置 */
        .nitro-container {
            position: absolute;
            bottom: 80px;
            left: 20px;
            right: 20px;
            height: 25px;
            z-index: 200;
        }

        .nitro-bar-background {
            width: 100%;
            height: 100%;
            background: rgba(40, 40, 70, 0.8);
            border-radius: 12px;
            border: 2px solid rgba(100, 200, 255, 0.5);
            overflow: hidden;
            box-shadow: 0 0 10px rgba(0, 255, 255, 0.3);
        }

        .nitro-bar-fill {
            height: 100%;
            width: 0%;
            background: linear-gradient(90deg, #00ffff, #00bfff);
            border-radius: 10px;
            transition: width 0.3s ease;
            box-shadow: inset 0 0 15px rgba(0, 255, 255, 0.8);
        }

        /* 控制按钮 - 重新设计 */
        .controls {
            position: absolute;
            bottom: 20px;
            left: 0;
            width: 100%;
            display: flex;
            justify-content: space-around;
            z-index: 300;
            padding: 0 40px;
        }

        .control-btn {
            width: 70px;
            height: 70px;
            background: linear-gradient(135deg, #4a4a78, #3a3a60);
            border: 3px solid rgba(150, 220, 255, 0.7);
            border-radius: 20px;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 28px;
            font-weight: bold;
            color: white;
            cursor: pointer;
            user-select: none;
            transition: all 0.2s ease;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.4);
        }

        .control-btn:hover {
            background: linear-gradient(135deg, #5a5a88, #4a4a70);
            transform: translateY(-2px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.5);
        }

        .control-btn:active {
            transform: translateY(2px);
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.3);
        }

        /* 游戏结束界面 */
        .game-over {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(15, 15, 30, 0.95);
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            z-index: 300;
            display: none;
        }

        .game-over h1 {
            font-size: 48px;
            font-weight: bold;
            color: #ff1a75;
            text-shadow: 0 0 30px rgba(255, 26, 117, 0.8);
            margin-bottom: 20px;
            text-align: center;
        }

        .game-over-stats {
            display: flex;
            gap: 30px;
            margin: 20px 0;
        }

        .stat-box {
            text-align: center;
            padding: 15px 25px;
            background: rgba(40, 40, 70, 0.8);
            border-radius: 15px;
            border: 2px solid rgba(150, 220, 255, 0.5);
        }

        .stat-title {
            font-size: 16px;
            color: #a0a0c0;
            margin-bottom: 8px;
        }

        .stat-value {
            font-size: 28px;
            font-weight: bold;
            color: #ffeb3b;
            text-shadow: 0 0 10px rgba(255, 235, 59, 0.7);
        }

        .action-buttons {
            display: flex;
            gap: 20px;
            margin-top: 25px;
        }

        .action-btn {
            padding: 12px 30px;
            font-size: 18px;
            font-weight: bold;
            border: none;
            border-radius: 15px;
            cursor: pointer;
            transition: all 0.3s ease;
            background: linear-gradient(135deg, #4a4a78, #3a3a60);
            color: white;
            border: 2px solid rgba(150, 220, 255, 0.7);
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.3);
        }

        .action-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.4);
            background: linear-gradient(135deg, #5a5a88, #4a4a70);
        }

        .countdown {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            font-size: 80px;
            font-weight: bold;
            color: #ff1a75;
            text-shadow: 0 0 40px rgba(255, 26, 117, 0.9);
            z-index: 250;
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        /* 简洁的背景 - 减少视觉干扰 */
        .background-stars {
            position: absolute;
            width: 100%;
            height: 100%;
            z-index: 5;
        }

        .star {
            position: absolute;
            width: 2px;
            height: 2px;
            background: white;
            border-radius: 50%;
            opacity: 0.6;
        }

        @keyframes coinSpin {
            0% { transform: rotate(0deg) scale(1); }
            50% { transform: rotate(180deg) scale(1.1); }
            100% { transform: rotate(360deg) scale(1); }
        }

        @keyframes pulse {
            0% { transform: scale(1); opacity: 0.7; }
            100% { transform: scale(1.2); opacity: 1; }
        }

        @keyframes shieldPulse {
            0% { transform: scale(1); box-shadow: 0 0 25px rgba(76, 175, 80, 0.9); }
            100% { transform: scale(1.1); box-shadow: 0 0 35px rgba(76, 175, 80, 1); }
        }

        @keyframes explosion {
            0% { transform: scale(0); opacity: 1; }
            100% { transform: scale(1.5); opacity: 0; }
        }

        @keyframes policeLight {
            0% { opacity: 1; }
            100% { opacity: 0.6; }
        }

        @keyframes starBlink {
            0% { opacity: 0.3; }
            50% { opacity: 1; }
            100% { opacity: 0.3; }
        }
    </style>
</head>
<body>
    <div class="game-container">
        <div class="road">
            <div class="road-markings" id="road-markings"></div>
            <div class="side-line left"></div>
            <div class="side-line right"></div>
            <div class="background-stars" id="background-stars"></div>
        </div>
        
        <div class="player-car" id="player-car">
            <div class="car-window"></div>
            <div class="car-light left"></div>
            <div class="car-light right"></div>
            <div class="car-exhaust"></div>
        </div>
        
        <div class="top-ui">
            <div class="score-display" id="score">SCORE: 0</div>
            <div class="speed-display" id="speed">SPEED: 0 KM/H</div>
        </div>
        
        <div class="nitro-container">
            <div class="nitro-bar-background">
                <div class="nitro-bar-fill" id="nitro-bar"></div>
            </div>
        </div>
        
        <div class="skills-bar">
            <div class="skill-slot skill-nitro" id="nitro-skill">
                <div class="skill-icon">⚡</div>
                <div class="skill-name">NITRO</div>
                <div class="skill-cooldown" id="nitro-cooldown"></div>
                <div class="skill-charge" id="nitro-charge"></div>
            </div>
            <div class="skill-slot skill-shield" id="shield-skill">
                <div class="skill-icon">🛡️</div>
                <div class="skill-name">SHIELD</div>
                <div class="skill-cooldown" id="shield-cooldown"></div>
            </div>
            <div class="skill-slot skill-drift" id="drift-skill">
                <div class="skill-icon">🔥</div>
                <div class="skill-name">DRIFT</div>
                <div class="skill-cooldown" id="drift-cooldown"></div>
            </div>
        </div>
        
        <div class="controls">
            <div class="control-btn" id="left-btn">←</div>
            <div class="control-btn" id="right-btn">→</div>
        </div>
        
        <div class="countdown" id="countdown">3</div>
        
        <div class="game-over" id="game-over">
            <h1>RACE OVER</h1>
            
            <div class="game-over-stats">
                <div class="stat-box">
                    <div class="stat-title">FINAL SCORE</div>
                    <div class="stat-value" id="final-score">0</div>
                </div>
                <div class="stat-box">
                    <div class="stat-title">MAX SPEED</div>
                    <div class="stat-value" id="max-speed">0 KM/H</div>
                </div>
            </div>
            
            <div class="action-buttons">
                <button class="action-btn" id="restart-btn">RESTART</button>
                <button class="action-btn" id="menu-btn">MENU</button>
            </div>
        </div>
    </div>

    <script>
        class StreetRacingPro {
            constructor() {
                // DOM元素
                this.playerCar = document.getElementById('player-car');
                this.road = document.querySelector('.road');
                this.scoreDisplay = document.getElementById('score');
                this.speedDisplay = document.getElementById('speed');
                this.nitroBar = document.getElementById('nitro-bar');
                this.nitroChargeBar = document.getElementById('nitro-charge');
                this.countdownElement = document.getElementById('countdown');
                this.gameOverScreen = document.getElementById('game-over');
                this.finalScoreDisplay = document.getElementById('final-score');
                this.maxSpeedDisplay = document.getElementById('max-speed');
                
                // 技能按钮
                this.nitroSkillBtn = document.getElementById('nitro-skill');
                this.shieldSkillBtn = document.getElementById('shield-skill');
                this.driftSkillBtn = document.getElementById('drift-skill');
                this.nitroCooldown = document.getElementById('nitro-cooldown');
                this.shieldCooldown = document.getElementById('shield-cooldown');
                this.driftCooldown = document.getElementById('drift-cooldown');
                
                // 控制按钮
                this.leftBtn = document.getElementById('left-btn');
                this.rightBtn = document.getElementById('right-btn');
                this.restartBtn = document.getElementById('restart-btn');
                this.menuBtn = document.getElementById('menu-btn');
                
                // 游戏状态
                this.playerX = 240; // 初始位置 (480px width / 2)
                this.playerY = 610; // 固定Y位置
                this.playerSpeed = 0;
                this.maxSpeed = 40;
                this.baseAcceleration = 0.8;
                this.acceleration = this.baseAcceleration;
                this.deceleration = 0.5;
                this.turnSpeed = 12;
                this.score = 0;
                this.maxSpeedAchieved = 0;
                this.gameOver = false;
                this.gameStarted = false;
                this.nitroActive = false;
                this.shieldActive = false;
                this.driftActive = false;
                this.nitroCharge = 0;
                this.nitroMax = 100;
                this.skillCooldowns = {
                    nitro: 0,
                    shield: 0,
                    drift: 0
                };
                
                // 游戏对象
                this.obstacles = [];
                this.coins = [];
                this.powerups = [];
                this.particles = [];
                this.keys = {};
                this.roadOffset = 0;
                this.difficulty = 1;
                this.obstacleFrequency = 1000;
                this.coinFrequency = 800;
                this.powerupFrequency = 1500;
                
                // 初始化
                this.init();
            }
            
            init() {
                this.createRoadMarkings();
                this.createBackgroundStars();
                this.setupEventListeners();
                this.showCountdown();
            }
            
            createRoadMarkings() {
                const roadMarkings = document.getElementById('road-markings');
                for (let i = 0; i < 25; i++) {
                    const marking = document.createElement('div');
                    marking.className = 'road-marking';
                    marking.style.top = `${i * 40}px`;
                    roadMarkings.appendChild(marking);
                }
            }
            
            createBackgroundStars() {
                const starsContainer = document.getElementById('background-stars');
                const starCount = 80;
                
                for (let i = 0; i < starCount; i++) {
                    const star = document.createElement('div');
                    star.className = 'star';
                    
                    const size = 1 + Math.random() * 2;
                    const leftPos = Math.random() * 480;
                    const topPos = Math.random() * 760;
                    const opacity = 0.2 + Math.random() * 0.8;
                    
                    star.style.width = `${size}px`;
                    star.style.height = `${size}px`;
                    star.style.left = `${leftPos}px`;
                    star.style.top = `${topPos}px`;
                    star.style.opacity = opacity;
                    star.style.animation = `starBlink ${2 + Math.random() * 4}s infinite`;
                    
                    starsContainer.appendChild(star);
                }
            }
            
            setupEventListeners() {
                // 键盘控制
                window.addEventListener('keydown', (e) => {
                    this.keys[e.key] = true;
                    
                    // 技能快捷键
                    if (e.key === '1' && !this.skillCooldowns.nitro && this.nitroCharge >= 30) this.activateNitro();
                    if (e.key === '2' && !this.skillCooldowns.shield) this.activateShield();
                    if (e.key === '3' && !this.skillCooldowns.drift) this.activateDrift();
                    
                    // 空格键加速
                    if (e.key === ' ' && !this.nitroActive) {
                        this.accelerate();
                    }
                    
                    // R键重新开始
                    if (e.key === 'r' && this.gameOver) {
                        this.restartGame();
                    }
                });
                
                window.addEventListener('keyup', (e) => {
                    this.keys[e.key] = false;
                });
                
                // 触屏控制
                this.leftBtn.addEventListener('touchstart', (e) => {
                    e.preventDefault();
                    this.keys.ArrowLeft = true;
                });
                
                this.leftBtn.addEventListener('touchend', (e) => {
                    e.preventDefault();
                    this.keys.ArrowLeft = false;
                });
                
                this.rightBtn.addEventListener('touchstart', (e) => {
                    e.preventDefault();
                    this.keys.ArrowRight = true;
                });
                
                this.rightBtn.addEventListener('touchend', (e) => {
                    e.preventDefault();
                    this.keys.ArrowRight = false;
                });
                
                // 技能按钮
                this.nitroSkillBtn.addEventListener('click', () => {
                    if (!this.skillCooldowns.nitro && this.nitroCharge >= 30) {
                        this.activateNitro();
                    }
                });
                
                this.shieldSkillBtn.addEventListener('click', () => {
                    if (!this.skillCooldowns.shield) {
                        this.activateShield();
                    }
                });
                
                this.driftSkillBtn.addEventListener('click', () => {
                    if (!this.skillCooldowns.drift) {
                        this.activateDrift();
                    }
                });
                
                // 重新开始和菜单按钮
                this.restartBtn.addEventListener('click', () => {
                    this.restartGame();
                });
                
                this.menuBtn.addEventListener('click', () => {
                    this.showMainMenu();
                });
                
                // 防止页面滚动
                document.addEventListener('touchmove', (e) => {
                    if (e.target.closest('.control-btn, .skill-slot')) {
                        e.preventDefault();
                    }
                }, { passive: false });
            }
            
            showCountdown() {
                let count = 3;
                this.countdownElement.style.opacity = '1';
                this.countdownElement.style.display = 'block';
                
                const countdownInterval = setInterval(() => {
                    if (count > 0) {
                        this.countdownElement.textContent = count;
                        count--;
                    } else {
                        this.countdownElement.textContent = 'GO!';
                        setTimeout(() => {
                            this.countdownElement.style.opacity = '0';
                            setTimeout(() => {
                                this.countdownElement.style.display = 'none';
                                this.gameStarted = true;
                                this.startGame();
                            }, 300);
                        }, 500);
                        clearInterval(countdownInterval);
                    }
                }, 1000);
            }
            
            startGame() {
                this.gameLoop();
                this.spawnObstacles();
                this.spawnCoins();
                this.spawnPowerups();
                this.updateRoad();
            }
            
            gameLoop() {
                if (!this.gameOver && this.gameStarted) {
                    this.updatePlayer();
                    this.moveObstacles();
                    this.moveCoins();
                    this.movePowerups();
                    this.updateParticles();
                    this.checkCollisions();
                    this.updateGameStats();
                    this.updateSkillsUI();
                    
                    requestAnimationFrame(() => this.gameLoop());
                }
            }
            
            updatePlayer() {
                // 处理转向
                if (this.keys.ArrowLeft) {
                    this.playerX = Math.max(70, this.playerX - this.turnSpeed);
                    this.playerCar.style.transform = `translateX(-50%) rotateZ(-3deg)`;
                } else if (this.keys.ArrowRight) {
                    this.playerX = Math.min(410, this.playerX + this.turnSpeed);
                    this.playerCar.style.transform = `translateX(-50%) rotateZ(3deg)`;
                } else {
                    this.playerCar.style.transform = `translateX(-50%) rotateZ(0deg)`;
                }
                
                // 更新玩家位置
                this.playerCar.style.left = `${this.playerX}px`;
                
                // 加速/减速
                if (this.keys[' '] && !this.nitroActive) {
                    this.playerSpeed = Math.min(this.maxSpeed, this.playerSpeed + this.acceleration);
                } else {
                    this.playerSpeed = Math.max(0, this.playerSpeed - this.deceleration);
                }
                
                // 更新氮气充能
                if (this.playerSpeed > 10) {
                    this.nitroCharge = Math.min(this.nitroMax, this.nitroCharge + 0.2);
                    this.nitroBar.style.width = `${this.nitroCharge}%`;
                    this.nitroChargeBar.style.width = `${this.nitroCharge}%`;
                }
                
                // 氮气效果
                if (this.nitroActive) {
                    const exhaust = this.playerCar.querySelector('.car-exhaust');
                    exhaust.style.boxShadow = '0 0 30px rgba(255, 255, 255, 0.9), 0 0 60px rgba(0, 255, 255, 0.8)';
                }
                
                // 护盾效果
                if (this.shieldActive) {
                    this.playerCar.style.boxShadow = '0 0 30px rgba(76, 175, 80, 0.9), 0 0 60px rgba(76, 175, 80, 0.7), inset 0 0 15px rgba(255, 255, 255, 0.2)';
                }
                
                // 更新最高速度记录
                this.maxSpeedAchieved = Math.max(this.maxSpeedAchieved, this.playerSpeed * 4);
            }
            
            accelerate() {
                this.playerSpeed = Math.min(this.maxSpeed, this.playerSpeed + this.acceleration * 2);
            }
            
            activateNitro() {
                if (this.nitroCharge < 30 || this.skillCooldowns.nitro || this.nitroActive) return;
                
                this.nitroActive = true;
                this.nitroCharge -= 30;
                this.nitroBar.style.width = `${this.nitroCharge}%`;
                this.nitroChargeBar.style.width = `${this.nitroCharge}%`;
                
                // 3秒氮气加速
                this.playerSpeed = Math.min(this.maxSpeed * 1.8, this.playerSpeed + 15);
                this.acceleration *= 2.5;
                
                // 创建氮气特效
                this.createNitroParticles();
                
                setTimeout(() => {
                    this.nitroActive = false;
                    this.acceleration = this.baseAcceleration;
                    const exhaust = this.playerCar.querySelector('.car-exhaust');
                    exhaust.style.boxShadow = '0 0 15px rgba(255, 26, 26, 0.8)';
                    
                    // 设置冷却时间
                    this.skillCooldowns.nitro = 3;
                    this.updateSkillCooldown('nitro');
                }, 3000);
            }
            
            activateShield() {
                if (this.skillCooldowns.shield || this.shieldActive) return;
                
                this.shieldActive = true;
                this.playerCar.style.boxShadow = '0 0 30px rgba(76, 175, 80, 0.9), 0 0 60px rgba(76, 175, 80, 0.7), inset 0 0 15px rgba(255, 255, 255, 0.2)';
                
                // 5秒护盾
                setTimeout(() => {
                    this.shieldActive = false;
                    this.playerCar.style.boxShadow = '0 0 30px rgba(255, 26, 117, 0.8), inset 0 0 15px rgba(255, 255, 255, 0.2)';
                    
                    // 设置冷却时间
                    this.skillCooldowns.shield = 5;
                    this.updateSkillCooldown('shield');
                }, 5000);
            }
            
            activateDrift() {
                if (this.skillCooldowns.drift || this.driftActive) return;
                
                this.driftActive = true;
                this.turnSpeed *= 1.8;
                
                // 3秒飘移
                setTimeout(() => {
                    this.driftActive = false;
                    this.turnSpeed = 12;
                    
                    // 设置冷却时间
                    this.skillCooldowns.drift = 6;
                    this.updateSkillCooldown('drift');
                }, 3000);
            }
            
            updateSkillCooldown(skill) {
                const cooldownElement = {
                    'nitro': this.nitroCooldown,
                    'shield': this.shieldCooldown,
                    'drift': this.driftCooldown
                }[skill];
                
                cooldownElement.textContent = `${this.skillCooldowns[skill]}s`;
                
                const interval = setInterval(() => {
                    if (this.skillCooldowns[skill] <= 0) {
                        clearInterval(interval);
                        cooldownElement.textContent = '';
                        return;
                    }
                    
                    this.skillCooldowns[skill]--;
                    cooldownElement.textContent = `${this.skillCooldowns[skill]}s`;
                }, 1000);
            }
            
            createNitroParticles() {
                for (let i = 0; i < 20; i++) {
                    setTimeout(() => {
                        if (!this.gameOver) {
                            const particle = document.createElement('div');
                            particle.className = 'particle';
                            particle.style.background = `linear-gradient(135deg, #00ffff, #00bfff)`;
                            particle.style.width = `${4 + Math.random() * 8}px`;
                            particle.style.height = `${4 + Math.random() * 8}px`;
                            particle.style.left = `${this.playerX + (-15 + Math.random() * 30)}px`;
                            particle.style.top = `${this.playerY + 80}px`;
                            particle.style.boxShadow = '0 0 10px rgba(0, 255, 255, 0.8)';
                            
                            this.road.appendChild(particle);
                            
                            this.particles.push({
                                element: particle,
                                x: parseFloat(particle.style.left),
                                y: parseFloat(particle.style.top),
                                speedX: -8 + Math.random() * 16,
                                speedY: 5 + Math.random() * 10,
                                life: 25,
                                opacity: 1
                            });
                        }
                    }, i * 40);
                }
            }
            
            createExplosion(x, y) {
                const explosion = document.createElement('div');
                explosion.className = 'explosion';
                explosion.style.left = `${x}px`;
                explosion.style.top = `${y}px`;
                
                this.road.appendChild(explosion);
                
                setTimeout(() => {
                    explosion.remove();
                }, 500);
            }
            
            updateParticles() {
                for (let i = this.particles.length - 1; i >= 0; i--) {
                    const p = this.particles[i];
                    p.x += p.speedX;
                    p.y += p.speedY;
                    
                    p.life--;
                    p.opacity = p.life / 25;
                    
                    p.element.style.left = `${p.x}px`;
                    p.element.style.top = `${p.y}px`;
                    p.element.style.opacity = p.opacity;
                    
                    if (p.life <= 0 || p.y > 800 || p.x < -50 || p.x > 530) {
                        p.element.remove();
                        this.particles.splice(i, 1);
                    }
                }
            }
            
            spawnObstacles() {
                if (this.gameOver || !this.gameStarted) return;
                
                const obstacleTypes = ['car', 'truck', 'police', 'motorcycle'];
                const randomType = obstacleTypes[Math.floor(Math.random() * obstacleTypes.length)];
                
                const obstacle = document.createElement('div');
                obstacle.className = 'obstacle obstacle-' + randomType;
                
                // 根据类型设置尺寸
                const dimensions = {
                    'car': { width: 50, height: 80 },
                    'truck': { width: 70, height: 90 },
                    'police': { width: 55, height: 85 },
                    'motorcycle': { width: 30, height: 60 }
                };
                
                const { width, height } = dimensions[randomType];
                
                // 确保障碍物不会生成在道路边缘
                const safeLeft = 70;
                const safeRight = 410 - width;
                const leftPos = safeLeft + Math.random() * (safeRight - safeLeft);
                
                obstacle.style.width = `${width}px`;
                obstacle.style.height = `${height}px`;
                obstacle.style.left = `${leftPos}px`;
                obstacle.style.top = '-150px';
                
                this.road.appendChild(obstacle);
                
                // 添加子元素（根据类型）
                if (randomType === 'car') {
                    const topPart = document.createElement('div');
                    topPart.className = 'obstacle-car-top';
                    obstacle.appendChild(topPart);
                } else if (randomType === 'truck') {
                    const cab = document.createElement('div');
                    cab.className = 'obstacle-truck-cab';
                    obstacle.appendChild(cab);
                } else if (randomType === 'police') {
                    const topPart = document.createElement('div');
                    topPart.className = 'obstacle-police-top';
                    obstacle.appendChild(topPart);
                    
                    const bottomPart = document.createElement('div');
                    bottomPart.className = 'obstacle-police-bottom';
                    obstacle.appendChild(bottomPart);
                    
                    const light = document.createElement('div');
                    light.className = 'police-light';
                    bottomPart.appendChild(light);
                } else if (randomType === 'motorcycle') {
                    const seat = document.createElement('div');
                    seat.className = 'motorcycle-seat';
                    obstacle.appendChild(seat);
                }
                
                this.obstacles.push({
                    element: obstacle,
                    x: leftPos,
                    y: -150,
                    width: width,
                    height: height,
                    speed: 3 + Math.random() * 3 + this.playerSpeed * 0.6 * this.difficulty,
                    type: randomType
                });
                
                // 根据速度和难度调整生成频率
                const baseFrequency = 1200;
                const speedFactor = Math.max(0.4, 1 - this.playerSpeed / 60);
                const difficultyFactor = Math.max(0.6, 1.4 - this.difficulty * 0.2);
                const spawnInterval = baseFrequency * speedFactor * difficultyFactor;
                
                setTimeout(() => this.spawnObstacles(), spawnInterval);
            }
            
            spawnCoins() {
                if (this.gameOver || !this.gameStarted) return;
                
                const coin = document.createElement('div');
                coin.className = 'coin';
                
                // 确保不会生成在道路边缘
                const safeLeft = 80;
                const safeRight = 400;
                const leftPos = safeLeft + Math.random() * (safeRight - safeLeft);
                
                coin.style.left = `${leftPos}px`;
                coin.style.top = '-80px';
                
                this.road.appendChild(coin);
                
                this.coins.push({
                    element: coin,
                    x: leftPos,
                    y: -80,
                    width: 25,
                    height: 25,
                    speed: 4 + this.playerSpeed * 0.5
                });
                
                setTimeout(() => this.spawnCoins(), this.coinFrequency);
            }
            
            spawnPowerups() {
                if (this.gameOver || !this.gameStarted) return;
                
                const powerupTypes = ['nitro', 'shield'];
                const randomType = powerupTypes[Math.floor(Math.random() * powerupTypes.length)];
                
                const powerup = document.createElement('div');
                powerup.className = randomType + '-powerup';
                
                // 确保不会生成在道路边缘
                const safeLeft = 85;
                const safeRight = 395;
                const leftPos = safeLeft + Math.random() * (safeRight - safeLeft);
                
                powerup.style.left = `${leftPos}px`;
                powerup.style.top = '-100px';
                
                this.road.appendChild(powerup);
                
                this.powerups.push({
                    element: powerup,
                    x: leftPos,
                    y: -100,
                    width: 35,
                    height: 35,
                    speed: 3 + this.playerSpeed * 0.4,
                    type: randomType
                });
                
                setTimeout(() => this.spawnPowerups(), this.powerupFrequency);
            }
            
            moveObstacles() {
                for (let i = this.obstacles.length - 1; i >= 0; i--) {
                    const obs = this.obstacles[i];
                    obs.y += obs.speed;
                    obs.element.style.top = `${obs.y}px`;
                    
                    // 移除超出屏幕的障碍物
                    if (obs.y > 800) {
                        obs.element.remove();
                        this.obstacles.splice(i, 1);
                    }
                }
            }
            
            moveCoins() {
                for (let i = this.coins.length - 1; i >= 0; i--) {
                    const coin = this.coins[i];
                    coin.y += coin.speed;
                    coin.element.style.top = `${coin.y}px`;
                    
                    // 移除超出屏幕的硬币
                    if (coin.y > 800) {
                        coin.element.remove();
                        this.coins.splice(i, 1);
                    }
                }
            }
            
            movePowerups() {
                for (let i = this.powerups.length - 1; i >= 0; i--) {
                    const powerup = this.powerups[i];
                    powerup.y += powerup.speed;
                    powerup.element.style.top = `${powerup.y}px`;
                    
                    // 移除超出屏幕的道具
                    if (powerup.y > 800) {
                        powerup.element.remove();
                        this.powerups.splice(i, 1);
                    }
                }
            }
            
            updateRoad() {
                if (this.gameOver || !this.gameStarted) return;
                
                this.roadOffset += this.playerSpeed * 3;
                const markings = document.querySelectorAll('.road-marking');
                
                markings.forEach(marking => {
                    let top = parseInt(marking.style.top) || 0;
                    top += this.playerSpeed * 4 + (this.nitroActive ? 8 : 0);
                    
                    if (top > 800) {
                        top = -50;
                    }
                    
                    marking.style.top = `${top}px`;
                });
                
                requestAnimationFrame(() => this.updateRoad());
            }
            
            checkCollisions() {
                const playerRect = {
                    x: this.playerX - 30,
                    y: this.playerY - 100,
                    width: 60,
                    height: 100
                };
                
                // 检查与障碍物的碰撞
                for (let i = 0; i < this.obstacles.length; i++) {
                    const obs = this.obstacles[i];
                    if (this.checkCollision(playerRect, obs)) {
                        if (this.shieldActive) {
                            // 护盾吸收碰撞
                            this.shieldActive = false;
                            this.playerCar.style.boxShadow = '0 0 30px rgba(255, 26, 117, 0.8), inset 0 0 15px rgba(255, 255, 255, 0.2)';
                            this.createExplosion(obs.x + obs.width / 2, obs.y + obs.height / 2);
                            obs.element.remove();
                            this.obstacles.splice(i, 1);
                            this.score += 200;
                        } else {
                            this.endGame();
                            return;
                        }
                    }
                }
                
                // 检查与硬币的碰撞
                for (let i = this.coins.length - 1; i >= 0; i--) {
                    const coin = this.coins[i];
                    if (this.checkCollision(playerRect, coin)) {
                        this.collectCoin(i);
                    }
                }
                
                // 检查与道具的碰撞
                for (let i = this.powerups.length - 1; i >= 0; i--) {
                    const powerup = this.powerups[i];
                    if (this.checkCollision(playerRect, powerup)) {
                        this.collectPowerup(i, powerup.type);
                    }
                }
            }
            
            checkCollision(rect1, rect2) {
                return (
                    rect1.x < rect2.x + rect2.width &&
                    rect1.x + rect1.width > rect2.x &&
                    rect1.y < rect2.y + rect2.height &&
                    rect1.y + rect1.height > rect2.y
                );
            }
            
            collectCoin(index) {
                const coin = this.coins[index];
                coin.element.remove();
                this.coins.splice(index, 1);
                
                this.score += 100;
                this.nitroCharge = Math.min(this.nitroMax, this.nitroCharge + 3);
                
                // 创建收集特效
                this.createCollectEffect(coin.x + 12, coin.y + 12, '#ffd700');
            }
            
            collectPowerup(index, type) {
                const powerup = this.powerups[index];
                powerup.element.remove();
                this.powerups.splice(index, 1);
                
                switch (type) {
                    case 'nitro':
                        this.nitroCharge = Math.min(this.nitroMax, this.nitroCharge + 40);
                        break;
                    case 'shield':
                        if (!this.shieldActive && !this.skillCooldowns.shield) {
                            this.activateShield();
                        }
                        break;
                }
                
                // 创建收集特效
                const color = type === 'nitro' ? '#00ffff' : '#4caf50';
                this.createCollectEffect(powerup.x + 17, powerup.y + 17, color);
            }
            
            createCollectEffect(x, y, color) {
                for (let i = 0; i < 10; i++) {
                    const particle = document.createElement('div');
                    particle.className = 'particle';
                    particle.style.background = color;
                    particle.style.width = `${2 + Math.random() * 5}px`;
                    particle.style.height = `${2 + Math.random() * 5}px`;
                    particle.style.left = `${x}px`;
                    particle.style.top = `${y}px`;
                    particle.style.boxShadow = `0 0 8px ${color}`;
                    
                    this.road.appendChild(particle);
                    
                    this.particles.push({
                        element: particle,
                        x: x,
                        y: y,
                        speedX: -4 + Math.random() * 8,
                        speedY: -4 + Math.random() * 8,
                        life: 15,
                        opacity: 1
                    });
                }
            }
            
            updateGameStats() {
                this.score += Math.floor(this.playerSpeed * 0.3);
                this.scoreDisplay.textContent = `SCORE: ${Math.floor(this.score)}`;
                this.speedDisplay.textContent = `SPEED: ${Math.floor(this.playerSpeed * 4)} KM/H`;
            }
            
            updateSkillsUI() {
                // 更新技能按钮状态
                this.nitroSkillBtn.style.opacity = this.nitroCharge >= 30 && !this.skillCooldowns.nitro ? '1' : '0.5';
                this.nitroSkillBtn.classList.toggle('inactive', !(this.nitroCharge >= 30 && !this.skillCooldowns.nitro));
                
                this.shieldSkillBtn.style.opacity = !this.skillCooldowns.shield ? '1' : '0.5';
                this.shieldSkillBtn.classList.toggle('inactive', !!this.skillCooldowns.shield);
                
                this.driftSkillBtn.style.opacity = !this.skillCooldowns.drift ? '1' : '0.5';
                this.driftSkillBtn.classList.toggle('inactive', !!this.skillCooldowns.drift);
            }
            
            endGame() {
                this.gameOver = true;
                this.finalScoreDisplay.textContent = Math.floor(this.score);
                this.maxSpeedDisplay.textContent = `${Math.floor(this.maxSpeedAchieved)} KM/H`;
                
                this.gameOverScreen.style.display = 'flex';
                
                // 移除所有游戏对象
                this.obstacles.forEach(obs => obs.element.remove());
                this.coins.forEach(coin => coin.element.remove());
                this.powerups.forEach(powerup => powerup.element.remove());
                this.obstacles = [];
                this.coins = [];
                this.powerups = [];
            }
            
            restartGame() {
                this.gameOver = false;
                this.gameStarted = true;
                this.score = 0;
                this.maxSpeedAchieved = 0;
                this.nitroCharge = 0;
                this.difficulty = 1;
                this.maxSpeed = 40;
                this.playerSpeed = 0;
                this.playerX = 240;
                this.skillCooldowns = { nitro: 0, shield: 0, drift: 0 };
                this.nitroActive = false;
                this.shieldActive = false;
                this.driftActive = false;
                
                // 重置UI
                this.scoreDisplay.textContent = 'SCORE: 0';
                this.speedDisplay.textContent = 'SPEED: 0 KM/H';
                this.nitroBar.style.width = '0%';
                this.nitroChargeBar.style.width = '0%';
                this.nitroCooldown.textContent = '';
                this.shieldCooldown.textContent = '';
                this.driftCooldown.textContent = '';
                
                this.gameOverScreen.style.display = 'none';
                this.playerCar.style.left = '240px';
                this.playerCar.style.transform = 'translateX(-50%) rotateZ(0deg)';
                this.playerCar.style.boxShadow = '0 0 30px rgba(255, 26, 117, 0.8), inset 0 0 15px rgba(255, 255, 255, 0.2)';
                
                // 清除所有粒子
                this.particles.forEach(p => p.element.remove());
                this.particles = [];
                
                // 重新开始游戏
                this.startGame();
            }
            
            showMainMenu() {
                alert('Main Menu Coming Soon!\nThis is a demo version.');
                this.restartGame();
            }
        }
        
        // 初始化游戏
        document.addEventListener('DOMContentLoaded', () => {
            new StreetRacingPro();
        });
    </script>
</body>
</html>
<!-- 完整代碼已上傳，包含以下核心組件： -->

1. HTML結構
   - 遊戲容器 (480x760px)
   - 道路系統
   - 玩家賽車
   - UI元素（分數、速度、技能欄、控制按鈕）

2. CSS樣式
   - 遊戲界面美化
   - 賽車和障礙物樣式
   - 技能按鈕設計
   - 動畫效果（旋轉、脈衝、爆炸）

3. JavaScript遊戲邏輯
   - StreetRacingPro類（主遊戲類）
   - 初始化系統
   - 道路和背景生成
   - 玩家控制系統
   - 技能系統（氮氣、護盾、飄移）
   - 障礙物生成和管理
   - 收集系統（金币、道具）
   - 碰撞檢測
   - 粒子特效系統
   - 遊戲循環和統計更新

4. 遊戲對象
   - 四種障礙物：普通轎車、卡車、警車、摩托車
   - 兩種道具：氮氣、護盾
   - 金币收集
   - 粒子和爆炸特效

5. 事件監聽
   - 鍵盤控制（方向鍵、空格、1-3技能鍵）
   - 觸屏控制（左右按鈕、技能按鈕）
   - 遊戲重啟和菜單功能
```

## 八、後續擴展建議

1. **音效系統**：添加背景音樂和音效
2. **成就系統**：更多成就和獎勵
3. **車輛自定義**：多種賽車選擇
4. **排行榜**：全球或好友排行榜
5. **多種賽道**：不同主題的賽道
6. **故事模式**：關卡和任務系統
7. **社交分享**：分享成績到社交媒體

---

**文檔版本**：1.0  
**最後更新**：2026年1月30日  
**狀態**：已完成