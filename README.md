# URLShield

![URLShield](https://img.shields.io/badge/URLShield-Secure%20URL%20Shortener-blue)
![Version](https://img.shields.io/badge/version-1.0.0-green)
![License](https://img.shields.io/badge/license-ISC-yellow)

**URLShield** is a feature-rich, secure URL shortener with comprehensive analytics and advanced security monitoring capabilities. Built with modern web technologies, it provides detailed insights into link usage while maintaining user privacy and security.

## 🚀 Features

### Core Functionality
- **Secure URL Shortening**: Generate short, memorable links for any URL
- **Link Expiration**: Set custom expiration dates for temporary links
- **User Authentication**: Account-based link management and tracking
- **Session Management**: Secure session handling with cookie-based authentication

### Advanced Analytics
- **Real-time Click Tracking**: Monitor link clicks with timestamp precision
- **Geolocation Intelligence**: Track visitor location down to city level with timezone support
- **Device & Browser Analytics**: Comprehensive client environment detection
- **Network Security Analysis**: VPN, proxy, and Tor detection for enhanced security
- **Visitor Fingerprinting**: Anonymous visitor identification and tracking

### Security Features
- **IP Address Monitoring**: Track and analyze visitor IP addresses
- **Security Threat Detection**: Identify VPN, proxy, and Tor usage
- **Input Sanitization**: Protection against malicious input
- **Encrypted Password Storage**: Secure user authentication with bcrypt

## 🛠️ Technology Stack

### Frontend
- **React 17** - Modern UI library
- **React Router DOM** - Client-side routing
- **Webpack 5** - Module bundling and development server
- **CSS3** - Custom styling

### Backend
- **Node.js** - Server runtime
- **Express.js** - Web application framework
- **PostgreSQL** - Relational database
- **bcrypt** - Password hashing
- **UUID** - Unique identifier generation

### Analytics & APIs
- **IPStack API** - Geolocation and network information
- **VPN Detection API** - Security threat analysis
- **Custom Analytics Engine** - Real-time data processing

## 📊 Analytics Dashboard

URLShield provides comprehensive analytics through multiple data layers:

- **Basic Logs**: IP addresses, timestamps, and basic tracking
- **Location Logs**: Country, region, city, timezone, and coordinates
- **Client Logs**: Browser, OS, device, screen resolution, and hardware specs
- **Network Logs**: ISP information, connection type, and security analysis
- **Session Logs**: User session tracking and account association

## 🚦 Getting Started

### Prerequisites
- Node.js (v14 or higher)
- PostgreSQL (v12 or higher)
- npm or yarn package manager

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/URLShield.git
   cd URLShield
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Database Setup**
   ```bash
   # Create your PostgreSQL database
   createdb urlshield
   
   # Run the database schema
   psql urlshield < scripts.sql
   ```

4. **Environment Configuration**
   Create a `.env` file in the root directory:
   ```env
   DB_HOST=localhost
   DB_PORT=5432
   DB_NAME=urlshield
   DB_USER=your_username
   DB_PASSWORD=your_password
   IPSTACK_API_KEY=your_ipstack_key
   VPN_API_KEY=your_vpn_detection_key
   ```

5. **Start the application**
   ```bash
   # Development mode
   npm run build    # Build frontend assets
   npm start        # Start webpack dev server
   
   # Production mode
   node server/server.js
   ```

## 📖 API Documentation

### URL Management
- `POST /api/shorten` - Create a new short URL
- `GET /api/:shortUrl` - Retrieve URL information
- `GET /api/:shortUrl/analytics` - Get basic analytics
- `GET /api/:shortUrl/extended-analytics` - Get comprehensive analytics

### User Management
- `POST /api/auth/register` - Create new user account
- `POST /api/auth/login` - User authentication
- `GET /api/user/links` - Get user's created links

## 🔒 Privacy & Security

URLShield is designed with privacy and security in mind:

- **Data Encryption**: All sensitive data is encrypted
- **Anonymous Tracking**: Visitor analytics don't store personally identifiable information
- **Secure Sessions**: Cookie-based authentication with secure flags
- **Input Validation**: All inputs are sanitized and validated
- **SQL Injection Protection**: Parameterized queries prevent SQL injection

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the ISC License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

If you encounter any issues or have questions:

1. Check the [Issues](https://github.com/your-username/URLShield/issues) page
2. Create a new issue with detailed information
3. Contact the development team

## 🎯 Roadmap

- [ ] Real-time analytics dashboard
- [ ] API rate limiting
- [ ] Bulk URL shortening
- [ ] Custom domain support
- [ ] Advanced user roles and permissions
- [ ] Integration with popular analytics platforms

---

**URLShield** - Secure, intelligent URL shortening for the modern web.
