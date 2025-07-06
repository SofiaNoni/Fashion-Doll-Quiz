# Fashion-Doll-Quiz
Quiz for customers
    body {
        font-family: 'Arial', sans-serif;
        background: linear-gradient(135deg, #ff6b9d 0%, #c44569 50%, #786fa6 100%);
        min-height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 20px;
    }

    .quiz-container {
        background: rgba(255, 255, 255, 0.95);
        border-radius: 20px;
        padding: 30px;
        max-width: 650px;
        width: 100%;
        box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
        backdrop-filter: blur(10px);
        border: 1px solid rgba(255, 255, 255, 0.2);
    }

    .quiz-header {
        text-align: center;
        margin-bottom: 30px;
    }

    .quiz-title {
        color: #333;
        font-size: 2.5em;
        margin-bottom: 10px;
        font-weight: bold;
        background: linear-gradient(45deg, #ff6b9d, #c44569);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        background-clip: text;
    }

    .quiz-subtitle {
        color: #666;
        font-size: 1.1em;
        margin-bottom: 20px;
        line-height: 1.4;
    }

    .question-container {
        margin-bottom: 25px;
    }

    .question {
        font-size: 1.2em;
        color: #333;
        margin-bottom: 15px;
        font-weight: 600;
    }

    .options {
        display: grid;
        gap: 12px;
    }

    .option {
        background: linear-gradient(135deg, #ffeef8 0%, #f8f4ff 100%);
        border: 2px solid #e9d5ff;
        border-radius: 15px;
        padding: 18px;
        cursor: pointer;
        transition: all 0.3s ease;
        display: flex;
        align-items: center;
        position: relative;
        overflow: hidden;
    }

    .option::before {
        content: '';
        position: absolute;
        top: 0;
        left: -100%;
        width: 100%;
        height: 100%;
        background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.4), transparent);
        transition: left 0.5s ease;
    }

    .option:hover::before {
        left: 100%;
    }

    .option:hover {
        background: linear-gradient(135deg, #ff6b9d, #c44569);
        border-color: #ff6b9d;
        transform: translateY(-3px);
        color: white;
        box-shadow: 0 10px 25px rgba(255, 107, 157, 0.3);
    }

    .option input[type="radio"] {
        margin-right: 15px;
        transform: scale(1.3);
        accent-color: #ff6b9d;
    }

    .option.selected {
        background: linear-gradient(135deg, #ff6b9d, #c44569);
        border-color: #ff6b9d;
        color: white;
        transform: translateY(-2px);
        box-shadow: 0 8px 20px rgba(255, 107, 157, 0.4);
    }

    .submit-btn {
        background: linear-gradient(135deg, #ff6b9d 0%, #c44569 50%, #786fa6 100%);
        color: white;
        border: none;
        padding: 18px 45px;
        font-size: 1.2em;
        border-radius: 30px;
        cursor: pointer;
        width: 100%;
        margin-top: 25px;
        transition: all 0.3s ease;
        font-weight: 600;
        text-transform: uppercase;
        letter-spacing: 1px;
    }

    .submit-btn:hover {
        transform: translateY(-3px);
        box-shadow: 0 15px 30px rgba(255, 107, 157, 0.4);
    }

    .submit-btn:disabled {
        background: #ccc;
        cursor: not-allowed;
        transform: none;
    }

    .results {
        display: none;
        text-align: center;
        padding: 25px;
        background: linear-gradient(135deg, #ffeef8 0%, #f8f4ff 100%);
        border-radius: 20px;
        margin-top: 25px;
        border: 2px solid #e9d5ff;
    }

    .results h3 {
        color: #333;
        margin-bottom: 20px;
        font-size: 1.6em;
        background: linear-gradient(45deg, #ff6b9d, #c44569);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        background-clip: text;
    }

    .result-item {
        background: white;
        padding: 15px;
        margin: 8px 0;
        border-radius: 12px;
        border-left: 5px solid #ff6b9d;
        box-shadow: 0 3px 10px rgba(0, 0, 0, 0.1);
    }

    .progress-bar {
        background: rgba(255, 255, 255, 0.3);
        height: 8px;
        border-radius: 4px;
        margin-bottom: 25px;
        overflow: hidden;
        backdrop-filter: blur(5px);
    }

    .progress-fill {
        background: linear-gradient(90deg, #ff6b9d, #c44569);
        height: 100%;
        width: 0%;
        transition: width 0.4s ease;
        border-radius: 4px;
    }

    .question-number {
        color: #ff6b9d;
        font-weight: bold;
        font-size: 0.9em;
        margin-bottom: 8px;
        display: flex;
        align-items: center;
    }

    .question-number::before {
        content: '✨';
        margin-right: 8px;
    }

    .doll-emoji {
        font-size: 1.5em;
        margin: 0 8px;
    }

    @media (max-width: 600px) {
        .quiz-title {
            font-size: 2em;
        }
        
        .quiz-container {
            padding: 20px;
        }
        
        .option {
            padding: 15px;
        }
    }
</style>
