<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BLISS eduPower</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: #f0f2f5;
            max-width: 420px;
            margin: 0 auto;
            overflow-x: hidden;
        }
        
        .app-container {
            background: white;
            min-height: 100vh;
        }
        
        .header {
            background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
            color: white;
            padding: 30px 20px;
            text-align: center;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0,0,0,0.2);
        }
        
        .header h1 {
            font-size: 1.8em;
            margin-bottom: 5px;
        }
        
        .header .tagline {
            font-size: 0.9em;
            font-style: italic;
            opacity: 0.95;
            margin-bottom: 10px;
        }
        
        .header .address {
            font-size: 0.75em;
            opacity: 0.9;
            line-height: 1.4;
        }
        
        .content {
            padding: 15px;
        }
        
        .section {
            background: white;
            padding: 15px;
            margin-bottom: 15px;
            border-radius: 12px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.08);
        }
        
        .section h2 {
            color: #1e3c72;
            margin-bottom: 12px;
            font-size: 1.3em;
            border-bottom: 2px solid #2a5298;
            padding-bottom: 8px;
        }
        
        .section h3 {
            color: #2a5298;
            margin-top: 15px;
            margin-bottom: 12px;
            font-size: 1.1em;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .section p, .section li {
            color: #333;
            line-height: 1.5;
            margin-bottom: 8px;
            font-size: 0.9em;
        }
        
        .section ul {
            margin-left: 20px;
        }
        
        .course-card {
            background: #f8f9fa;
            padding: 12px;
            border-radius: 10px;
            margin-bottom: 10px;
            border-left: 4px solid #667eea;
            display: flex;
            gap: 12px;
            align-items: start;
        }
        
        .course-icon {
            font-size: 2em;
            flex-shrink: 0;
        }
        
        .course-content {
            flex: 1;
        }
        
        .course-card h4 {
            color: #1e3c72;
            margin-bottom: 5px;
            font-size: 1em;
        }
        
        .course-card p {
            font-size: 0.85em;
            color: #555;
            margin-bottom: 8px;
        }
        
        .course-card .price {
            color: #28a745;
            font-weight: bold;
            font-size: 1em;
        }
        
        .discount-badge {
            background: #ff4757;
            color: white;
            padding: 3px 8px;
            border-radius: 4px;
            font-size: 0.75em;
            display: inline-block;
            margin-left: 5px;
        }
        
        .learning-modes {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 15px;
            border-radius: 10px;
            margin-top: 12px;
        }
        
        .learning-modes h3 {
            color: white;
            margin-bottom: 12px;
            border: none;
        }
        
        .mode-item {
            background: rgba(255,255,255,0.15);
            padding: 12px;
            border-radius: 8px;
            margin-bottom: 10px;
            backdrop-filter: blur(10px);
        }
        
        .mode-item h4 {
            margin-bottom: 8px;
            font-size: 1em;
        }
        
        .mode-item p {
            color: white;
            font-size: 0.85em;
        }
        
        .perks-grid {
            display: grid;
            grid-template-columns: 1fr;
            gap: 10px;
            margin-top: 12px;
        }
        
        .perk-item {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 12px;
            border-radius: 8px;
            display: flex;
            align-items: center;
            gap: 12px;
        }
        
        .perk-icon {
            font-size: 1.5em;
            flex-shrink: 0;
        }
        
        .perk-content h4 {
            margin-bottom: 4px;
            font-size: 0.95em;
        }
        
        .perk-content p {
            font-size: 0.8em;
            color: rgba(255,255,255,0.9);
        }
        
        .footer {
            background: #1e3c72;
            color: white;
            padding: 20px;
            text-align: center;
        }
        
        .footer h2 {
            margin-bottom: 15px;
            font-size: 1.3em;
            color: white;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            margin-bottom: 10px;
            font-size: 0.9em;
        }
        
        .cta {
            margin-top: 15px;
            font-size: 1em;
            font-weight: bold;
        }
        
        .nav-tabs {
            display: flex;
            gap: 5px;
            margin-bottom: 15px;
            overflow-x: auto;
            padding: 5px 0;
        }
        
        .nav-tab {
            background: #f0f2f5;
            border: none;
            padding: 8px 15px;
            border-radius: 20px;
            font-size: 0.85em;
            cursor: pointer;
            white-space: nowrap;
            transition: all 0.3s;
        }
        
        .nav-tab.active {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
        }
    </style>
</head>
<body>
    <div class="app-container">
        <div class="header">
            <h1>🎓 BLISS eduPower</h1>
            <p class="tagline">Unleash the Power of Education...</p>
            <p class="address">📍 #235 BEML Layout, 2nd Stage, R.R. Nagar, Sharda Devi Nagar, Dattagalli, Mysuru-570023</p>
        </div>
        
        <div class="content">
            <div class="section">
                <h2>📚 Learning Modes</h2>
                <div class="learning-modes">
                    <h3>🎯 Flexible Learning Options</h3>
                    <div class="mode-item">
                        <h4>🏢 Offline Classes</h4>
                        <p>Face-to-face interactive sessions at our institute with hands-on practice in our computer labs.</p>
                    </div>
                    <div class="mode-item">
                        <h4>💻 Online Classes</h4>
                        <p>Live interactive online sessions from anywhere with recorded lectures and virtual lab access.</p>
                    </div>
                    <p style="margin-top: 12px; text-align: center; font-weight: bold;">Choose what suits your schedule!</p>
                </div>
            </div>
            
            <div class="section">
                <h2>👥 Who Can Join?</h2>
                <ul>
                    <li>✅ Diploma in CS students</li>
                    <li>✅ BCA students</li>
                    <li>✅ BSc Computer Science</li>
                    <li>✅ Engineering (CSE, ISE, ECE)</li>
                    <li>✅ PUC (PCMC) students</li>
                    <li>✅ School students</li>
                    <li>✅ Tech enthusiasts</li>
                </ul>
            </div>
            
            <div class="section">
                <h2>📖 Our Courses</h2>
                
                <h3>🌐 Web Development</h3>
                
                <div class="course-card">
                    <div class="course-icon">📄</div>
                    <div class="course-content">
                        <h4>HTML5 & CSS3</h4>
                        <p>Build stunning web pages with modern styling techniques.</p>
                        <div class="price">₹4,500</div>
                    </div>
                </div>
                
                <div class="course-card">
                    <div class="course-icon">⚡</div>
                    <div class="course-content">
                        <h4>JavaScript</h4>
                        <p>Dynamic programming for interactive websites.</p>
                        <div class="price">₹5,200</div>
                    </div>
                </div>
                
                <div class="course-card">
                    <div class="course-icon">⚛️</div>
                    <div class="course-content">
                        <h4>React.js</h4>
                        <p>Build modern UI and single-page applications.</p>
                        <div class="price">₹6,500 <span class="discount-badge">15% OFF</span></div>
                    </div>
                </div>
                
                <div class="course-card">
                    <div class="course-icon">🚀</div>
                    <div class="course-content">
                        <h4>Full Stack Development</h4>
                        <p>Complete web development - frontend to backend.</p>
                        <div class="price">₹7,800 <span class="discount-badge">15% OFF</span></div>
                    </div>
                </div>
                
                <h3>💻 Programming Languages</h3>
                
                <div class="course-card">
                    <div class="course-icon">🐍</div>
                    <div class="course-content">
                        <h4>Python Programming</h4>
                        <p>From basics to advanced OOP and applications.</p>
                        <div class="price">₹4,500</div>
                    </div>
                </div>
                
                <div class="course-card">
                    <div class="course-icon">©️</div>
                    <div class="course-content">
                        <h4>C Programming</h4>
                        <p>Programming fundamentals with C language.</p>
                        <div class="price">₹4,500</div>
                    </div>
                </div>
                
                <div class="course-card">
                    <div class="course-icon">➕</div>
                    <div class="course-content">
                        <h4>C++ Programming</h4>
                        <p>Object-oriented programming with modern C++.</p>
                        <div class="price">₹5,000</div>
                    </div>
                </div>
                
                <div class="course-card">
                    <div class="course-icon">☕</div>
                    <div class="course-content">
                        <h4>Java Programming</h4>
                        <p>Core Java, OOP, collections, and enterprise apps.</p>
                        <div class="price">₹5,200</div>
                    </div>
                </div>
                
                <div class="course-card">
                    <div class="course-icon">🔷</div>
                    <div class="course-content">
                        <h4>C# & .NET</h4>
                        <p>Windows applications and web services with .NET.</p>
                        <div class="price">₹5,800</div>
                    </div>
                </div>
                
                <div class="course-card">
                    <div class="course-icon">🐘</div>
                    <div class="course-content">
                        <h4>PHP & MySQL</h4>
                        <p>Server-side scripting and database management.</p>
                        <div class="price">₹5,500</div>
                    </div>
                </div>
                
                <h3>🔬 Advanced Topics</h3>
                
                <div class="course-card">
                    <div class="course-icon">🔗</div>
                    <div class="course-content">
                        <h4>Data Structures & Algorithms</h4>
                        <p>Essential DSA for interviews and coding competitions.</p>
                        <div class="price">₹6,200</div>
                    </div>
                </div>
                
                <div class="course-card">
                    <div class="course-icon">💾</div>
                    <div class="course-content">
                        <h4>Database Management (DBMS)</h4>
                        <p>SQL, database design, and normalization.</p>
                        <div class="price">₹5,500</div>
                    </div>
                </div>
                
                <div class="course-card">
                    <div class="course-icon">⚙️</div>
                    <div class="course-content">
                        <h4>Software Engineering</h4>
                        <p>SDLC, design patterns, and project management.</p>
                        <div class="price">₹6,000</div>
                    </div>
                </div>
                
                <div class="course-card">
                    <div class="course-icon">🤖</div>
                    <div class="course-content">
                        <h4>Artificial Intelligence & ML</h4>
                        <p>AI concepts, ML algorithms, and practical tools.</p>
                        <div class="price">₹7,500 <span class="discount-badge">25% OFF</span></div>
                    </div>
                </div>
                
                <div class="course-card">
                    <div class="course-icon">🖥️</div>
                    <div class="course-content">
                        <h4>Operating Systems</h4>
                        <p>OS concepts, process & memory management.</p>
                        <div class="price">₹5,000</div>
                    </div>
                </div>
                
                <div class="course-card">
                    <div class="course-icon">🌐</div>
                    <div class="course-content">
                        <h4>Computer Networking</h4>
                        <p>Network protocols, security, and configuration.</p>
                        <div class="price">₹5,500</div>
                    </div>
                </div>
                
                <div class="course-card">
                    <div class="course-icon">🔒</div>
                    <div class="course-content">
                        <h4>Cyber Security & Tools</h4>
                        <p>Network security, ethical hacking, and cryptography.</p>
                        <div class="price">₹7,000 <span class="discount-badge">20% OFF</span></div>
                    </div>
                </div>
                
                <div class="course-card">
                    <div class="course-icon">📐</div>
                    <div class="course-content">
                        <h4>Mathematical Foundations</h4>
                        <p>Discrete math, logic, and algorithm analysis.</p>
                        <div class="price">₹5,200</div>
                    </div>
                </div>
                
                <h3>☁️ IoT & Cloud</h3>
                
                <div class="course-card">
                    <div class="course-icon">🌐</div>
                    <div class="course-content">
                        <h4>Internet of Things (IoT)</h4>
                        <p>IoT fundamentals, Arduino, Raspberry Pi, sensors.</p>
                        <div class="price">₹6,800</div>
                    </div>
                </div>
                
                <div class="course-card">
                    <div class="course-icon">☁️</div>
                    <div class="course-content">
                        <h4>Cloud Computing</h4>
                        <p>AWS, Azure, Google Cloud platforms & deployment.</p>
                        <div class="price">₹7,200 <span class="discount-badge">18% OFF</span></div>
                    </div>
                </div>
                
                <h3>🎨 Design & Tools</h3>
                
                <div class="course-card">
                    <div class="course-icon">🎨</div>
                    <div class="course-content">
                        <h4>UI/UX Design</h4>
                        <p>Design principles, wireframing, and prototyping.</p>
                        <div class="price">₹6,000</div>
                    </div>
                </div>
                
                <div class="course-card">
                    <div class="course-icon">🔀</div>
                    <div class="course-content">
                        <h4>Git & GitHub</h4>
                        <p>Version control and open-source collaboration.</p>
                        <div class="price">₹3,500</div>
                    </div>
                </div>
                
                <div class="course-card">
                    <div class="course-icon">📊</div>
                    <div class="course-content">
                        <h4>Microsoft Office</h4>
                        <p>Word, PowerPoint, Outlook for productivity.</p>
                        <div class="price">₹4,500</div>
                    </div>
                </div>
                
                <div class="course-card">
                    <div class="course-icon">📈</div>
                    <div class="course-content">
                        <h4>Excel Advanced</h4>
                        <p>Formulas, pivot tables, macros, VBA, analysis.</p>
                        <div class="price">₹5,000</div>
                    </div>
                </div>
                
                <div class="course-card">
                    <div class="course-icon">📊</div>
                    <div class="course-content">
                        <h4>R Programming</h4>
                        <p>Statistical computing and data analysis.</p>
                        <div class="price">₹5,500</div>
                    </div>
                </div>
                
                <div class="course-card">
                    <div class="course-icon">💻</div>
                    <div class="course-content">
                        <h4>Fundamentals of Computers</h4>
                        <p>Computer basics, hardware, software, digital literacy.</p>
                        <div class="price">₹4,500</div>
                    </div>
                </div>
            </div>
            
            <div class="section">
                <h2>🌟 Exclusive Benefits</h2>
                <div class="perks-grid">
                    <div class="perk-item">
                        <div class="perk-icon">📄</div>
                        <div class="perk-content">
                            <h4>Resume Building</h4>
                            <p>Professional resume creation & optimization</p>
                        </div>
                    </div>
                    <div class="perk-item">
                        <div class="perk-icon">💼</div>
                        <div class="perk-content">
                            <h4>LinkedIn Profile</h4>
                            <p>Build strong professional presence</p>
                        </div>
                    </div>
                    <div class="perk-item">
                        <div class="perk-icon">🏆</div>
                        <div class="perk-content">
                            <h4>Hackathons</h4>
                            <p>Regular coding competitions access</p>
                        </div>
                    </div>
                    <div class="perk-item">
                        <div class="perk-icon">🚀</div>
                        <div class="perk-content">
                            <h4>Live Projects</h4>
                            <p>Hands-on real-world project experience</p>
                        </div>
                    </div>
                    <div class="perk-item">
                        <div class="perk-icon">🎯</div>
                        <div class="perk-content">
                            <h4>Interview Prep</h4>
                            <p>Mock interviews & coding challenges</p>
                        </div>
                    </div>
                    <div class="perk-item">
                        <div class="perk-icon">📜</div>
                        <div class="perk-content">
                            <h4>Certifications</h4>
                            <p>Industry-recognized certificates</p>
                        </div>
                    </div>
                    <div class="perk-item">
                        <div class="perk-icon">👥</div>
                        <div class="perk-content">
                            <h4>Mentorship</h4>
                            <p>One-on-one guidance from experts</p>
                        </div>
                    </div>
                    <div class="perk-item">
                        <div class="perk-icon">💻</div>
                        <div class="perk-content">
                            <h4>Practical Labs</h4>
                            <p>Fully equipped computer labs</p>
                        </div>
                    </div>
                    <div class="perk-item">
                        <div class="perk-icon">🌐</div>
                        <div class="perk-content">
                            <h4>Job Assistance</h4>
                            <p>Career guidance & placement support</p>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="section">
                <h2>🎁 Special Offers</h2>
                <ul>
                    <li>🎉 <strong>Early Bird:</strong> 20% off in first week</li>
                    <li>👥 <strong>Group Discount:</strong> 15% off for 3+ students</li>
                    <li>🎓 <strong>Student Special:</strong> Extra 10% off with ID</li>
                    <li>📚 <strong>Bundle Offer:</strong> Buy 2, get 3rd at 50% off</li>
                    <li>🔄 <strong>Referral Bonus:</strong> ₹500 cashback per referral</li>
                </ul>
            </div>
            
            <div class="section">
                <h2>✨ Why Choose Us?</h2>
                <ul>
                    <li>✨ Industry-expert instructors</li>
                    <li>✨ Small batch sizes</li>
                    <li>✨ Flexible timings</li>
                    <li>✨ Updated curriculum</li>
                    <li>✨ Lifetime course access</li>
                    <li>✨ Project-based learning</li>
                    <li>✨ Regular competitions</li>
                    <li>✨ Alumni network</li>
                </ul>
            </div>
        </div>
        
        <div class="footer">
            <h2>📞 Contact Us</h2>
            <div class="contact-item">
                <span>📱</span>
                <span>+91 9449344298</span>
            </div>
            <div class="contact-item">
                <span>📱</span>
                <span>+91 9916777925</span>
            </div>
            <div class="contact-item">
                <span>📱</span>
                <span>+91 8095155552</span>
            </div>
            <p class="cta">🚀 Start Your Coding Journey Today!</p>
            <p style="margin-top: 10px; font-size: 0.9em;">Limited seats - Enroll now!</p>
        </div>
    </div>
</body>
</html>
