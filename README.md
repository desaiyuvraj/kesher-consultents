from zipfile import ZipFile
import os

# HTML content from the document
html_content = """<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Kesher Consultants</title>
  <style>
    body { font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; margin: 0; padding: 0; background: #f8f9fa; color: #212529; }
    header, footer { background: #1a1a2e; color: white; text-align: center; padding: 30px 20px; }
    nav a { color: white; margin: 0 20px; text-decoration: none; font-weight: 600; font-size: 18px; }
    nav a:hover { text-decoration: underline; }
    section { padding: 60px 20px; max-width: 1100px; margin: auto; }
    .services, .contact { background: #e9ecef; }
    h1, h2 { color: #1a1a2e; font-weight: 800; }
    h1 { font-size: 42px; }
    h2 { font-size: 32px; }
    p, li { font-size: 18px; line-height: 1.6; }
    ul { padding-left: 20px; }
    .contact-info { margin-top: 30px; }
    form input, form textarea { width: 100%; padding: 15px; margin: 15px 0; font-size: 16px; border: 1px solid #ccc; border-radius: 5px; }
    form button { background: #1a1a2e; color: white; border: none; padding: 12px 25px; font-size: 16px; font-weight: bold; cursor: pointer; border-radius: 5px; }
    form button:hover { background: #16213e; }
    footer small { display: block; margin-top: 10px; font-size: 14px; }
  </style>
</head>
<body>

  <header>
    <h1>Kesher Consultants</h1>
    <nav>
      <a href="#home">Home</a>
      <a href="#about">About</a>
      <a href="#services">Services</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <section id="home">
    <h2>Welcome to Kesher Consultants</h2>
    <p>Your trusted partner for buying, selling, or renting property in New Vadaj and beyond.</p>
  </section>

  <section id="about">
    <h2>About Us</h2>
    <p>Kesher Consultants is a trusted real estate consulting firm based in New Vadaj. We specialize in property brokerage, helping clients buy,
