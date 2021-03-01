# Hi there, I'm Deyan 👋

```tsx

import React from "react";
import cn from "classnames";
import ProfileCard from '../Cards/ProfileCard';

import { SkillProps } from "./SkillProps.types";

const Deyan: React.FC<SkillProps> = (props) => {
	const { 
    classNames, 
    skills = [
      'react',
      'typescript',
      'sass',
      'nodejs',
      'mysql',
    ],  
    work = {
      company: 'Veniway',
      position: 'Front-end Developer'
    },
    children, 
    ...rest
  } = props;
  
	return (
		<ProfileCard {...rest}>
      <h1>Company: {work?.company}</h1>
      <h4>Position: {work?.position}</h4>
      <hr/>
      {skills.map(skill => (
        <Badge>{skill}</Badge>
      )}
			{children}
		</ProfileCard>
	);
};

export default Deyan;

```
