<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Geotechnical Engineering: End-of-Course Feedback Survey</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
            min-height: 100vh;
            padding: 20px;
        }
        
        .container {
            max-width: 900px;
            margin: 0 auto;
            background: white;
            border-radius: 12px;
            box-shadow: 0 10px 40px rgba(0,0,0,0.2);
            padding: 40px;
        }
        
        h1 {
            color: #1e3c72;
            margin-bottom: 10px;
            font-size: 28px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .subtitle {
            color: #666;
            margin-bottom: 30px;
            font-size: 16px;
            line-height: 1.6;
        }
        
        .section {
            margin: 40px 0;
            padding: 30px;
            background: #f8f9fa;
            border-radius: 8px;
            border-left: 4px solid #2a5298;
        }
        
        .section-title {
            font-size: 22px;
            color: #1e3c72;
            font-weight: 600;
            margin-bottom: 25px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .question-block {
            margin-bottom: 30px;
            padding: 20px;
            background: white;
            border-radius: 6px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.05);
        }
        
        .question {
            font-weight: 600;
            color: #333;
            margin-bottom: 15px;
            font-size: 15px;
            line-height: 1.5;
        }
        
        .required {
            color: #e74c3c;
            margin-left: 4px;
        }
        
        input[type="text"],
        textarea {
            width: 100%;
            padding: 12px;
            border: 2px solid #e0e0e0;
            border-radius: 6px;
            font-size: 14px;
            font-family: inherit;
            transition: border-color 0.3s;
        }
        
        input[type="text"]:focus,
        textarea:focus {
            outline: none;
            border-color: #2a5298;
        }
        
        textarea {
            resize: vertical;
            min-height: 80px;
        }
        
        .radio-group {
            display: flex;
            flex-direction: column;
            gap: 10px;
        }
        
        .radio-option {
            display: flex;
            align-items: center;
            padding: 10px;
            border-radius: 6px;
            transition: background-color 0.2s;
        }
        
        .radio-option:hover {
            background-color: #f8f9fa;
        }
        
        input[type="radio"] {
            margin-right: 10px;
            width: 18px;
            height: 18px;
            cursor: pointer;
        }
        
        label {
            cursor: pointer;
            font-size: 14px;
            color: #555;
        }
        
        .scale-table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 10px;
        }
        
        .scale-table th,
        .scale-table td {
            padding: 12px;
            text-align: center;
            border: 1px solid #dee2e6;
        }
        
        .scale-table th {
            background-color: #e9ecef;
            font-weight: 600;
            color: #495057;
            font-size: 14px;
        }
        
        .scale-table td:first-child {
            text-align: left;
            font-weight: 500;
            background-color: #f8f9fa;
        }
        
        .ranking-item {
            margin-bottom: 15px;
            padding: 15px;
            background: #f8f9fa;
            border-radius: 6px;
        }
        
        .ranking-item label {
            display: block;
            font-weight: 500;
            margin-bottom: 10px;
            color: #333;
        }
        
        .ranking-input {
            display: flex;
            gap: 15px;
            align-items: center;
            margin-bottom: 10px;
        }
        
        .ranking-input select {
            padding: 8px 12px;
            border: 2px solid #e0e0e0;
            border-radius: 6px;
            font-size: 14px;
            cursor: pointer;
            background: white;
        }
        
        .ranking-input select:focus {
            outline: none;
            border-color: #2a5298;
        }
        
        .feedback-table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 10px;
        }
        
        .feedback-table th,
        .feedback-table td {
            padding: 12px;
            border: 1px solid #dee2e6;
            text-align: left;
        }
        
        .feedback-table th {
            background-color: #e9ecef;
            font-weight: 600;
            color: #495057;
            font-size: 13px;
        }
        
        .feedback-table td:first-child {
            font-weight: 500;
            background-color: #f8f9fa;
            width: 25%;
        }
        
        .table-radio-group {
            display: flex;
            gap: 15px;
        }
        
        .submit-btn {
            background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
            color: white;
            padding: 14px 40px;
            border: none;
            border-radius: 6px;
            font-size: 16px;
            font-weight: 600;
            cursor: pointer;
            transition: transform 0.2s, box-shadow 0.2s;
            margin-top: 30px;
        }
        
        .submit-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 20px rgba(30, 60, 114, 0.4);
        }
        
        .submit-btn:active {
            transform: translateY(0);
        }
        
        .submit-btn:disabled {
            opacity: 0.6;
            cursor: not-allowed;
        }
        
        .success-message {
            display: none;
            background-color: #d4edda;
            color: #155724;
            padding: 20px;
            border-radius: 6px;
            margin-top: 20px;
            border: 1px solid #c3e6cb;
        }
        
        .note {
            font-size: 13px;
            color: #6c757d;
            font-style: italic;
            margin-top: 5px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>📝 Geotechnical Engineering: End-of-Course Feedback Survey</h1>
        <p class="subtitle">Your feedback is invaluable in helping improve this course. Please take a few minutes to complete this survey. Your responses will be sent directly to the instructor.</p>
        
        <!-- IMPORTANT: Replace YOUR_EMAIL_HERE with your actual email address -->
        <form id="surveyForm" action="https://formspree.io/f/mqargyob" method="POST">
            
            <!-- Section 1: Student Demographics -->
            <div class="section">
                <div class="section-title">🧑‍🎓 Student Demographics</div>
                
                <div class="question-block">
                    <div class="question">Please select your current student status: <span class="required">*</span></div>
                    <div class="radio-group">
                        <div class="radio-option">
                            <input type="radio" name="student_status" value="Undergraduate Student" required id="status1">
                            <label for="status1">Undergraduate Student</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="student_status" value="Master's Student (Graduate)" id="status2">
                            <label for="status2">Master's Student (Graduate)</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="student_status" value="Ph.D. Student (Graduate)" id="status3">
                            <label for="status3">Ph.D. Student (Graduate)</label>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- Section 2: Interest and Course Format -->
            <div class="section">
                <div class="section-title">💡 Interest and Course Format</div>
                
                <div class="question-block">
                    <div class="question">Interest Level in the Topic (e.g., Soil Mechanics/Geotechnical Engineering) <span class="required">*</span></div>
                    <p class="note">Please rate your interest using the scale (1 = Very Low Interest, 5 = Very High Interest)</p>
                    <table class="scale-table">
                        <thead>
                            <tr>
                                <th>Timeframe</th>
                                <th>1</th>
                                <th>2</th>
                                <th>3</th>
                                <th>4</th>
                                <th>5</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td>Before taking this class</td>
                                <td><input type="radio" name="interest_before" value="1" required></td>
                                <td><input type="radio" name="interest_before" value="2"></td>
                                <td><input type="radio" name="interest_before" value="3"></td>
                                <td><input type="radio" name="interest_before" value="4"></td>
                                <td><input type="radio" name="interest_before" value="5"></td>
                            </tr>
                            <tr>
                                <td>After completing this class</td>
                                <td><input type="radio" name="interest_after" value="1" required></td>
                                <td><input type="radio" name="interest_after" value="2"></td>
                                <td><input type="radio" name="interest_after" value="3"></td>
                                <td><input type="radio" name="interest_after" value="4"></td>
                                <td><input type="radio" name="interest_after" value="5"></td>
                            </tr>
                        </tbody>
                    </table>
                </div>
                
                <div class="question-block">
                    <div class="question">Change in Interest Level <span class="required">*</span></div>
                    <p class="note">How has your interest in the topic changed since taking this course?</p>
                    <div class="radio-group">
                        <div class="radio-option">
                            <input type="radio" name="interest_change" value="Interest has significantly increased" required id="change1">
                            <label for="change1">Interest has significantly increased.</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="interest_change" value="Interest has slightly increased" id="change2">
                            <label for="change2">Interest has slightly increased.</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="interest_change" value="Interest has remained the same" id="change3">
                            <label for="change3">Interest has remained the same.</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="interest_change" value="Interest has slightly decreased" id="change4">
                            <label for="change4">Interest has slightly decreased.</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="interest_change" value="Interest has significantly decreased" id="change5">
                            <label for="change5">Interest has significantly decreased.</label>
                        </div>
                    </div>
                </div>
                
                <div class="question-block">
                    <div class="question">Future Course Offering and Recommendation <span class="required">*</span></div>
                    <p style="margin-bottom: 15px; font-weight: 500;">If this course were offered fully online in the future, would you be interested in taking it?</p>
                    <div class="radio-group">
                        <div class="radio-option">
                            <input type="radio" name="online_interest" value="Yes" required id="online1">
                            <label for="online1">Yes</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="online_interest" value="No" id="online2">
                            <label for="online2">No</label>
                        </div>
                    </div>
                    
                    <p style="margin: 20px 0 15px 0; font-weight: 500;">Would you be willing to recommend taking this course online to other classmates?</p>
                    <div class="radio-group">
                        <div class="radio-option">
                            <input type="radio" name="recommend_online" value="Yes" required id="recommend1">
                            <label for="recommend1">Yes</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="recommend_online" value="No" id="recommend2">
                            <label for="recommend2">No</label>
                        </div>
                    </div>
                </div>
                
                <div class="question-block">
                    <div class="question">Hybrid Format Preference <span class="required">*</span></div>
                    <p class="note">How do you like the format of one lecture face-to-face and one lecture online?</p>
                    <div class="radio-group">
                        <div class="radio-option">
                            <input type="radio" name="hybrid_preference" value="We should definitely keep this hybrid format in the future" required id="hybrid1">
                            <label for="hybrid1">We should definitely keep this hybrid format in the future.</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="hybrid_preference" value="It is a good format, but could be improved" id="hybrid2">
                            <label for="hybrid2">It is a good format, but could be improved.</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="hybrid_preference" value="I would prefer totally face-to-face lectures" id="hybrid3">
                            <label for="hybrid3">I would prefer totally face-to-face lectures.</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="hybrid_preference" value="I would prefer totally online lectures" id="hybrid4">
                            <label for="hybrid4">I would prefer totally online lectures.</label>
                        </div>
                    </div>
                    
                    <div style="margin-top: 20px;">
                        <label style="font-weight: 500; display: block; margin-bottom: 10px;">Please provide suggestions for improving the hybrid format:</label>
                        <textarea name="hybrid_suggestions" placeholder="Your suggestions..."></textarea>
                    </div>
                </div>
            </div>
            
            <!-- Section 3: Course Content and Topics -->
            <div class="section">
                <div class="section-title">📚 Course Content and Topics</div>
                
                <div class="question-block">
                    <div class="question">Please rank the following topics from 1 (Most Interesting/Helpful) to 5 (Least Interesting/Helpful) <span class="required">*</span></div>
                    
                    <div class="ranking-item">
                        <label>Shear strength of the soil</label>
                        <div class="ranking-input">
                            <span>Rank:</span>
                            <select name="rank_shear_strength" required>
                                <option value="">Select...</option>
                                <option value="1">1 - Most Interesting/Helpful</option>
                                <option value="2">2</option>
                                <option value="3">3</option>
                                <option value="4">4</option>
                                <option value="5">5 - Least Interesting/Helpful</option>
                            </select>
                        </div>
                        <label style="font-size: 13px; margin-top: 10px;">Suggestions for Improvement:</label>
                        <textarea name="suggestions_shear_strength" style="margin-top: 5px;" placeholder="Your suggestions..."></textarea>
                    </div>
                    
                    <div class="ranking-item">
                        <label>Influence of stress on M<sub>r</sub> values (Resilient Modulus)</label>
                        <div class="ranking-input">
                            <span>Rank:</span>
                            <select name="rank_resilient_modulus" required>
                                <option value="">Select...</option>
                                <option value="1">1 - Most Interesting/Helpful</option>
                                <option value="2">2</option>
                                <option value="3">3</option>
                                <option value="4">4</option>
                                <option value="5">5 - Least Interesting/Helpful</option>
                            </select>
                        </div>
                        <label style="font-size: 13px; margin-top: 10px;">Suggestions for Improvement:</label>
                        <textarea name="suggestions_resilient_modulus" style="margin-top: 5px;" placeholder="Your suggestions..."></textarea>
                    </div>
                    
                    <div class="ranking-item">
                        <label>Soil Dynamics</label>
                        <div class="ranking-input">
                            <span>Rank:</span>
                            <select name="rank_soil_dynamics" required>
                                <option value="">Select...</option>
                                <option value="1">1 - Most Interesting/Helpful</option>
                                <option value="2">2</option>
                                <option value="3">3</option>
                                <option value="4">4</option>
                                <option value="5">5 - Least Interesting/Helpful</option>
                            </select>
                        </div>
                        <label style="font-size: 13px; margin-top: 10px;">Suggestions for Improvement:</label>
                        <textarea name="suggestions_soil_dynamics" style="margin-top: 5px;" placeholder="Your suggestions..."></textarea>
                    </div>
                    
                    <div class="ranking-item">
                        <label>Soil liquefaction</label>
                        <div class="ranking-input">
                            <span>Rank:</span>
                            <select name="rank_soil_liquefaction" required>
                                <option value="">Select...</option>
                                <option value="1">1 - Most Interesting/Helpful</option>
                                <option value="2">2</option>
                                <option value="3">3</option>
                                <option value="4">4</option>
                                <option value="5">5 - Least Interesting/Helpful</option>
                            </select>
                        </div>
                        <label style="font-size: 13px; margin-top: 10px;">Suggestions for Improvement:</label>
                        <textarea name="suggestions_soil_liquefaction" style="margin-top: 5px;" placeholder="Your suggestions..."></textarea>
                    </div>
                    
                    <div class="ranking-item">
                        <label>Stress path</label>
                        <div class="ranking-input">
                            <span>Rank:</span>
                            <select name="rank_stress_path" required>
                                <option value="">Select...</option>
                                <option value="1">1 - Most Interesting/Helpful</option>
                                <option value="2">2</option>
                                <option value="3">3</option>
                                <option value="4">4</option>
                                <option value="5">5 - Least Interesting/Helpful</option>
                            </select>
                        </div>
                        <label style="font-size: 13px; margin-top: 10px;">Suggestions for Improvement:</label>
                        <textarea name="suggestions_stress_path" style="margin-top: 5px;" placeholder="Your suggestions..."></textarea>
                    </div>
                </div>
            </div>
            
            <!-- Section 4: Lecture Video Feedback -->
            <div class="section">
                <div class="section-title">🎥 Lecture Video Feedback</div>
                <p class="note" style="margin-bottom: 20px;">This section focuses on the pre-recorded lecture videos assigned for the course.</p>
                
                <div class="question-block">
                    <div class="question">Video Length <span class="required">*</span></div>
                    <p class="note">For the lecture videos covering individual topics, how would you rate their overall length?</p>
                    <div class="radio-group">
                        <div class="radio-option">
                            <input type="radio" name="video_length" value="Too Short - I needed more detail/examples" required id="length1">
                            <label for="length1">Too Short - I needed more detail/examples.</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="video_length" value="Just Right - The length was perfect for the content" id="length2">
                            <label for="length2">Just Right - The length was perfect for the content.</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="video_length" value="Too Long - They could be condensed without losing important information" id="length3">
                            <label for="length3">Too Long - They could be condensed without losing important information.</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="video_length" value="Varied by Video - Some were too long, others were too short" id="length4">
                            <label for="length4">Varied by Video - Some were too long, others were too short.</label>
                        </div>
                    </div>
                </div>
                
                <div class="question-block">
                    <div class="question">Embedded Questions/Checks <span class="required">*</span></div>
                    <p class="note">The questions included within the lecture videos (e.g., pop quizzes, comprehension checks) were:</p>
                    <div class="radio-group">
                        <div class="radio-option">
                            <input type="radio" name="embedded_questions" value="Very helpful for testing my understanding" required id="embedded1">
                            <label for="embedded1">Very helpful for testing my understanding.</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="embedded_questions" value="Somewhat helpful, but could be improved" id="embedded2">
                            <label for="embedded2">Somewhat helpful, but could be improved.</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="embedded_questions" value="Not helpful, or I did not utilize them" id="embedded3">
                            <label for="embedded3">Not helpful, or I did not utilize them.</label>
                        </div>
                    </div>
                </div>
                
                <div class="question-block">
                    <div class="question">Relevance to Assignments <span class="required">*</span></div>
                    <p class="note">How helpful were the lecture videos in preparing you for the course assignments and problem-solving (e.g., homework, quizzes, projects)?</p>
                    <div class="radio-group">
                        <div class="radio-option">
                            <input type="radio" name="video_relevance" value="Extremely helpful - They directly covered the necessary concepts and problem types" required id="relevance1">
                            <label for="relevance1">Extremely helpful - They directly covered the necessary concepts and problem types.</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="video_relevance" value="Moderately helpful - They covered the concepts, but I needed additional resources for problem-solving" id="relevance2">
                            <label for="relevance2">Moderately helpful - They covered the concepts, but I needed additional resources for problem-solving.</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="video_relevance" value="Slightly helpful - There was little to no clear connection to the assignments" id="relevance3">
                            <label for="relevance3">Slightly helpful - There was little to no clear connection to the assignments.</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="video_relevance" value="Not applicable - I did not use the lecture videos for problem-solving" id="relevance4">
                            <label for="relevance4">Not applicable - I did not use the lecture videos for problem-solving.</label>
                        </div>
                    </div>
                </div>
                
                <div class="question-block">
                    <div class="question">Suggested Improvements for Videos</div>
                    <p class="note">What specific improvements would you suggest for the lecture videos (e.g., production quality, pace, examples, use of graphics, structure)?</p>
                    <textarea name="video_improvements" placeholder="Your suggestions..."></textarea>
                </div>
            </div>
            
            <!-- Section 5: Assessments and Assignments -->
            <div class="section">
                <div class="section-title">📝 Assessments and Assignments</div>
                <p class="note" style="margin-bottom: 20px;">Please provide feedback on the Quizzes, Homework, Reading Assignments (Papers), and Projects.</p>
                
                <div class="question-block">
                    <table class="feedback-table">
                        <thead>
                            <tr>
                                <th>Component</th>
                                <th>Do you prefer this format?</th>
                                <th>If NO, what is your preferred format?</th>
                                <th>Key Improvement Suggestions</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td>Quizzes</td>
                                <td>
                                    <div class="table-radio-group">
                                        <label><input type="radio" name="quizzes_format" value="Yes" required> Yes</label>
                                        <label><input type="radio" name="quizzes_format" value="No"> No</label>
                                    </div>
                                </td>
                                <td><textarea name="quizzes_preferred" placeholder="Your preferred format..."></textarea></td>
                                <td><textarea name="quizzes_improvements" placeholder="Suggestions (e.g., timing, submission, evaluation, content)..."></textarea></td>
                            </tr>
                            <tr>
                                <td>Homework Style</td>
                                <td>
                                    <div class="table-radio-group">
                                        <label><input type="radio" name="homework_format" value="Yes" required> Yes</label>
                                        <label><input type="radio" name="homework_format" value="No"> No</label>
                                    </div>
                                </td>
                                <td><textarea name="homework_preferred" placeholder="Your preferred format..."></textarea></td>
                                <td><textarea name="homework_improvements" placeholder="Suggestions (e.g., submission time, complexity)..."></textarea></td>
                            </tr>
                            <tr>
                                <td>Paper Reading Assignments</td>
                                <td>
                                    <div class="table-radio-group">
                                        <label><input type="radio" name="papers_format" value="Yes" required> Yes</label>
                                        <label><input type="radio" name="papers_format" value="No"> No</label>
                                    </div>
                                </td>
                                <td><textarea name="papers_preferred" placeholder="Your preferred format..."></textarea></td>
                                <td><textarea name="papers_improvements" placeholder="Suggestions..."></textarea></td>
                            </tr>
                            <tr>
                                <td>Projects</td>
                                <td>
                                    <div class="table-radio-group">
                                        <label><input type="radio" name="projects_format" value="Yes" required> Yes</label>
                                        <label><input type="radio" name="projects_format" value="No"> No</label>
                                    </div>
                                </td>
                                <td><textarea name="projects_preferred" placeholder="Your preferred format..."></textarea></td>
                                <td><textarea name="projects_improvements" placeholder="Suggestions (e.g., format, list, evaluation)..."></textarea></td>
                            </tr>
                        </tbody>
                    </table>
                </div>
            </div>
            
            <button type="submit" class="submit-btn">Submit Survey</button>
            
            <div class="success-message" id="successMessage">
                <strong>Thank you for your feedback!</strong> Your responses have been submitted successfully.
            </div>
        </form>
    </div>
    
    <script>
        // Form submission handling
        const form = document.getElementById('surveyForm');
        const submitBtn = form.querySelector('.submit-btn');
        const successMessage = document.getElementById('successMessage');
        
        form.addEventListener('submit', function(e) {
            // Disable submit button to prevent double submission
            submitBtn.disabled = true;
            submitBtn.textContent = 'Submitting...';
        });
    </script>
</body>
</html>
