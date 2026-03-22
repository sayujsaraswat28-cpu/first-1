# first-1

Action: file_editor create /app/memory/PRD.md --file-text "# Cafe La Foresta - Product Requirements Document

## Project Overview
A modern, elegant website for Cafe La Foresta - a nature-inspired café that blends forest aesthetics with a cozy, premium dining experience.

## Original Problem Statement
Design a website featuring:
- Calming color palette (deep greens, earthy browns, warm beige, soft cream)
- Natural textures (wood, leaves, soft lighting)
- Full sections: Homepage, About, Menu, Gallery, Reservations, Contact
- Features: Dark/light mode toggle, online ordering button, testimonials, Instagram feed
- Minimalist yet warm design with smooth scrolling and subtle animations

## User Personas
1. **Nature Lovers**: Seeking peaceful, eco-conscious dining experiences
2. **Health-Conscious Diners**: Looking for organic, fresh, locally sourced food
3. **Social Media Enthusiasts**: Want Instagram-worthy café experiences
4. **Event Planners**: Need group booking options for gatherings

## Architecture & Tech Stack
- **Frontend**: React 19, Tailwind CSS, Shadcn UI components
- **Backend**: FastAPI (Python), MongoDB with Motor (async)
- **State Management**: React Hooks
- **Styling**: Custom CSS with natural color palette
- **Features**: Responsive design, dark/light mode, smooth scrolling

---

## Implementation Status (December 2025)

### ✅ Phase 1: Frontend with Mock Data (Completed - Dec 22, 2025)

**Implemented Components:**
1. **Header Component** - Sticky navigation with theme toggle, smooth scroll
2. **Hero Section** - Full-screen hero with forest café image, dual CTAs
3. **About Section** - Story narrative with forest image, 3 value cards
4. **Menu Section** - Tabbed interface (Coffee, Tea, Bakery, Meals) with image cards
5. **Gallery Section** - 3x2 grid with lightbox modal functionality
6. **Testimonials Section** - Customer reviews with 5-star ratings
7. **Reservations Section** - Form with date/time pickers, guest count dropdown
8. **Instagram Feed** - Mock Instagram grid (6 posts)
9. **Contact Section** - Contact form + Google Maps iframe + info cards
10. **Footer** - Multi-column layout with links, social media, contact info

**Mock Data File**: `/app/frontend/src/mockData.js`
- Menu items (coffee, tea, bakery, meals) with images, prices, descriptions
- Gallery images (6 café interior/food photos)
- Testimonials (3 customer reviews)
- Instagram posts (6 mock posts)

**Design Features:**
- ✓ Emerald green (#059669) primary color
- ✓ Light/dark mode toggle
- ✓ Serif fonts for headings, sans-serif for body
- ✓ Smooth scroll navigation
- ✓ Hover animations on cards
- ✓ Responsive grid layouts
- ✓ Toast notifications (Sonner)
- ✓ Custom scrollbar styling

---

## API Contracts (For Backend Implementation)

### 1. Reservations API
**POST /api/reservations**
```json
Request: {
  \"name\": \"string\",
  \"email\": \"string\",
  \"phone\": \"string\",
  \"date\": \"YYYY-MM-DD\",
  \"time\": \"HH:MM\",
  \"guests\": \"number\"
}
Response: {
  \"id\": \"string\",
  \"status\": \"confirmed\",
  \"message\": \"Reservation confirmed\",
  \"reservation\": { ...request data }
}
```

**GET /api/reservations** (Admin)
- Returns list of all reservations

### 2. Contact Form API
**POST /api/contact**
```json
Request: {
  \"name\": \"string\",
  \"email\": \"string\",
  \"subject\": \"string\",
  \"message\": \"string\"
}
Response: {
  \"success\": true,
  \"message\": \"Message received\"
}
```

### 3. Menu Items API
**GET /api/menu**
```json
Response: {
  \"coffee\": [...],
  \"tea\": [...],
  \"bakery\": [...],
  \"meals\": [...]
}
```

### 4. Instagram Feed API
**GET /api/instagram**
- Integrate with Instagram Basic Display API
- Return recent posts with images and links

---

## Prioritized Backlog

### P0 - Critical (Next Phase)
- [ ] Backend API implementation (MongoDB models, FastAPI endpoints)
- [ ] Reservations database storage and retrieval
- [ ] Contact form submission and email notifications
- [ ] Frontend-backend integration (remove mock data)
- [ ] Form validation and error handling

### P1 - High Priority
- [ ] Instagram API integration (replace mock feed)
- [ ] Google Maps API integration (replace iframe with interactive map)
- [ ] Admin dashboard for managing reservations
- [ ] Email confirmations for reservations
- [ ] Menu management system (add/edit/delete items)

### P2 - Nice to Have
- [ ] Online ordering system integration
- [ ] Payment gateway (Stripe/PayPal)
- [ ] User accounts and order history
- [ ] Newsletter subscription
- [ ] Analytics integration (Google Analytics)
- [ ] SEO optimization
- [ ] Performance optimization (image lazy loading)

---

## Next Action Items
1. **Backend Development**: Create MongoDB models for reservations and contacts
2. **API Endpoints**: Implement FastAPI routes for all forms
3. **Integration**: Connect frontend forms to backend APIs
4. **Testing**: End-to-end testing of all features
5. **External Integrations**: Instagram Feed and Google Maps APIs

---

## Technical Notes
- All mock data currently in `/app/frontend/src/mockData.js`
- Forms use client-side validation (HTML5 required fields)
- Toast notifications ready for backend success/error messages
- Dark mode state managed via React useState + localStorage potential
- Smooth scroll implemented with native CSS scroll-behavior

## Success Metrics
- Page load time < 3 seconds
- Mobile responsive (all breakpoints)
- Accessibility score > 90
- User engagement: Avg session > 2 minutes
- Reservation conversion rate target: 15%
"
Observation: Create successful: /app/memory/PRD.md
