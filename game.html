import React, { useState, useEffect } from 'react';

const MemoryGame = () => {
  // قائمة الصور المستخدمة في اللعبة
  const cardImages = [
    { src: "/api/placeholder/80/80", matched: false, name: "قطة" },
    { src: "/api/placeholder/80/80", matched: false, name: "كلب" },
    { src: "/api/placeholder/80/80", matched: false, name: "أسد" },
    { src: "/api/placeholder/80/80", matched: false, name: "فيل" },
    { src: "/api/placeholder/80/80", matched: false, name: "زرافة" },
    { src: "/api/placeholder/80/80", matched: false, name: "قرد" },
  ];

  const [cards, setCards] = useState([]);
  const [turns, setTurns] = useState(0);
  const [choiceOne, setChoiceOne] = useState(null);
  const [choiceTwo, setChoiceTwo] = useState(null);
  const [disabled, setDisabled] = useState(false);
  const [matchedPairs, setMatchedPairs] = useState(0);
  const [gameComplete, setGameComplete] = useState(false);

  // خلط البطاقات
  const shuffleCards = () => {
    // مضاعفة البطاقات وخلطها
    const shuffledCards = [...cardImages, ...cardImages]
      .sort(() => Math.random() - 0.5)
      .map((card, index) => ({ ...card, id: index }));
    
    setChoiceOne(null);
    setChoiceTwo(null);
    setCards(shuffledCards);
    setTurns(0);
    setMatchedPairs(0);
    setGameComplete(false);
  };

  // التعامل مع اختيار البطاقة
  const handleChoice = (card) => {
    choiceOne ? setChoiceTwo(card) : setChoiceOne(card);
  };

  // مقارنة البطاقتين المختارتين
  useEffect(() => {
    if (choiceOne && choiceTwo) {
      setDisabled(true);
      
      if (choiceOne.name === choiceTwo.name) {
        // تطابق البطاقات
        setCards(prevCards => {
          return prevCards.map(card => {
            if (card.name === choiceOne.name) {
              return { ...card, matched: true };
            } else {
              return card;
            }
          });
        });
        setMatchedPairs(prev => prev + 1);
        resetTurn();
      } else {
        // عدم تطابق البطاقات
        setTimeout(() => resetTurn(), 1000);
      }
    }
  }, [choiceOne, choiceTwo]);

  // التحقق من اكتمال اللعبة
  useEffect(() => {
    if (matchedPairs === cardImages.length) {
      setGameComplete(true);
    }
  }, [matchedPairs]);

  // إعادة ضبط الاختيارات وزيادة عدد الجولات
  const resetTurn = () => {
    setChoiceOne(null);
    setChoiceTwo(null);
    setTurns(prevTurns => prevTurns + 1);
    setDisabled(false);
  };

  // بدء اللعبة عند التحميل
  useEffect(() => {
    shuffleCards();
  }, []);

  return (
    <div className="flex flex-col items-center w-full max-w-lg mx-auto">
      <h1 className="text-2xl font-bold mb-4 text-center">لعبة الذاكرة للأطفال</h1>
      <div className="flex justify-between w-full mb-4">
        <button 
          onClick={shuffleCards} 
          className="bg-blue-500 text-white p-2 rounded-md"
        >
          لعبة جديدة
        </button>
        <p className="p-2">عدد المحاولات: {turns}</p>
      </div>
      
      {gameComplete && (
        <div className="mb-4 p-4 bg-green-100 text-green-800 rounded-md text-center">
          أحسنت! لقد أكملت اللعبة في {turns} محاولة!
        </div>
      )}
      
      <div className="grid grid-cols-3 gap-4 w-full">
        {cards.map(card => (
          <div 
            key={card.id} 
            className={`bg-blue-100 h-24 rounded-md flex items-center justify-center text-center cursor-pointer transition-all duration-300 hover:scale-105 ${card.matched ? 'bg-green-100' : ''}`}
            onClick={() => !disabled && !card.matched && card !== choiceOne && card !== choiceTwo && handleChoice(card)}
          >
            {card === choiceOne || card === choiceTwo || card.matched ? (
              <div className="flex flex-col items-center">
                <span className="mb-1">{card.name}</span>
              </div>
            ) : (
              <span className="text-2xl">؟</span>
            )}
          </div>
        ))}
      </div>
    </div>
  );
};

export default MemoryGame;
