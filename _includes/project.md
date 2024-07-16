import React from 'react';
import { Card, CardHeader, CardContent, CardFooter } from '@/components/ui/card';
import { Badge } from '@/components/ui/badge';
import { Button } from '@/components/ui/button';
import { FileText, Code, ExternalLink } from 'lucide-react';

const projects = {
  bioinformatics: [
    {
      title: "A Multiomics Approach for Investigating Nitrogen Metabolism in Pancreatic Cancer",
      authors: "Peter Sajjakulnukit, Kira Holton, Tianrui Ma, Zhengxu Tang, Michael Akpabey",
      pdf: "./assets/files/bioinf545_group_6_final_report_ds.pdf",
      image: "./assets/files/img/545_final.jpg",
      field: "Bioinformatics",
      field_short: "Bioinfo"
    }
  ],
  computational_neuroscience: [
    {
      title: "Computational Neuroscience Project 1",
      authors: "Author C, Zhengxu Tang",
      pdf: "./assets/files/MATH_568_FInal_Project.pdf",
      image: "./assets/files/img/598_final.jpg",
      field: "Computational Neuroscience",
      field_short: "CompNeuro",
      code: "https://github.com/TangZhengxu/MATH568_FInal_Project_2023"
    }
  ],
  mathematics_modeling: [
    {
      title: "Mathematics Modeling Project 1",
      authors: "Zhengxu Tang, Author E",
      pdf: "./assets/files/462_final.pdf",
      image: "./assets/files/img/23661721135991_.pic_hd.jpg",
      field: "Mathematics Modeling",
      field_short: "MathModel"
    },
    {
      title: "Mathematics Modeling Project 2",
      authors: "Zhengxu Tang, Author F",
      pdf: "./assets/files/462_Midterm.pdf",
      image: "./assets/files/img/462_midterm.jpg",
      field: "Mathematics Modeling",
      field_short: "MathModel"
    }
  ]
};

const ProjectCard = ({ project }) => (
  <Card className="mb-6">
    <CardHeader>
      <h3 className="text-lg font-semibold">{project.title}</h3>
      <Badge>{project.field_short}</Badge>
    </CardHeader>
    <CardContent>
      <div className="flex flex-col md:flex-row">
        <img src={project.image} alt={project.title} className="w-full md:w-1/3 h-48 object-cover mb-4 md:mb-0 md:mr-4" />
        <div>
          <p className="mb-2">{project.authors.replace('Zhengxu Tang', '<strong>Zhengxu Tang</strong>')}</p>
          <p className="italic">{project.field}</p>
        </div>
      </div>
    </CardContent>
    <CardFooter className="flex justify-start space-x-2">
      {project.pdf && (
        <Button size="sm" variant="outline">
          <FileText className="mr-2 h-4 w-4" />
          PDF
        </Button>
      )}
      {project.code && (
        <Button size="sm" variant="outline">
          <Code className="mr-2 h-4 w-4" />
          Code
        </Button>
      )}
      {project.page && (
        <Button size="sm" variant="outline">
          <ExternalLink className="mr-2 h-4 w-4" />
          Project Page
        </Button>
      )}
    </CardFooter>
  </Card>
);

const ProjectsDisplay = () => (
  <div className="space-y-8">
    {Object.entries(projects).map(([category, projectList]) => (
      <div key={category}>
        <h2 className="text-2xl font-bold mb-4 capitalize">{category.replace('_', ' ')}</h2>
        {projectList.map((project, index) => (
          <ProjectCard key={index} project={project} />
        ))}
      </div>
    ))}
  </div>
);

export default ProjectsDisplay;