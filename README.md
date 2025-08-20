# Quebec Car Finance Calculator

A comprehensive web-based car payment calculator specifically designed for Quebec, Canada, featuring accurate tax calculations and multiple payment frequency options.

🚗 **Live Demo:** [car.m0rk.space](https://car.m0rk.space)

## Features

### 🧮 Payment Calculator
- **Vehicle Pricing**: Enter vehicle price, fees (freight, PDI, AC tax, etc.)
- **Deductions**: Factor in down payment, trade-in value, federal and provincial EV incentives
- **Quebec Tax Accuracy**: Automatically calculates GST (5%) and QST (9.975%) on the correct taxable amount
- **Multiple Payment Frequencies**: View monthly, bi-weekly, and weekly payment options
- **Interactive Controls**: Slider-based interest rate and loan term selection
- **Payment Matrix**: Compare multiple interest rates and loan terms side-by-side

### 💰 Budget Calculator
- **Reverse Calculations**: Start with your desired monthly payment
- **Two Modes**:
  - Find maximum affordable vehicle price
  - Calculate minimum required down payment
- **Real-time Results**: Instant calculations as you adjust parameters

### 🎯 Key Highlights
- **Quebec-Specific**: Properly handles Quebec's unique tax structure (trade-in reduces taxable amount)
- **Comprehensive**: Includes all common fees, incentives, and deductions
- **Visual Comparison**: Payment matrix with color-coded best/worst options
- **Data Persistence**: Automatically saves your inputs using local storage
- **Mobile Responsive**: Works seamlessly on desktop, tablet, and mobile devices

## How to Use

### Payment Calculator
1. Enter your vehicle price and associated fees
2. Add any deductions (down payment, trade-in, incentives)
3. Adjust interest rate and loan term using the sliders
4. View calculated payments for monthly, bi-weekly, and weekly schedules
5. Use the payment matrix to compare different scenarios

### Budget Calculator
1. Switch to the "Budget Calculator" tab
2. Enter your desired monthly payment amount
3. Choose calculation mode:
   - **Max Vehicle Price**: Find the most expensive vehicle you can afford
   - **Min Down Payment**: Calculate the minimum down payment needed for a specific vehicle
4. Results update automatically based on your loan parameters from the main tab

## Technical Details

### Technologies Used
- **Frontend**: Vanilla HTML5, CSS3, JavaScript
- **Framework**: [Alpine.js](https://alpinejs.dev/) for reactive data binding
- **Styling**: [Tailwind CSS](https://tailwindcss.com/) for responsive design
- **Icons**: Heroicons via SVG
- **Fonts**: Inter font family from Google Fonts

### Quebec Tax Calculations
The calculator correctly implements Quebec's tax structure:
- **GST**: 5% federal tax
- **QST**: 9.975% provincial tax  
- **Taxable Amount**: Vehicle price + fees - trade-in value (trade-in reduces tax burden)
- **Total Tax Rate**: 14.975% on taxable amount

### Payment Calculations
Uses standard loan amortization formulas:
```
Monthly Payment = P × [r(1+r)^n] / [(1+r)^n - 1]
```
Where:
- P = Principal (amount financed)
- r = Monthly interest rate
- n = Number of payments

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

This calculator is provided for estimation purposes only. Actual loan terms, taxes, and fees may vary. Always verify calculations with your financial institution and dealer before making financial decisions.

---

**Author**: Marc-André Dufresne  
**Live App**: [car.m0rk.space](https://car.m0rk.space)