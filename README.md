# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

# Currency Converter App

This is a simple currency converter app built with React that allows users to convert an amount from one currency to another using real-time exchange rates.

## Features

- **Dynamic Currency Conversion**: Converts an entered amount from one currency to another using live exchange rates.
- **Currency Swap**: Users can swap the base and target currencies with a single button click.
- **Responsive Design**: The UI adjusts to different screen sizes for a seamless experience on mobile, tablet, and desktop devices.
- **Conversion History**: Users can see the latest conversion rate in the console for debugging purposes.
- **Input Validations**: Ensures that users cannot submit invalid data.

## Technologies Used

- **React**: A JavaScript library for building user interfaces.
- **Tailwind CSS**: For responsive, utility-first styling.
- **Custom Hooks**: To handle currency information fetching.
- **JavaScript (ES6)**: For logic and state management using `useState` and `useEffect` hooks.

## How It Works

1. **Enter Amount**: Input an amount in the "From" currency field.
2. **Choose Currencies**: Select the base currency (from) and the target currency (to) from the dropdowns.
3. **Convert**: Press the "Convert" button to see the converted amount in the "To" field.
4. **Swap**: Use the "Swap" button to quickly switch the base and target currencies.

### API Hook: `useCurrencyInfo`

The app uses a custom hook called `useCurrencyInfo` to fetch live currency data for conversions. The hook returns an object containing currency conversion rates relative to a selected base currency.

### Example

```javascript
const currencyInfo = useCurrencyInfo('usd');
console.log(currencyInfo);
// Output: { inr: 74.85, eur: 0.84, ... }
```

## How to Run the Project

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/currency-converter-app.git
   cd currency-converter-app
   ```

2. Install the dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm start
   ```

4. Open your browser and navigate to:
   ```
   http://localhost:3000
   ```

## Folder Structure

```bash
currency-converter-app/
├── public/
├── src/
│   ├── components/   # InputBox and other UI components
│   ├── hooks/        # Custom hooks (useCurrencyInfo)
│   ├── App.js        # Main application component
│   ├── index.js      # Entry point for the React app
├── README.md         # Project documentation
├── package.json      # Project dependencies and scripts
└── tailwind.config.js # Tailwind CSS configuration
```

## Improvements and Future Features

- **Conversion History**: Store and display a list of past conversions.
- **Error Handling**: Improve error handling for API failures.
- **Loading States**: Add a loading spinner when fetching data.
- **Mobile Optimizations**: Enhance mobile-specific UI/UX features.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
```

Feel free to customize it based on your specific project requirements and features!
