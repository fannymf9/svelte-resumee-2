<script>
  import Header from './components/Header.svelte';
  import Education from './components/Education.svelte';
  import Experience from './components/Experience.svelte';
  import LanguagesAndSkills from './components/LanguagesAndSkills.svelte';

  const name = "Fanny Ferreira";
  const email = "fanny.ferreira@essec.edu";
  const phone = "06 52 20 90 83";
  const photoUrl = "/Users/fannyferreira/Desktop/WEBSITE CREATION/CV.jpg"; 

  const education = [
    { school: "ESSEC Business School", years: "Since 2021", program: "Grande Ecole Program, Master in Management, Cergy" },
    { school: "George Clémenceau High School", years: "2019 – 2021", program: "Preparatory Class in Economics and Business – Economics Track, Reims" },
    { school: "Jean-Jaurès High School", years: "2019", program: "High School Diploma in Economics and Social Sciences, Reims" }
  ];

  const jobs = [
    {
      title: "Apprenticeship, CFO's Right-Hand Man",
      company: "Le Fooding",
      years: "2023-2025",
      tasks: [
        "Cash-flow monitoring",
        "Cut off",
        "Client Billing: Issuing invoices, bank collections, and following up on unpaid invoices",
        "Supplier Invoicing: Organizing and paying invoices",
        "Payroll Processing",
        "Monitoring employee leave and absences",
        "Office management"
      ]
    },
    {
      title: "Intern in International Management Control",
      company: "GREENYELLOW",
      years: "2022",
      tasks: [
        "Cash management, analysis of cash reports",
        "Preparation of FTE reporting",
        "Closing of a Business Unit",
        "Counterparty analysis"
      ]
    },
    {
      title: "Junior Consultant",
      company: "ANDIBO",
      years: "2022",
      tasks: [
        "Customer feedback analysis",
        "Conducting market studies"
      ]
    }
  ];

  const languages = ["French (Native)", "English (Professional)", "Spanish (Fluent - Cervantes Diploma)"];
  const skills = ["Advanced Excel", "iOS", "Power BI", "Oracle (SQL)", "VBA", "Python"];
</script>

<main class="max-w-4xl mx-auto mt-10">
  <Header {name} {email} {phone} {photoUrl} />
  <Education {education} />
  <Experience {jobs} />
  <LanguagesAndSkills {languages} {skills} />
</main>


