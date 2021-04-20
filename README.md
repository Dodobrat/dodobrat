# I'm Dodo, Dodobrat <img src="https://media.giphy.com/media/TdvgwNdoIY9Ncl2D4d/giphy.gif" height="50">

Giving Google a run for their money since 2017

<img src="https://media.giphy.com/media/eoxomXXVL2S0E/source.gif" height="250">

```tsx

import React from "react";

import {SkillProps} from "./Deyan.types"

const Deyan: React.FC<SkillProps> = (props) => {
	const { 
    		skills = [
      			'react',
      			'typescript',
		      	'sass',
		      	'nodejs',
			'express',
		      	'mysql',
	    	],  
	    	work = {
	      		company: 'Veniway',
	      		position: 'Front-end Developer'
	    	},
		location = 'Sofia, Bulgaria',
	    	children, 
	    	...rest
  	} = props;
  
	return (
		<div {...rest}>
			<span>Location: {location}</span>
			
			<hr/>
			
      			<h1>Company: {work?.company}</h1>
      			<h4>Position: {work?.position}</h4>
			
			<div className='skills'>
      				{skills.map(skill: string => <span>{skill}</span>}
			</div>
			
			{children}
		</div>
	);
};

export default Deyan;

```
