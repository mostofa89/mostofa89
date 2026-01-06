<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Abu Hena Mostofa Kamal Joy - Developer Portfolio</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
            background: #0f172a;
            color: #e2e8f0;
            line-height: 1.6;
            min-height: 100vh;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
        }

        .header {
            background: linear-gradient(135deg, #1e293b 0%, #334155 100%);
            padding: 4rem 2rem;
            border-radius: 16px;
            margin-bottom: 3rem;
            border: 1px solid #334155;
            position: relative;
            overflow: hidden;
        }

        .header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(90deg, #3b82f6, #8b5cf6, #ec4899);
        }

        .header-content {
            position: relative;
            z-index: 1;
        }

        .name {
            font-size: 3rem;
            font-weight: 700;
            color: #f8fafc;
            margin-bottom: 0.5rem;
            letter-spacing: -0.5px;
        }

        .title {
            font-size: 1.5rem;
            color: #94a3b8;
            font-weight: 400;
            margin-bottom: 1rem;
        }

        .location {
            color: #64748b;
            font-size: 1rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .section {
            background: #1e293b;
            border-radius: 16px;
            padding: 2.5rem;
            margin-bottom: 2rem;
            border: 1px solid #334155;
            transition: border-color 0.3s ease;
        }

        .section:hover {
            border-color: #475569;
        }

        .section-title {
            font-size: 1.5rem;
            font-weight: 600;
            color: #f8fafc;
            margin-bottom: 1.5rem;
            display: flex;
            align-items: center;
            gap: 0.75rem;
            letter-spacing: -0.3px;
        }

        .section-title::before {
            content: '';
            width: 4px;
            height: 24px;
            background: linear-gradient(180deg, #3b82f6, #8b5cf6);
            border-radius: 2px;
        }

        .connect-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1rem;
        }

        .connect-link {
            display: flex;
            align-items: center;
            gap: 1rem;
            padding: 1rem 1.5rem;
            background: #0f172a;
            border: 1px solid #334155;
            border-radius: 12px;
            color: #e2e8f0;
            text-decoration: none;
            transition: all 0.3s ease;
            font-weight: 500;
        }

        .connect-link:hover {
            background: #1e293b;
            border-color: #3b82f6;
            transform: translateY(-2px);
        }

        .icon {
            font-size: 1.5rem;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(140px, 1fr));
            gap: 1rem;
        }

        .skill-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding: 1.5rem 1rem;
            background: #0f172a;
            border: 1px solid #334155;
            border-radius: 12px;
            transition: all 0.3s ease;
            text-align: center;
        }

        .skill-item:hover {
            border-color: #3b82f6;
            background: #1e293b;
            transform: translateY(-4px);
        }

        .skill-icon {
            font-size: 2.5rem;
            margin-bottom: 0.75rem;
        }

        .skill-name {
            font-size: 0.95rem;
            font-weight: 500;
            color: #cbd5e1;
        }

        .stats-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
        }

        .stat-box {
            background: linear-gradient(135deg, #1e293b 0%, #334155 100%);
            padding: 2rem;
            border-radius: 12px;
            border: 1px solid #334155;
            text-align: center;
            transition: all 0.3s ease;
        }

        .stat-box:hover {
            transform: translateY(-5px);
            border-color: #3b82f6;
        }

        .stat-value {
            font-size: 2.5rem;
            font-weight: 700;
            color: #3b82f6;
            margin-bottom: 0.5rem;
        }

        .stat-label {
            font-size: 1rem;
            color: #94a3b8;
            text-transform: uppercase;
            letter-spacing: 1px;
            font-weight: 500;
        }

        .trophy-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
            gap: 1.5rem;
            text-align: center;
        }

        .trophy-item {
            padding: 1.5rem;
            background: #0f172a;
            border: 1px solid #334155;
            border-radius: 12px;
            transition: all 0.3s ease;
        }

        .trophy-item:hover {
            border-color: #fbbf24;
            transform: scale(1.05);
        }

        .trophy-icon {
            font-size: 3rem;
            margin-bottom: 0.5rem;
        }

        .trophy-name {
            font-size: 0.85rem;
            color: #94a3b8;
            font-weight: 500;
        }

        .quote-section {
            text-align: center;
            padding: 3rem 2rem;
            background: linear-gradient(135deg, #1e293b 0%, #334155 100%);
            border-radius: 16px;
            border: 1px solid #334155;
            margin-top: 2rem;
            position: relative;
        }

        .quote-text {
            font-size: 1.5rem;
            color: #f8fafc;
            font-weight: 500;
            font-style: italic;
            letter-spacing: -0.3px;
        }

        .divider {
            height: 1px;
            background: linear-gradient(90deg, transparent, #334155, transparent);
            margin: 2rem 0;
        }

        @media (max-width: 768px) {
            .name {
                font-size: 2rem;
            }
            
            .title {
                font-size: 1.2rem;
            }
            
            .section {
                padding: 1.5rem;
            }
            
            .container {
                padding: 1rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header class="header">
            <div class="header-content">
                <h1 class="name">Abu Hena Mostofa Kamal Joy</h1>
                <p class="title">Full Stack Developer & Software Engineer</p>
                <p class="location">
                    <span>📍</span>
                    <span>Dhaka, Bangladesh</span>
                </p>
            </div>
        </header>

        <section class="section">
            <h2 class="section-title">Connect</h2>
            <div class="connect-grid">
                <a href="#" class="connect-link">
                    <span class="icon">💼</span>
                    <span>LinkedIn</span>
                </a>
                <a href="#" class="connect-link">
                    <span class="icon">🔗</span>
                    <span>GitHub</span>
                </a>
                <a href="#" class="connect-link">
                    <span class="icon">🐦</span>
                    <span>Twitter</span>
                </a>
                <a href="#" class="connect-link">
                    <span class="icon">📧</span>
                    <span>Email</span>
                </a>
                <a href="#" class="connect-link">
                    <span class="icon">🌐</span>
                    <span>Portfolio</span>
                </a>
            </div>
        </section>

        <section class="section">
            <h2 class="section-title">Technical Skills</h2>
            <div class="skills-grid">
                <div class="skill-item">
                    <div class="skill-icon">🐍</div>
                    <div class="skill-name">Python</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon">⚛️</div>
                    <div class="skill-name">React</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon">📜</div>
                    <div class="skill-name">JavaScript</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon">📘</div>
                    <div class="skill-name">TypeScript</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon">🟢</div>
                    <div class="skill-name">Node.js</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon">🗄️</div>
                    <div class="skill-name">MongoDB</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon">🐘</div>
                    <div class="skill-name">PostgreSQL</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon">🐳</div>
                    <div class="skill-name">Docker</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon">☁️</div>
                    <div class="skill-name">AWS</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon">🔧</div>
                    <div class="skill-name">Git</div>
                </div>
            </div>
        </section>

        <section class="section">
            <h2 class="section-title">GitHub Statistics</h2>
            <div class="stats-container">
                <div class="stat-box">
                    <div class="stat-value">500+</div>
                    <div class="stat-label">Total Contributions</div>
                </div>
                <div class="stat-box">
                    <div class="stat-value">25+</div>
                    <div class="stat-label">Public Projects</div>
                </div>
                <div class="stat-box">
                    <div class="stat-value">1,000+</div>
                    <div class="stat-label">Commits</div>
                </div>
                <div class="stat-box">
                    <div class="stat-value">15+</div>
                    <div class="stat-label">Repositories</div>
                </div>
            </div>
        </section>

        <section class="section">
            <h2 class="section-title">Achievements</h2>
            <div class="trophy-grid">
                <div class="trophy-item">
                    <div class="trophy-icon">🏆</div>
                    <div class="trophy-name">Top Contributor</div>
                </div>
                <div class="trophy-item">
                    <div class="trophy-icon">⭐</div>
                    <div class="trophy-name">Popular Repo</div>
                </div>
                <div class="trophy-item">
                    <div class="trophy-icon">🎯</div>
                    <div class="trophy-name">Streak Master</div>
                </div>
                <div class="trophy-item">
                    <div class="trophy-icon">💎</div>
                    <div class="trophy-name">Code Quality</div>
                </div>
                <div class="trophy-item">
                    <div class="trophy-icon">🚀</div>
                    <div class="trophy-name">Quick Learner</div>
                </div>
            </div>
        </section>

        <div class="quote-section">
            <p class="quote-text">"Code. Learn. Build. Repeat."</p>
        </div>
    </div>
</body>
</html>






