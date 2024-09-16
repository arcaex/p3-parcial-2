# p3-parcial-2

// Ejercicio 6: Mostrando/Ocultando Texto

    import React from 'react';

    const ToggleText = () => {
      const [isVisible, setIsVisible] = useState(true);

      return (
        <div>
          <button onClick={() => setIsVisible(!isVisible)}>
            {isVisible ? 'Ocultar' : 'Mostrar'} Texto
          </button>
          {isVisible && <p>Este es el texto que se puede ocultar o mostrar.</p>}
        </div>
      );
    };

    export default ToggleText;
    

    // Ejercicio 7: Selección de Colores

    import React from 'react';

    const ColorSelector = () => {
      const colors = ['red', 'green', 'blue', 'yellow', 'pink'];
      const [selectedColor, setSelectedColor] = useState('');

      return (
        <div style={{ backgroundColor: selectedColor, height: '100vh', padding: '20px' }}>
          <h1>Seleccione un Color</h1>
          {colors.map(color) => (
            <button key={color} onClick={() => setSelectedColor(color)} style={{ margin: '5px' }}>
              {color}
            </button>
          )}
        </div>
      );
    };

    export default ColorSelector;
    

    // Ejercicio 8: Contador de Clicks

    import React from 'react';

    const ClickCounter = () => {
      const [count, setCount] = useState(0);

      return (
        <div>
          <h1>Has hecho clic {count} veces</h1>
          <button onClick={() => count + 1}>Haz clic aquí</button>
        </div>
      );
    };

    export default ClickCounter;
    

    // Ejercicio 9: Filtro de Búsqueda

    import React from 'react';

    const SearchFilter = () => {
      const items = ['Manzana', 'Banana', 'Cereza', 'Naranja', 'Pera'];
      const [searchTerm, setSearchTerm] = useState('');

      const filteredItems = items.filter((item) =>
        item.toLowerCase().contains(searchTerm.toLowerCase())
      );

      return (
        <div>
          <h1>Filtro de Búsqueda</h1>
          <input
            type="text"
            placeholder="Buscar..."
            value={searchTerm}
            onChange={(e) => setSearchTerm(e.target.value)}
          />
          <ul>
            {filteredItems.map((item, index) => (
              <li key={index}>{item}</li>
            ))}
          </ul>
        </div>
      );
    };

    export default SearchFilter;
    

    // Ejercicio 10: Cambio de Fuente

    import React from 'react';

    const FontChanger = () => {
      const fonts = ['Arial', 'Courier New', 'Georgia', 'Times New Roman', 'Verdana'];
      const [selectedFont, setSelectedFont] = useState('Arial');

      return (
        <div style={{ fontFamily: selectedFont, padding: '20px' }}>
          <h1>Cambiar Fuente</h1>
          <select onChange={(e) => setSelectedFont(e.target.value)} value={selectedFont}>
            {fonts.map((font) => (
              <option key={font} value={font}>
                {font}
              </option>
            ))}
          </select>
          <p>Este es un texto de ejemplo con la fuente seleccionada.</p>
        </div>
      );
    };

    export default FontChanger;
    
