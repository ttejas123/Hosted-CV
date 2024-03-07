<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Khushboo_Resume</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="html2pdf.bundle.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/html2pdf.js/0.10.1/html2pdf.bundle.min.js" integrity="sha512-GsLlZN/3F2ErC5ifS5QtgpiJtWd43JWSuIgh7mbzZ8zBps+dvLusV+eNQATqgA/HdeKFVgA5v3S/cIrLF7QnIg==" crossorigin="anonymous" referrerpolicy="no-referrer"></script>
    <style>
        .title-xl-Text {
            font-size: 20px;
        }
        .title-md-Text {
            font-size: 17px;
        }
        .subText {
            font-size: 15px;
        }
        .divider {
            border: 1px solid #0f2f2f;
        }
        .extraSpace{
            /* padding-left: 10rem;
            padding-right: 10rem; */
            margin-top: 3rem;
            margin-bottom: 5rem;
            display: flex;
            justify-content: center;
            align-items: center;
        }
    </style>
      <script>
        function downloadHTML() {
          const resumeContent = document.querySelector('.downloadContentclass').outerHTML;
          const blob = new Blob([resumeContent], { type: 'text/html' });
          const url = URL.createObjectURL(blob);
          const a = document.createElement('a');
          a.href = url;
          a.download = 'resume.html';
          a.click();
        }
          
        function downloadPDF() {
          const element = document.querySelector('.downloadContentclass');
          const opt = {
            margin: 1,
            filename: 'resume.pdf',
            image: { type: 'jpeg', quality: 0.98 },
            html2canvas: { scale: 2 },
            jsPDF: { 
                        orientation: 'p',
                        unit: 'pt',
                        format: 'a3',
                        precision: 16,
                        putOnlyUsedFonts:true,
                        floatPrecision: 16  
                    }
          };
          html2pdf().set(opt).from(element).save();
          
        }
    
        function downloadWord() {
          // You can use a third-party library like html-docx-js or html-to-docx to convert HTML to Word file
          // Or you can utilize a server-side API or service to generate Word files from HTML
          alert('Word file download functionality is not implemented yet.');
        }
      </script>
</head>

