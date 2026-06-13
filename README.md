<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ayush Sharma - AI/ML Engineer & Cloud Architect</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary: #00D68F;
            --secondary: #4285F4;
            --dark: #0D1117;
            --darker: #1a1a2e;
            --text: #e9ecef;
            --text-muted: #adb5bd;
            --accent: #FF6B6B;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
            background: linear-gradient(135deg, var(--dark) 0%, var(--darker) 100%);
            color: var(--text);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* ANIMATIONS */
        @keyframes slideInDown {
            from {
                opacity: 0;
                transform: translateY(-50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes slideInUp {
            from {
                opacity: 0;
                transform: translateY(50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        @keyframes typewriter {
            from {
                width: 0;
                opacity: 0;
            }
            to {
                width: 100%;
                opacity: 1;
            }
        }

        @keyframes pulse {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.7; }
        }

        @keyframes shimmer {
            0% { background-position: -1000px 0; }
            100% { background-position: 1000px 0; }
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
        }

        /* HEADER */
        header {
            min-height: 90vh;
            background: linear-gradient(135deg, #0D1117 0%, #1a3a52 50%, var(--primary) 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
        }

        header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: radial-gradient(circle at 20% 50%, rgba(66, 133, 244, 0.15) 0%, transparent 50%),
                        radial-gradient(circle at 80% 80%, rgba(0, 214, 143, 0.1) 0%, transparent 50%);
            pointer-events: none;
        }

        .header-content {
            text-align: center;
            z-index: 2;
            animation: slideInDown 1s ease-out;
        }

        h1 {
            font-size: clamp(3rem, 8vw, 5rem);
            font-weight: 900;
            margin-bottom: 10px;
            letter-spacing: -2px;
            background: linear-gradient(135deg, #fff, var(--primary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .subtitle {
            font-size: clamp(1rem, 3vw, 1.5rem);
            color: var(--primary);
            margin-bottom: 30px;
            font-weight: 300;
            animation: slideInUp 1s ease-out 0.2s both;
        }

        .tagline {
            font-size: 1.1rem;
            color: var(--text-muted);
            max-width: 600px;
            margin: 0 auto 40px;
            animation: slideInUp 1s ease-out 0.4s both;
        }

        /* CTA BUTTONS */
        .cta-group {
            display: flex;
            gap: 15px;
            justify-content: center;
            flex-wrap: wrap;
            animation: slideInUp 1s ease-out 0.6s both;
        }

        .btn {
            padding: 14px 28px;
            border-radius: 8px;
            border: 2px solid transparent;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 8px;
        }

        .btn-primary {
            background: var(--primary);
            color: var(--dark);
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 30px rgba(0, 214, 143, 0.3);
        }

        .btn-secondary {
            background: transparent;
            color: var(--text);
            border-color: var(--text);
        }

        .btn-secondary:hover {
            background: rgba(233, 236, 239, 0.1);
            border-color: var(--primary);
            color: var(--primary);
        }

        /* METRICS SECTION */
        .metrics {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-top: 60px;
            padding: 0 20px;
        }

        .metric {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            padding: 25px;
            border-radius: 12px;
            border: 1px solid rgba(0, 214, 143, 0.2);
            text-align: center;
            animation: slideInUp 1s ease-out;
            transition: all 0.3s ease;
        }

        .metric:hover {
            border-color: var(--primary);
            background: rgba(0, 214, 143, 0.1);
            transform: translateY(-5px);
        }

        .metric-number {
            font-size: 2.5rem;
            font-weight: 900;
            color: var(--primary);
            margin-bottom: 5px;
        }

        .metric-label {
            font-size: 0.95rem;
            color: var(--text-muted);
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        /* CONTAINER */
        .container {
            max-width: 1000px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* SECTIONS */
        section {
            padding: 80px 0;
            border-bottom: 1px solid rgba(0, 214, 143, 0.1);
        }

        section:last-child {
            border-bottom: none;
        }

        section h2 {
            font-size: 2.5rem;
            margin-bottom: 40px;
            display: flex;
            align-items: center;
            gap: 12px;
        }

        section h2::before {
            content: '';
            width: 4px;
            height: 40px;
            background: linear-gradient(180deg, var(--primary), transparent);
            border-radius: 2px;
        }

        /* EXPERIENCE CARDS */
        .experience-card {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(0, 214, 143, 0.1);
            border-radius: 12px;
            padding: 30px;
            margin-bottom: 25px;
            transition: all 0.3s ease;
            animation: slideInUp 0.8s ease-out;
        }

        .experience-card:hover {
            background: rgba(0, 214, 143, 0.08);
            border-color: var(--primary);
            transform: translateX(5px);
        }

        .exp-title {
            font-size: 1.5rem;
            color: var(--primary);
            margin-bottom: 5px;
            font-weight: 700;
        }

        .exp-company {
            font-size: 0.95rem;
            color: var(--text-muted);
            margin-bottom: 15px;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .exp-description {
            font-size: 1rem;
            line-height: 1.8;
            color: var(--text);
            margin-bottom: 15px;
        }

        .exp-highlights {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 10px;
        }

        .highlight {
            background: rgba(66, 133, 244, 0.1);
            padding: 10px 15px;
            border-radius: 6px;
            font-size: 0.9rem;
            color: var(--secondary);
            border-left: 3px solid var(--secondary);
        }

        /* TECH STACK */
        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 15px;
        }

        .tech-item {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(66, 133, 244, 0.3);
            padding: 15px;
            border-radius: 8px;
            text-align: center;
            font-weight: 500;
            transition: all 0.3s ease;
            cursor: default;
        }

        .tech-item:hover {
            background: rgba(66, 133, 244, 0.15);
            border-color: var(--secondary);
            transform: translateY(-3px);
        }

        /* STATS */
        .stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
            gap: 20px;
            margin: 40px 0;
        }

        .stat-box {
            background: rgba(0, 214, 143, 0.05);
            border: 2px solid var(--primary);
            border-radius: 12px;
            padding: 25px;
            text-align: center;
        }

        .stat-number {
            font-size: 2rem;
            font-weight: 900;
            color: var(--primary);
            margin-bottom: 5px;
        }

        .stat-text {
            font-size: 0.9rem;
            color: var(--text-muted);
        }

        /* FOOTER */
        footer {
            background: rgba(0, 0, 0, 0.3);
            padding: 50px 0;
            border-top: 1px solid rgba(0, 214, 143, 0.1);
            text-align: center;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
            margin: 30px 0;
        }

        .social-link {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 45px;
            height: 45px;
            border-radius: 50%;
            background: rgba(66, 133, 244, 0.1);
            border: 2px solid var(--secondary);
            color: var(--secondary);
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
        }

        .social-link:hover {
            background: var(--secondary);
            color: white;
            transform: translateY(-3px);
        }

        /* RESPONSIVE */
        @media (max-width: 768px) {
            h1 { font-size: 2.5rem; }
            section h2 { font-size: 1.8rem; }
            .metrics { grid-template-columns: 1fr 1fr; }
            .cta-group { flex-direction: column; align-items: center; }
            .btn { width: 100%; justify-content: center; }
        }

        /* SCROLL ANIMATION */
        .fade-in {
            animation: fadeIn 0.8s ease-out;
        }

        /* DIVIDER */
        .divider {
            height: 2px;
            background: linear-gradient(90deg, transparent, var(--primary), transparent);
            margin: 60px 0;
        }
    </style>
</head>
<body>
    <!-- HEADER -->
    <header>
        <div class="header-content">
            <h1>AYUSH SHARMA</h1>
            <p class="subtitle">AI/ML Engineer • Cloud Architect • Community Builder</p>
            <p class="tagline">Building RAG systems at scale • Mentored 4,000+ • Founder of 5,000+ community</p>
            
            <div class="cta-group">
                <a href="mailto:ayush.sharmaa@hotmail.com" class="btn btn-primary">💬 Email Me</a>
                <a href="https://linkedin.com/in/ayushh-sharmaa" class="btn btn-secondary">LinkedIn</a>
                <a href="https://github.com/Ayushh-Sharmaa" class="btn btn-secondary">GitHub</a>
            </div>

            <div class="metrics">
                <div class="metric">
                    <div class="metric-number">5000+</div>
                    <div class="metric-label">Community Members</div>
                </div>
                <div class="metric">
                    <div class="metric-number">4000+</div>
                    <div class="metric-label">Learners Mentored</div>
                </div>
                <div class="metric">
                    <div class="metric-number">155K</div>
                    <div class="metric-label">GCP Points</div>
                </div>
                <div class="metric">
                    <div class="metric-number">200+</div>
                    <div class="metric-label">MVPs Shipped</div>
                </div>
            </div>
        </div>
    </header>

    <div class="container">
        <!-- CURRENT STATUS -->
        <section>
            <h2>🎯 Open To Opportunities</h2>
            <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 20px;">
                <div class="stat-box">
                    <div class="stat-number">Internship</div>
                    <div class="stat-text">Jun • Jul • Aug 2026</div>
                </div>
                <div class="stat-box">
                    <div class="stat-number">Full-Time</div>
                    <div class="stat-text">After Aug 2029</div>
                </div>
                <div class="stat-box">
                    <div class="stat-number">Flexible</div>
                    <div class="stat-text">Remote • On-site • Hybrid</div>
                </div>
            </div>
        </section>

        <div class="divider"></div>

        <!-- EXPERIENCE -->
        <section>
            <h2>💼 Professional Experience</h2>
            
            <div class="experience-card">
                <div class="exp-title">Google Student Ambassador 2026</div>
                <div class="exp-company">Google • Apr 2026 - Present</div>
                <div class="exp-description">
                    Selected from thousands of global applicants to represent Google's ecosystem at scale.
                </div>
                <div class="exp-highlights">
                    <div class="highlight">500+ Students Trained</div>
                    <div class="highlight">5 Technical Workshops</div>
                    <div class="highlight">GDG Partnerships</div>
                    <div class="highlight">North India Bootcamp</div>
                </div>
            </div>

            <div class="experience-card">
                <div class="exp-title">Global Society of Founders</div>
                <div class="exp-company">Founder • Jan 2026 - Present</div>
                <div class="exp-description">
                    Execution-first community scaled to 5,000+ members in 5 months with zero paid marketing.
                </div>
                <div class="exp-highlights">
                    <div class="highlight">0 → 5,000 Members</div>
                    <div class="highlight">200+ MVPs Shipped</div>
                    <div class="highlight">15 Countries</div>
                    <div class="highlight">40% Monthly Engagement</div>
                </div>
            </div>

            <div class="experience-card">
                <div class="exp-title">NexaSphere Campus Ecosystem</div>
                <div class="exp-company">Founder & Organizer • Feb 2026 - Present</div>
                <div class="exp-description">
                    Student-led tech ecosystem with 300+ members across 5 technical tracks.
                </div>
                <div class="exp-highlights">
                    <div class="highlight">300+ Members</div>
                    <div class="highlight">8 Workshops</div>
                    <div class="highlight">40+ Projects</div>
                    <div class="highlight">85% Participation</div>
                </div>
            </div>

            <div class="experience-card">
                <div class="exp-title">Google Cloud Arcade Facilitator</div>
                <div class="exp-company">Google Cloud Skills Boost • Jul - Oct 2025</div>
                <div class="exp-description">
                    Mentored 4,000+ learners through 50+ hands-on GCP labs with 92% completion rate.
                </div>
                <div class="exp-highlights">
                    <div class="highlight">4,000+ Learners</div>
                    <div class="highlight">50+ Labs</div>
                    <div class="highlight">200+ Live Sessions</div>
                    <div class="highlight">92% Completion Rate</div>
                </div>
            </div>

            <div class="experience-card">
                <div class="exp-title">GirlScript Summer of Code 2026</div>
                <div class="exp-company">Project Admin & Mentor • May 2026 - Present</div>
                <div class="exp-description">
                    Multi-role contributor managing repositories, mentoring, and community building.
                </div>
                <div class="exp-highlights">
                    <div class="highlight">3 Repositories</div>
                    <div class="highlight">48-hr Code Reviews</div>
                    <div class="highlight">20+ Mentees</div>
                    <div class="highlight">100+ Participants</div>
                </div>
            </div>
        </section>

        <div class="divider"></div>

        <!-- TECHNICAL SKILLS -->
        <section>
            <h2>🛠️ Technical Expertise</h2>
            
            <h3 style="margin-top: 30px; margin-bottom: 15px; color: var(--primary);">AI & Machine Learning</h3>
            <div class="tech-grid">
                <div class="tech-item">RAG Pipelines</div>
                <div class="tech-item">Vertex AI</div>
                <div class="tech-item">Gemini API</div>
                <div class="tech-item">TensorFlow</div>
                <div class="tech-item">Python</div>
                <div class="tech-item">LangChain</div>
            </div>

            <h3 style="margin-top: 30px; margin-bottom: 15px; color: var(--primary);">Cloud & DevOps</h3>
            <div class="tech-grid">
                <div class="tech-item">Google Cloud</div>
                <div class="tech-item">Kubernetes</div>
                <div class="tech-item">Docker</div>
                <div class="tech-item">Terraform</div>
                <div class="tech-item">BigQuery</div>
                <div class="tech-item">Cloud Run</div>
            </div>

            <h3 style="margin-top: 30px; margin-bottom: 15px; color: var(--primary);">Web & Backend</h3>
            <div class="tech-grid">
                <div class="tech-item">JavaScript</div>
                <div class="tech-item">React</div>
                <div class="tech-item">Node.js</div>
                <div class="tech-item">MongoDB</div>
                <div class="tech-item">PostgreSQL</div>
                <div class="tech-item">Git</div>
            </div>
        </section>

        <div class="divider"></div>

        <!-- ACHIEVEMENTS -->
        <section>
            <h2>🏆 Certifications & Recognition</h2>
            
            <div class="stats">
                <div class="stat-box">
                    <div class="stat-number">100+</div>
                    <div class="stat-text">Google Cloud Badges</div>
                </div>
                <div class="stat-box">
                    <div class="stat-number">155K</div>
                    <div class="stat-text">GCP Points</div>
                </div>
                <div class="stat-box">
                    <div class="stat-number">7</div>
                    <div class="stat-text">Ambassador Programs</div>
                </div>
                <div class="stat-box">
                    <div class="stat-number">2</div>
                    <div class="stat-text">Founder Status</div>
                </div>
            </div>

            <h3 style="margin-top: 30px; color: var(--primary);">Key Badges & Certifications:</h3>
            <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 10px; margin-top: 20px;">
                <div class="highlight">Arcade Facilitator Certificate</div>
                <div class="highlight">Arcade Legend Tier</div>
                <div class="highlight">Vertex AI Skill Badge</div>
                <div class="highlight">Multimodal RAG Certificate</div>
                <div class="highlight">Kubernetes Management</div>
                <div class="highlight">Cloud Security</div>
                <div class="highlight">Neo4j Certified Professional</div>
                <div class="highlight">Google Cloud Ambassador</div>
            </div>
        </section>

        <div class="divider"></div>

        <!-- WHAT MAKES YOU DIFFERENT -->
        <section>
            <h2>✨ What Makes Me Different</h2>
            
            <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 20px;">
                <div class="experience-card">
                    <h3 style="color: var(--primary); margin-bottom: 10px;">Execution Speed</h3>
                    <p>200+ MVPs shipped in 90 days. Zero marketing budget. Focus on shipping, not talking.</p>
                </div>
                <div class="experience-card">
                    <h3 style="color: var(--primary); margin-bottom: 10px;">Teaching Ability</h3>
                    <p>4,000+ learners mentored with 92% completion rate. Clear explanations at scale.</p>
                </div>
                <div class="experience-card">
                    <h3 style="color: var(--primary); margin-bottom: 10px;">Community Builder</h3>
                    <p>Founded GSF 0→5,000 in 5 months. NexaSphere 300+ students. Sustainable growth.</p>
                </div>
                <div class="experience-card">
                    <h3 style="color: var(--primary); margin-bottom: 10px;">Enterprise Focus</h3>
                    <p>RAG on Vertex AI. Production-grade systems. Scalable architecture expertise.</p>
                </div>
                <div class="experience-card">
                    <h3 style="color: var(--primary); margin-bottom: 10px;">Multi-Stack</h3>
                    <p>AI/ML • Cloud • Web • Backend • DevOps. Full-stack problem solver.</p>
                </div>
                <div class="experience-card">
                    <h3 style="color: var(--primary); margin-bottom: 10px;">Growth Mindset</h3>
                    <p>Always learning. Jumped from participant to facilitator at Google. Certified everywhere.</p>
                </div>
            </div>
        </section>

        <div class="divider"></div>

        <!-- CONNECT -->
        <section style="padding: 60px 0;">
            <h2>🔗 Let's Connect</h2>
            
            <div style="text-align: center; margin-top: 40px;">
                <p style="font-size: 1.1rem; color: var(--text-muted); margin-bottom: 30px;">
                    I respond to every message within 24 hours.<br/>
                    Let's build something great together.
                </p>
                
                <div class="cta-group">
                    <a href="mailto:ayush.sharmaa@hotmail.com" class="btn btn-primary">💬 Email</a>
                    <a href="https://linkedin.com/in/ayushh-sharmaa" class="btn btn-secondary">LinkedIn</a>
                    <a href="https://x.com/xAyush07" class="btn btn-secondary">Twitter/X</a>
                    <a href="https://github.com/Ayushh-Sharmaa" class="btn btn-secondary">GitHub</a>
                </div>

                <div class="social-links" style="margin-top: 40px;">
                    <a href="mailto:ayush.sharmaa@hotmail.com" class="social-link" title="Email">📧</a>
                    <a href="https://linkedin.com/in/ayushh-sharmaa" class="social-link" title="LinkedIn">💼</a>
                    <a href="https://x.com/xAyush07" class="social-link" title="Twitter">𝕏</a>
                    <a href="https://github.com/Ayushh-Sharmaa" class="social-link" title="GitHub">⚙️</a>
                    <a href="https://www.skills.google/public_profiles/1b1ac0dc-2352-4584-ac57-e7b9a60cbc9c" class="social-link" title="GCP">☁️</a>
                </div>
            </div>
        </section>
    </div>

    <!-- FOOTER -->
    <footer>
        <div class="container">
            <p style="color: var(--text-muted); margin-bottom: 20px;">
                <strong>Status:</strong> Open to Internship Offers (Jun • Jul • Aug 2026)
            </p>
            <p style="color: var(--text-muted); font-size: 0.9rem;">
                Execution > Education • Shipping > Talking
            </p>
            <p style="color: var(--text-muted); font-size: 0.85rem; margin-top: 20px;">
                © 2026 Ayush Sharma • Last Updated: June 2026
            </p>
        </div>
    </footer>

    <script>
        // Smooth scroll animations on scroll
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -100px 0px'
        };

        const observer = new IntersectionObserver(function(entries) {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('fade-in');
                    observer.unobserve(entry.target);
                }
            });
        }, observerOptions);

        document.querySelectorAll('section').forEach(el => {
            observer.observe(el);
        });
    </script>
</body>
</html>
