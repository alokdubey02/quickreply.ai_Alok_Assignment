# React Component Library

This repository contains a collection of reusable React components for building user interfaces. Each component is accompanied by stories that showcase different variations and use cases.

## Getting Started

To get started, follow these steps:

### Clone the Repository

git clone <repository_url>

### Navigate to Project Directory

cd <project_directory>

### Install Dependencies

npm install

### Run Storybook

npm run storybook

Once the Storybook server is running, you can view the components and their variations by navigating to `http://localhost:6006` in your browser.

## Components

### 1. ProgressStep

The `ProgressStep` component visualizes progress through a series of steps.

#### Usage

import ProgressStep from "../components/ProgressStep";

<ProgressStep
orientation="horizontal"
steps={[
{ title: "Step 1", description: "Step 1 description" },
{ title: "Step 2", description: "Step 2 description" },
{ title: "Step 3", description: "Step 3 description" },
]}
currentStepIndex={0}
/>;

#### Stories

- **Horizontal**: Displays progress steps horizontally.
- **Vertical**: Displays progress steps vertically.
- **Cell**: Displays progress steps in a grid cell layout.

#### Controls

- **orientation**: Sets the orientation of the progress steps. Options: `"horizontal"`, `"vertical"`, `"cell"`.
- **steps**: An array of objects representing each step in the progress. Each object should contain `title` and `description` properties.
- **currentStepIndex**: Index of the current step.
- **stepName**: Default step name to be displayed.
- **description**: Default description to be displayed.
- **editDescription**: Boolean value to enable editing of the description.
- **line**: Boolean value to display the connector line between steps.
- **success**: An array of booleans indicating the success state of each step.

### 2. Button

The `Button` component represents a clickable button element.

#### Usage

import Button from "../components/Button";

<Button
label="Press Me"
backgroundColor="red"
size="md"
onClick={() => console.log("Button clicked")}
/>;

#### Stories

- **Red**: Button with red background color.
- **Green**: Button with green background color.
- **Small**: Small-sized button.
- **Large**: Large-sized button.
- **LongLabel**: Button with a long label.

#### Controls

- **label**: Text to be displayed on the button.
- **backgroundColor**: Background color of the button. Options: Any valid CSS color value.
- **size**: Size of the button. Options: `"sm"`, `"md"`, `"lg"`.
- **onClick**: Function to be called when the button is clicked.

### 3. Stack

The `Stack` component arranges its children in a horizontal or vertical stack.

#### Usage

import Stack from "../components/Stack";

<Stack direction="row" spacing={2} wrap={false}>
  <div>Child 1</div>
  <div>Child 2</div>
  <div>Child 3</div>
</Stack>;

#### Stories

- **Horizontal**: Stack children horizontally.
- **Vertical**: Stack children vertically.
- **NoSpacing**: Stack children with no spacing.
- **WrapOverflow**: Stack children with wrapping for overflow.
- **Empty**: Empty stack.

#### Controls

- **spacing**: Spacing between stack children.
- **wrap**: Boolean value to enable wrapping of children.
- **direction**: Direction of the stack. Options: `"row"`, `"column"`.
- **numberOfChildren**: Number of children to be rendered in the stack.

## Development

Feel free to contribute to this repository by adding new components, improving existing ones, or fixing bugs. Please adhere to the existing coding style and conventions.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

This README provides detailed instructions on getting started with the project, an overview of the components, their usage examples, stories, and available controls for customization. It also includes information on contributing to the project and the project's license.