<body class="bg-gray-100 relative">
    <div class="sticky top-[5%] mr-3 flex justify-end">
        <!-- <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded" onclick="downloadHTML()">Download HTML</button> -->
        <button class="bg-while-500 hover:bg-gray-200  font-bold py-2 px-4 rounded flex text-current border border-2 justify-center items-center " onclick="downloadPDF()">Download<img width="20" class="ml-2" height="20" src="https://img.icons8.com/material-sharp/24/download--v2.png" alt="download--v2"/></button>
        <!-- <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded" onclick="downloadWord()">Download Word</button> -->
    </div>
    <div class="extraSpace">
    <div class="bg-white px-[60px] py-[30px] w-[1100px] rounded-2xl shadow-2xl downloadContentclass">
        <!-- Header Section -->
        <section class=" py-2">
            <h2 class="flex justify-center font-bold title-xl-Text">Khushboo Yadav, Software Engineer</h2>
            <h3 class="flex justify-center subText pt-2">Ghatkoper, Mumbai, India, +91 9136827371, yadavkhushboo7653@gmail.com, @APML</h3>
        </section>
        <hr class="divider my-3" />
        <!-- Links Section -->
        <section class="flex justify-center items-center py-2">
            <div class="flex-[0.3] title-md-Text italic">
                LINKS
            </div>
            <div class="flex-[0.7] subText underline">
                Portfolio, Github, Linkedin, Coding Profile
            </div>
        </section>
        <hr class="divider my-3" />
        <!-- Profile Section -->
        <section class="flex justify-center items-center py-2">
            <div class="flex-[0.3] title-md-Text italic">
                PROFILE
            </div>
            <div class="flex-[0.7] subText">
              Aspiring to work with an organization where I can utilize my skills and capabilities to curve a niche for myself and effectively deliver toward the organization's objectives.
            </div>
        </section>
        <hr class="divider my-3" />
        <!-- Projects -->
        <section class="flex justify-center items-center py-2">
          <div class="flex-[0.3] title-md-Text italic">
              PROJECTS
          </div>
          <div class="flex-[0.7] subText">
              <div class="">
                  <div class="grid grid-cols-1 gap-4">
                    <div class="flex justify-between">
                      <p class="text-gray-700 font-semibold">Node.js</p>
                      <p class="text-gray-600">Skilled</p>
                    </div>
                    <div class="flex justify-between">
                      <p class="text-gray-700 font-semibold">JavaScript</p>
                      <p class="text-gray-600">Skillful</p>
                    </div>
                    <div class="flex justify-between">
                      <p class="text-gray-700 font-semibold">React.js</p>
                      <p class="text-gray-600">Skillful</p>
                    </div>
                    <div class="flex justify-between">
                      <p class="text-gray-700 font-semibold">MongoDB</p>
                      <p class="text-gray-600">Skillful</p>
                    </div>
                    <div class="flex justify-between">
                      <p class="text-gray-700 font-semibold">HTML &amp; CSS</p>
                      <p class="text-gray-600">Skillful</p>
                    </div>
                    <div class="flex justify-between">
                      <p class="text-gray-700 font-semibold">SQL (Programming Language)</p>
                      <p class="text-gray-600">Skillful</p>
                    </div>
                    
                  </div>
                </div>
          </div>
      </section>
        <hr class="divider my-3" />
        <!-- Employement Section -->
        <section class="flex-col justify-center items-center py-2">
            <div class="flex-[1.0] title-md-Text italic">
                EMPLOYEMENT HISTORY
            </div>
            <div class="subText flex justify-center items-center w-full">
                <span class="w-[30%] text-left ">Jan-2023 -- Present</span>
                <span class="w-[70%]">
                    <span class="flex justify-between items-center w-full">
                        <span class="title-xl-Text">Full stack developer, Agarwal Packers & Movers (+1 year)</span>
                        <span class="italic">Goregao, Mumbai</span>
                    </span>
                    <span>
                        Achievements/Tasks
                    </span>
                    <span>
                        <li>Building Website using Wix website builder, also i have improve the existing site with new design and added extra features.</li>
                        <li>for initial 2 month i worked on 2 different project which is APML ODC & METNMAT, i have extensively improved site performance and simplicity.</li>
                        <li>After that I have undertaken multiple projects which make use of geo special data which are our ingrown projects such as APML Screen, APML MXL/SXL/ODD/CAR, this projects have live tracking system and Security system.</li>
                        <li>Currently I am invested in Vision Project which is Neo Non Banking Exchange Platform, I have structured this project and setup this project in Next.js currently it's phase 2 is in development.</li>
                        <li>During this Period I have also used some cloud features such as EC2.</li>
                        <li>I have udertaken multiple projects of APML and my major role is in improving existing software to meet current goal.</li>
                    </span>
                </span>
            </div>

        </section>
        <hr class="divider my-3" />
        <!-- Skills Section -->
        <section class="flex justify-center items-center py-2">
            <div class="flex-[0.3] title-md-Text italic">
                SKILLS
            </div>
            <div class="flex-[0.7] subText">
                <div class="">
                    <div class="grid grid-cols-2 gap-4">
                      <div class="flex justify-between">
                        <p class="text-gray-700 font-semibold">Node.js</p>
                        <p class="text-gray-600">Skilled</p>
                      </div>
                      <div class="flex justify-between">
                        <p class="text-gray-700 font-semibold">JavaScript</p>
                        <p class="text-gray-600">Skillful</p>
                      </div>
                      <div class="flex justify-between">
                        <p class="text-gray-700 font-semibold">React.js</p>
                        <p class="text-gray-600">Skillful</p>
                      </div>
                      <div class="flex justify-between">
                        <p class="text-gray-700 font-semibold">MongoDB</p>
                        <p class="text-gray-600">Skillful</p>
                      </div>
                      <div class="flex justify-between">
                        <p class="text-gray-700 font-semibold">HTML &amp; CSS</p>
                        <p class="text-gray-600">Skillful</p>
                      </div>
                      <div class="flex justify-between">
                        <p class="text-gray-700 font-semibold">Hosting</p>
                        <p class="text-gray-600">Skilled</p>
                      </div>
                      <div class="flex justify-between">
                        <p class="text-gray-700 font-semibold">Tailwindcss</p>
                        <p class="text-gray-600">Skillful</p>
                      </div>
                      <div class="flex justify-between">
                        <p class="text-gray-700 font-semibold">Git</p>
                        <p class="text-gray-600">Skillful</p>
                      </div>
                      <div class="flex justify-between">
                        <p class="text-gray-700 font-semibold">Bootstrap (Front-End Framework)</p>
                        <p class="text-gray-600">Skillful</p>
                      </div>
                      <div class="flex justify-between">
                        <p class="text-gray-700 font-semibold">Postman</p>
                        <p class="text-gray-600">Skillful</p>
                      </div>
                      <div class="flex justify-between">
                        <p class="text-gray-700 font-semibold">SQL (Programming Language)</p>
                        <p class="text-gray-600">Skillful</p>
                      </div>
                      <div class="flex justify-between">
                        <p class="text-gray-700 font-semibold">WIX</p>
                        <p class="text-gray-600">Skillful</p>
                      </div>
                      <div class="flex justify-between">
                        <p class="text-gray-700 font-semibold">UI/UX</p>
                        <p class="text-gray-600">Skillful</p>
                      </div>
                    </div>
                  </div>
            </div>
        </section>
        <hr class="divider my-3" />
        <!-- Education Section -->
        <section class="flex-col justify-center items-center py-2">
            <div class="flex-[1.0] title-md-Text italic">
                EDUCATION
            </div>
            <div class="subText flex justify-center items-center w-full">
                <span class="w-[30%] text-left ">Jun-2021 -- May-2023</span>
                <span class="w-[70%]">
                    <span class="flex justify-between items-center w-full">
                        <span class="title-xl-Text">Masters of science in computer science, Mumbai university kalina</span>
                        <span class="italic">Mumbai</span>
                    </span>
                    <span>
                        CGPA: 8.90
                    </span>
                </span>
            </div>
            <div class="subText flex justify-center items-center w-full  pt-5">
                <span class="w-[30%] text-left ">jun-2018 -- may-2021</span>
                <span class="w-[70%]">
                    <span class="flex justify-between items-center w-full">
                        <span class="title-xl-Text">Bachelor of science in Computer Science, RJ college ghatkoper</span>
                        <span class="italic">Mumbai</span>
                    </span>
                    <span>
                        CGPA: 8.80
                    </span>
                </span>
            </div>
        </section>
    </div>
    </div>
   
</body>
</html>
