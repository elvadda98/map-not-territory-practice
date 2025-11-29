<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>The Map Is Not The Territory – Practice</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      max-width: 900px;
      margin: 20px auto;
      line-height: 1.5;
      padding: 0 10px;
    }
    h1, h2, h3 {
      margin-top: 1.4em;
    }
    .card {
      border: 1px solid #ccc;
      border-radius: 8px;
      padding: 12px 14px;
      margin: 10px 0;
    }
    .question {
      margin-bottom: 8px;
      font-weight: bold;
    }
    button {
      margin-top: 8px;
      padding: 6px 10px;
      border-radius: 6px;
      border: 1px solid #888;
      cursor: pointer;
    }
    button:hover {
      opacity: 0.9;
    }
    .feedback {
      margin-top: 6px;
      font-style: italic;
    }
    textarea {
      width: 100%;
      min-height: 80px;
      margin-top: 8px;
    }
    .correct {
      color: green;
      font-weight: bold;
    }
    .incorrect {
      color: darkred;
      font-weight: bold;
    }
    .tag {
      display: inline-block;
      padding: 2px 6px;
      border-radius: 4px;
      border: 1px solid #ccc;
      font-size: 0.8em;
      margin-left: 4px;
    }
  </style>
</head>
<body>
  <h1>The Map Is Not The Territory – Interactive Practice</h1>
  <p>
    This page helps you practice the first mental model in
    <em>The Great Mental Models: Volume 1</em> – <strong>The Map is Not the Territory</strong>.
    Use it during the week to test yourself and spot where you are confusing
    your maps (models, stories, labels) with the real territory.
  </p>

  <!-- SECTION 1: QUICK DEFINITION CHECK -->
  <h2>1. Quick Definition Check</h2>
  <div class="card">
    <div class="question">
      Which statement best captures “The map is not the territory”?
    </div>
    <label>
      <input type="radio" name="def" value="A">
      A) Good theories are always perfectly accurate.
    </label><br>
    <label>
      <input type="radio" name="def" value="B">
      B) Any description of reality is a simplified representation, not reality itself.
    </label><br>
    <label>
      <input type="radio" name="def" value="C">
      C) If you collect enough data, you will know reality exactly.
    </label><br>
    <label>
      <input type="radio" name="def" value="D">
      D) Only scientific models count as “maps”.
    </label><br>
    <button onclick="checkDefinition()">Check answer</button>
    <div id="defFeedback" class="feedback"></div>
  </div>

  <!-- SECTION 2: SCENARIO QUIZ -->
  <h2>2. Are They Confusing Map and Territory?</h2>
  <p>
    For each situation, choose the best answer:
    <strong>Are they confusing map and territory?</strong>
  </p>

  <div class="card">
    <div class="question">
      2.1 Hiring by CV Only
    </div>
    <p>
      A manager rejects a candidate just because their CV doesn’t come
      from a top university, without ever talking to them or giving them
      a test task.
    </p>
    <label>
      <input type="radio" name="q1" value="yes"> Yes, they’re confusing map and territory
    </label><br>
    <label>
      <input type="radio" name="q1" value="no"> No, they’re not
    </label>
  </div>

  <div class="card">
    <div class="question">
      2.2 Testing a Business Idea
    </div>
    <p>
      An entrepreneur makes a beautiful slide deck with revenue projections,
      then goes out and talks to potential customers to see what they actually
      think of the product.
    </p>
    <label>
      <input type="radio" name="q2" value="yes"> Yes, they’re confusing map and territory
    </label><br>
    <label>
      <input type="radio" name="q2" value="no"> No, they’re not
    </label>
  </div>

  <div class="card">
    <div class="question">
      2.3 Stereotyping a Student
    </div>
    <p>
      A teacher decides that a student is “bad at languages” because the
      student failed one grammar test, and then gives up trying new approaches.
    </p>
    <label>
      <input type="radio" name="q3" value="yes"> Yes, they’re confusing map and territory
    </label><br>
    <label>
      <input type="radio" name="q3" value="no"> No, they’re not
    </label>
  </div>

  <div class="card">
    <div class="question">
      2.4 Investing by Ratios
    </div>
    <p>
      An investor uses valuation ratios (P/E, P/B, etc.) as a starting point,
      but then reads reports, listens to earnings calls, and studies the
      business model before investing.
    </p>
    <label>
      <input type="radio" name="q4" value="yes"> Yes, they’re confusing map and territory
    </label><br>
    <label>
      <input type="radio" name="q4" value="no"> No, they’re not
    </label>
  </div>

  <div class="card">
    <div class="question">
      2.5 Clinging to a First Impression
    </div>
    <p>
      After a slightly awkward first meeting, someone decides “this person
      is arrogant” and refuses to update their view even after several
      positive interactions.
    </p>
    <label>
      <input type="radio" name="q5" value="yes"> Yes, they’re confusing map and territory
    </label><br>
    <label>
      <input type="radio" name="q5" value="no"> No, they’re not
    </label>
  </div>

  <button onclick="checkScenarios()">Check all scenario answers</button>
  <div id="scenarioFeedback" class="feedback"></div>

  <!-- SECTION 3: Spot the Map -->
  <h2>3. Spot the Map – Quick Drill</h2>
  <p>
    Read each statement. Decide: <strong>What is the map?</strong> and
    <strong>what is the territory?</strong> Click “Show suggestion” to see one possible answer.
  </p>

  <div class="card">
    <div class="question">
      3.1 Language Level Test
    </div>
    <p>
      “This student scored B2 on a standardized test, so I know exactly
      how they will perform in every real-life conversation.”
    </p>
    <button onclick="toggleHint('hint1')">Show suggestion</button>
    <div id="hint1" class="feedback" style="display:none;">
      <span class="tag">Map</span> the B2 test score.<br>
      <span class="tag">Territory</span> the student’s actual performance in real conversations across
      different contexts, moods, topics, and partners.
    </div>
  </div>

  <div class="card">
    <div class="question">
      3.2 Business Plan
    </div>
    <p>
      “Our Excel model says we’ll grow 50% per year, so that’s what will happen.”
    </p>
    <button onclick="toggleHint('hint2')">Show suggestion</button>
    <div id="hint2" class="feedback" style="display:none;">
      <span class="tag">Map</span> the Excel model and revenue projections.<br>
      <span class="tag">Territory</span> what customers actually do, competitive responses,
      economic conditions, and all the events that really unfold.
    </div>
  </div>

  <div class="card">
    <div class="question">
      3.3 Personality Label
    </div>
    <p>
      “He’s an introvert, so he’ll never be good at sales.”
    </p>
    <button onclick="toggleHint('hint3')">Show suggestion</button>
    <div id="hint3" class="feedback" style="display:none;">
      <span class="tag">Map</span> the label “introvert” and the stereotype attached to it.<br>
      <span class="tag">Territory</span> the person’s actual behaviour in different sales situations,
      their skills, training, and how they grow over time.
    </div>
  </div>

  <!-- SECTION 4: Reflection & Real Life Application -->
  <h2>4. Reflection: Your Own Maps This Week</h2>
  <p>
    Use these prompts during the week. You can type directly here while
    the file is open in your browser (it won’t be saved automatically, so
    copy anything important elsewhere).
  </p>

  <div class="card">
    <div class="question">
      4.1 Where did I mistake a map for the territory recently?
    </div>
    <p>
      Think of a situation (teaching, business, relationships, investing, etc.)
      where you realized your model of reality was incomplete or wrong.
    </p>
    <textarea placeholder="Describe the situation & what you learned..."></textarea>
  </div>

  <div class="card">
    <div class="question">
      4.2 Which maps do I rely on most in my work?
    </div>
    <p>
      Examples: CVs, test scores, dashboards, financial ratios, labels about people.
      How could each of these maps be incomplete or misleading?
    </p>
    <textarea placeholder="List your key maps and their limitations..."></textarea>
  </div>

  <div class="card">
    <div class="question">
      4.3 How will I “touch the territory” more often?
    </div>
    <p>
      Concrete ideas: talk directly to customers/students, do small experiments,
      observe behaviour instead of just reading reports, etc.
    </p>
    <textarea placeholder="Write 2–3 experiments you can run this week..."></textarea>
  </div>

  <!-- SECTION 5: Mini Self-Test -->
  <h2>5. Mini Self-Test: One-Paragraph Summary</h2>
  <p>
    Try to write, in your own words, a short explanation you could give to a friend:
    “What does ‘the map is not the territory’ mean, and why does it matter?”
  </p>
  <div class="card">
    <textarea id="summaryText" placeholder="Write your explanation here..."></textarea>
    <button onclick="evaluateSummary()">Give me gentle feedback</button>
    <div id="summaryFeedback" class="feedback"></div>
  </div>

  <script>
    // SECTION 1: Definition check
    function checkDefinition() {
      const radios = document.getElementsByName("def");
      let choice = null;
      for (const r of radios) {
        if (r.checked) {
          choice = r.value;
          break;
        }
      }
      const fb = document.getElementById("defFeedback");
      if (!choice) {
        fb.textContent = "Choose an answer first 🙂";
        fb.className = "feedback";
        return;
      }
      if (choice === "B") {
        fb.innerHTML = "<span class='correct'>Correct!</span> The key idea is that any model or description is a simplified representation of reality, not reality itself.";
      } else {
        fb.innerHTML = "<span class='incorrect'>Not quite.</span> Remember: the model is a simplification. It can be useful without being perfectly accurate, and it never captures everything.";
      }
    }

    // SECTION 2: Scenario answers
    const scenarioAnswers = {
      q1: "yes", // hiring by CV only
      q2: "no",  // tests map vs territory
      q3: "yes", // stereotyping
      q4: "no",  // using ratios then checking reality
      q5: "yes"  // clinging to first impression
    };

    function checkScenarios() {
      let correctCount = 0;
      let total = 5;
      let missing = [];

      for (let i = 1; i <= total; i++) {
        const name = "q" + i;
        const radios = document.getElementsByName(name);
        let chosen = null;
        for (const r of radios) {
          if (r.checked) {
            chosen = r.value;
            break;
          }
        }
        if (!chosen) {
          missing.push(i);
        } else if (chosen === scenarioAnswers[name]) {
          correctCount++;
        }
      }

      const fb = document.getElementById("scenarioFeedback");
      if (missing.length > 0) {
        fb.innerHTML = "You still need to answer question(s): " + missing.join(", ") + ".";
        fb.className = "feedback";
        return;
      }

      fb.className = "feedback";
      fb.innerHTML =
        "You got " + correctCount + " out of " + total + " correct. " +
        (correctCount === total
          ? "<span class='correct'>Great job! You’re distinguishing map vs territory well.</span>"
          : "<span class='incorrect'>Nice effort.</span> Review the situations where you disagreed and ask yourself: which part is the map, and which part is the territory?");
    }

    // SECTION 3: Toggle hints
    function toggleHint(id) {
      const el = document.getElementById(id);
      if (!el) return;
      el.style.display = (el.style.display === "none" || el.style.display === "") ? "block" : "none";
    }

    // SECTION 5: Simple heuristic feedback on the written summary
    function evaluateSummary() {
      const text = document.getElementById("summaryText").value.trim();
      const fb = document.getElementById("summaryFeedback");

      if (!text) {
        fb.textContent = "Try writing at least one or two sentences in your own words 🙂";
        fb.className = "feedback";
        return;
      }

      let comments = [];
      if (text.length < 80) {
        comments.push("You could add a bit more detail: maybe an example from your life or why this model is useful.");
      }

      const hasMap = /map/i.test(text);
      const hasTerritory = /territory/i.test(text);
      const hasSimplify = /(simplif|represe|model|modello)/i.test(text);
      const hasWhyMatters = /(decision|errore|mistake|better|bias|sbagli|utile|useful)/i.test(text);

      if (hasMap && hasTerritory && hasSimplify && hasWhyMatters) {
        comments.unshift("Nice! Your explanation hits the essential elements of the model.");
      } else {
        comments.unshift("Good start. To strengthen it, make sure you mention that:");
        if (!hasMap || !hasTerritory) {
          comments.push("- There is a difference between the <strong>map</strong> (your model) and the <strong>territory</strong> (reality).");
        }
        if (!hasSimplify) {
          comments.push("- The map is always a <strong>simplified representation</strong> or model, not the full reality.");
        }
        if (!hasWhyMatters) {
          comments.push("- Why this matters for your <strong>decisions</strong> or for avoiding mistakes.");
        }
      }

      fb.innerHTML = comments.join("<br>");
      fb.className = "feedback";
    }
  </script>
</body>
</html>
