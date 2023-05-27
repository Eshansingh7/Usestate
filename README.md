import React, { useState } from 'react';

const App = () => {
  const [isBackgroundDark, setBackgroundDark] = useState(false);

  const toggleBackground = () => {
    setBackgroundDark(!isBackgroundDark);
  };

  const backgroundColor = isBackgroundDark ? 'black' : 'white';
  const textColor = isBackgroundDark ? 'white' : 'black';

  return (
    <div style={{ backgroundColor, color: textColor, minHeight: '100vh' }}>
      <h1>Background Toggle</h1>
      <button onClick={toggleBackground}>Toggle Background</button>
    </div>
  );
};

export default App;
