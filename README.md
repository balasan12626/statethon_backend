# UAE NCO Job Classification Frontend

This is the frontend application for the UAE NCO (National Classification of Occupations) Job Classification system.

## Features

- **Job Description Input**: Users can describe their job responsibilities
- **Voice Input**: Simulated voice input functionality
- **NCO Code Matching**: Connects to backend API to find matching NCO codes
- **Results Display**: Shows detailed match information with scores
- **Export Functionality**: Download results as text files
- **Sharing**: Share results via URL
- **Responsive Design**: Works on desktop and mobile devices
- **Dark/Light Theme**: Toggle between themes
- **Multi-language Support**: Internationalization support

## API Integration

The frontend connects to the backend API at `http://localhost:3000/api/search` with the following specifications:

### Request Format
```json
{
  "text": "Job description text"
}
```

### Response Format
```json
{
  "success": true,
  "data": {
    "success": true,
    "input": "Original job description",
    "topMatch": {
      "title": "Job Title",
      "score": 0.95,
      "metadata": {
        "description": "Job description",
        "division": "Division code",
        "family": "Family code",
        "family_title": "Family title",
        "group": "Group code",
        "nco_code": "NCO code",
        "sub_division": "Sub-division code",
        "title": "Job title"
      }
    }
  }
}
```

## Getting Started

1. **Install Dependencies**:
   ```bash
   npm install
   ```

2. **Start Development Server**:
   ```bash
   npm run dev
   ```

3. **Build for Production**:
   ```bash
   npm run build
   ```

## Backend Requirements

Make sure your backend server is running at `http://localhost:3000` and has the `/api/search` endpoint available.

## Error Handling

The application includes comprehensive error handling for:
- Network connectivity issues
- Invalid API responses
- Server errors
- Missing or invalid data

## Browser Compatibility

- Chrome (recommended)
- Firefox
- Safari
- Edge

## Dependencies

- React 18
- TypeScript
- Tailwind CSS
- Framer Motion
- React Router
- i18next for internationalization
- Lucide React for icons
- React CountUp for animations 