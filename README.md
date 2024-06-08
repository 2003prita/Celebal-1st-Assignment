# Celebal-1st-Assignment
import React, { useState } from 'react';

const BasicForm = () => {
  const [formData, setFormData] = useState({
    firstName: '',
    lastName: '',
    username: '',
    email: '',
    password: '',
    phone: {
      countryCode: '',
      number: ''
    },
    country: '',
    city: '',
    panNo: '',
    aadharNo: ''
  });

  const handleChange = (e) => {
    const { name, value } = e.target;
    setFormData({
      ...formData,
      [name]: value
    });
  };

  return (
    <form>
      <div>
        <label htmlFor="firstName">First Name:</label>
        <input
          type="text"
          id="firstName"
          name="firstName"
          value={formData.firstName}
          onChange={handleChange}
        />
      </div>
      <div>
        <label htmlFor="lastName">Last Name:</label>
        <input
          type="text"
          id="lastName"
          name="lastName"
          value={formData.lastName}
          onChange={handleChange}
        />
      </div>
      <div>
        <label htmlFor="username">Username:</label>
        <input
          type="text"
          id="username"
          name="username"
          value={formData.username}
          onChange={handleChange}
        />
      </div>
      <div>
        <label htmlFor="email">E-mail:</label>
        <input
          type="email"
          id="email"
          name="email"
          value={formData.email}
          onChange={handleChange}
        />
      </div>
      <div>
        <label htmlFor="password">Password:</label>
        <input
          type="password"
          id="password"
          name="password"
          value={formData.password}
          onChange={handleChange}
        />
      </div>
      <div>
        <label htmlFor="phone">Phone Number:</label>
        <input
          type="text"
          id="countryCode"
          name="countryCode"
          placeholder="Country Code"
          value={formData.phone.countryCode}
          onChange={handleChange}
        />
        <input
          type="text"
          id="number"
          name="number"
          placeholder="Phone Number"
          value={formData.phone.number}
          onChange={handleChange}
        />
      </div>
      <div>
        <label htmlFor="country">Country:</label>
        <select
          id="country"
          name="country"
          value={formData.country}
          onChange={handleChange}
        >
          <option value="">Select Country</option>
          {/* Add options for countries */}
        </select>
      </div>
      <div>
        <label htmlFor="city">City:</label>
        <select
          id="city"
          name="city"
          value={formData.city}
          onChange={handleChange}
        >
          <option value="">Select City</option>
          {/* Add options for cities */}
        </select>
      </div>
      <div>
        <label htmlFor="panNo">Pan No.:</label>
        <input
          type="text"
          id="panNo"
          name="panNo"
          value={formData.panNo}
          onChange={handleChange}
        />
      </div>
      <div>
        <label htmlFor="aadharNo">Aadhar No.:</label>
        <input
          type="text"
          id="aadharNo"
          name="aadharNo"
          value={formData.aadharNo}
          onChange={handleChange}
        />
      </div>
    </form>
  );
};

export default BasicForm;
