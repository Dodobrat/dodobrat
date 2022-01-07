# I'm Dodo, Dodobrat <img src="https://media.giphy.com/media/TdvgwNdoIY9Ncl2D4d/giphy.gif" height="50">

Giving Google a run for their money since 2017

<img src="https://media.giphy.com/media/eoxomXXVL2S0E/source.gif" height="250">

```js

function Deyan(props){
  const {
    details = {
      fullName: "Deyan Bozhilov",
      age: "24",
      education: "Coventry University"
    },
    skills = [
      "react", 
      "typescript", 
      "sass", 
      "nodejs", 
      "express", 
      "mysql" 
    ],
    work = {
      company: "Dreamix",
      position: "React Developer"
    },
    location = {
      city: "Sofia",
      country: "Bulgaria"
    }
  } = props;
  
  const {t} = useTranslation();

  return (
    <article className="flex bg-white dark:bg-black text-black dark:text-white rounded p-4 md:p-2 shadow-sm">
      <Avatar />
      <div className="grid gap-2">
        <h1 className="text-lg space-x-2">
          <span>{details.fullName}</span> 
          <span className="text-sm text-gray">{details.age}</span>
        </h1>
        <h4 className="text-md">{details.education}</h4>
	
        <div className="px-4 py-2 border">
          <p>{t('common.work')}: {work.company} as {work.position}</p> 
          <p>{t('common.location')}: {location.city}, {location.country}</p>
	</div>
	
        <ul className="flex flex-wrap items-center gap-2">
          {skills.map((skill) => (
            <li key={skill} className="p-2 rounded bg-indigo-500 text-white cursor-pointer select-none">
              {skill}
            </li>
          ))}
        </ul>
      </div>
    </article>
  );
};

export default Deyan;

```
