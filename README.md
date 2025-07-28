# M-7003-QA
PennDOT M-7003 Environmental QA Form
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>M-7003 Environmental QA Form</title>
  <link rel="stylesheet" href="style.css" />
  <script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
</head>
<body>
  <div class="container">
    <h1>PennDOT M-7003 Form</h1>
    <p>Environmental QA Inspection</p>

    <form id="m7003Form">
      <!-- Section 1 -->
      <div class="section">
        <h2>1. Site Layout & Access (10 pts)</h2>
        <label>Driveways stabilized? <select name="q1"><option>0</option><option>1</option><option>2</option><option>3</option></select></label>
        <label>Access control in place? <select name="q2"><option>0</option><option>1</option><option>2</option><option>3</option></select></label>
        <label>Material storage protected? <select name="q3"><option>0</option><option>1</option><option>2</option><option>3</option><option>4</option></select></label>
      </div>

      <!-- Section 2 -->
      <div class="section">
        <h2>2. Erosion Control (25 pts)</h2>
        <label>Seeding applied? <select name="q4"><option>0</option><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select></label>
        <label>Mulching installed? <select name="q5"><option>0</option><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select></label>
        <label>Erosion control mats used? <select name="q6"><option>0</option><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select></label>
        <label>Slope protection? <select name="q7"><option>0</option><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option><option>6</option><option>7</option><option>8</option><option>9</option><option>10</option></select></label>
      </div>

      <!-- Section 3 -->
      <div class="section">
        <h2>3. Sediment Control (30 pts)</h2>
        <label>Silt fence installed? <select name="q8"><option>0</option><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select></label>
        <label>Sediment basin functional? <select name="q9"><option>0</option><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select></label>
        <label>Storm inlet protection? <select name="q10"><option>0</option><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select></label>
        <label>Sweeping/storm drain protection? <select name="q11"><option>0</option><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select></label>
        <label>Sediment trap cleaned? <select name="q12"><option>0</option><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select></label>
        <label>Diversion berms maintained? <select name="q13"><option>0</option><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select></label>
      </div>

      <!-- Section 4 -->
      <div class="section">
        <h2>4. Pollution Prevention (20 pts)</h2>
        <label>Fueling areas controlled? <select name="q14"><option>0</option><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select></label>
        <label>Waste containers covered? <select name="q15"><option>0</option><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select></label>
        <label>Chemicals stored properly? <select name="q16"><option>0</option><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select></label>
        <label>Spill kit available? <select name="q17"><option>0</option><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select></label>
      </div>

      <!-- Section 5 -->
      <div class="section">
        <h2>5. Site Maintenance (15 pts)</h2>
        <label>Site clean and debris-free? <select name="q18"><option>0</option><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select></label>
        <label>Erosion/sediment repairs made? <select name="q19"><option>0</option><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select></label>
        <label>Inspection log maintained? <select name="q20"><option>0</option><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select></label>
      </div>

      <button type="button" onclick="calculateScore()">Calculate Score</button>
      <button type="button" onclick="exportPDF()">Export as PDF</button>
    </form>

    <div id="result" class="result" style="display:none;">
      <h2>Results</h2>
      <p><strong>Total Score:</strong> <span id="totalScore">0</span> / 100</p>
      <p><strong>Percentage:</strong> <span id="percentage">0</span>%</p>
      <p><strong>Status:</strong> <span id="status">Pending</span></p>
    </div>
  </div>

  <script src="script.js"></script>
</body>
</html>
