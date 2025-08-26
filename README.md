# Quebec Car Finance Calculator

A comprehensive web-based car payment calculator specifically designed for Quebec, Canada, featuring accurate tax calculations, luxury tax support, dark mode, and multiple payment frequency options.

🚗 **Live Demo:** [car.m0rk.space](https://car.m0rk.space)

## Features

### 🧮 Payment Calculator
- **Vehicle Pricing**: Enter vehicle price with support for multiple fees (freight, PDI, AC tax, etc.)
- **Advanced Fee Management**: Add, remove, and describe multiple fees with dynamic input fields
- **Luxury Tax Support**: Automatic calculation of federal luxury tax for vehicles over $100,000
  - Uses the lesser of: 10% of full amount OR 20% of amount exceeding $100,000
  - Includes helpful tooltip explaining the calculation
- **Deductions**: Factor in down payment, trade-in value, federal and provincial EV incentives
- **Quebec Tax Accuracy**: Automatically calculates GST (5%) and QST (9.975%) on the correct taxable amount
- **Multiple Payment Frequencies**: View monthly, bi-weekly, and weekly payment options
- **Interactive Controls**: Slider-based interest rate and loan term selection with live updates
- **Payment Matrix**: Compare multiple interest rates and loan terms side-by-side with color-coded best/worst options

### 💰 Budget Calculator
- **Reverse Calculations**: Start with your desired monthly payment
- **Two Modes**:
  - Find maximum affordable vehicle price (accounts for all fees and taxes)
  - Calculate minimum required down payment for a specific vehicle
- **Real-time Results**: Instant calculations as you adjust parameters
- **Context Awareness**: Uses all settings from the main calculator tab

### 🌙 User Experience
- **Dark Mode**: Full dark/light theme toggle with system preference detection
- **Responsive Design**: Seamless experience across desktop, tablet, and mobile devices
- **Data Persistence**: Automatically saves all inputs using local storage
- **Visual Feedback**: Color-coded payment comparisons and interactive tooltips
- **Smooth Animations**: Transitions and hover effects for enhanced UX

### 🎯 Key Highlights
- **Quebec-Specific**: Properly handles Quebec's unique tax structure (trade-in reduces taxable amount)
- **Luxury Vehicle Ready**: Full support for federal luxury tax calculations
- **Comprehensive**: Includes all common fees, incentives, and deductions with flexible input system
- **Visual Comparison**: Payment matrix with color-coded best/worst options and trend indicators
- **Professional UI**: Clean, modern interface with Inter font and Tailwind CSS styling

## How to Use

### Payment Calculator
1. Enter your vehicle price and add any associated fees using the dynamic fee system
2. Add deductions (down payment, trade-in, federal/provincial incentives)
3. Adjust interest rate and loan term using the interactive sliders
4. View calculated payments for monthly, bi-weekly, and weekly schedules
5. Use the payment matrix to compare different interest rates and loan terms
6. Hover over the luxury tax info icon for calculation details

### Budget Calculator
1. Switch to the "Budget Calculator" tab
2. Enter your desired monthly payment amount
3. Choose calculation mode:
   - **Max Vehicle Price**: Find the most expensive vehicle you can afford
   - **Min Down Payment**: Calculate the minimum down payment needed for a specific vehicle
4. Results update automatically based on your loan parameters from the main tab

## Technical Details

### Technologies Used
- **Frontend**: Vanilla HTML5, CSS3, JavaScript (ES6+)
- **Framework**: [Alpine.js](https://alpinejs.dev/) v3.13.3 for reactive data binding
- **Styling**: [Tailwind CSS](https://tailwindcss.com/) with custom dark mode configuration
- **Icons**: Heroicons via inline SVG
- **Fonts**: Inter font family from Google Fonts for optimal readability

### Tax Calculations

#### Quebec Tax Structure
The calculator correctly implements Quebec's tax structure:
- **GST**: 5% federal tax
- **QST**: 9.975% provincial tax
- **Taxable Amount**: Vehicle price + fees + luxury tax - trade-in value
- **Total Standard Tax Rate**: 14.975% on taxable amount

#### Federal Luxury Tax
For vehicles over $100,000, the calculator applies federal luxury tax:
- **Threshold**: $100,000 CAD
- **Calculation**: Lesser of two methods:
  1. 10% of the full vehicle price + fees
  2. 20% of the amount exceeding $100,000
- **Tax on Tax**: Luxury tax is included in the taxable amount for GST/QST

### Payment Calculations
Uses standard loan amortization formulas:
```
Monthly Payment = P × [r(1+r)^n] / [(1+r)^n - 1]
```
Where:
- P = Principal (amount financed)
- r = Monthly interest rate
- n = Number of payments

Supports multiple payment frequencies:
- **Monthly**: 12 payments per year
- **Bi-weekly**: 26 payments per year (accelerated)
- **Weekly**: 52 payments per year (accelerated)

## Installation & Setup

### For Development
1. Clone the repository:
   ```bash
   git clone https://github.com/MarcDufresne/Car-Payment-Calculator.git
   cd Car-Payment-Calculator
   ```

2. Open `index.html` in your web browser or serve it with a local web server:
   ```bash
   # Using Python
   python -m http.server 8000

   # Using Node.js http-server
   npx http-server

   # Using PHP
   php -S localhost:8000
   ```

### For Production
Simply upload the files to any web server. The application is entirely client-side and requires no backend infrastructure.

## Browser Support

- Chrome 88+
- Firefox 78+
- Safari 14+
- Edge 88+

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Disclaimer

This calculator is provided for estimation purposes only. Actual loan terms, taxes, fees, and luxury tax calculations may vary. Always verify calculations with your financial institution and dealer before making financial decisions. Luxury tax calculations are based on current federal regulations and may be subject to change.

---

**Author**: Marc-André Dufresne  
**Live App**: [car.m0rk.space](https://car.m0rk.space)
