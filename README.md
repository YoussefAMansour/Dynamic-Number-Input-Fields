# Dynamic Number Input Fields Component

This repository provides a Vue 3 component using Vuetify 3 that dynamically generates number input fields based on the selected number. It allows users to specify the number of input fields they want and enter corresponding values.

## Features

- **Dynamic Input Fields**: Input fields are generated dynamically based on the selected number.
- **Flexible Number Selection**: Users can choose the number of input fields they want to add.
- **Data Handling**: Entered values are captured and displayed as an array.
- **Clearable Input**: Input fields can be cleared individually or all at once.

## Installation

To integrate this component into your project, follow these steps:

1. **Clone the repository**:
   ```sh
   git clone https://github.com/YoussefAMansour/Dynamic-Number-Input-Fields

2. **Navigate to the project directory**:
    ```sh
   cd dynamic-number-input-fields

3.  **Install dependencies**:
    ```sh
    npm install
    
4.  **Run the project**:
    ```sh
    npm run serve

## Usage

Here's an example of how to use the VAutocomplete Infinite Scroll component in your Vue 3 application:
1. ```shell
    <template>
        <div>
        <DynamicNumberInputFields/>
      </div>
    </template>

    <script setup>
        import DynamicNumberInputFields from '@/components/DynamicNumberInputFields.vue';
    </scrpit>

## Configuration

The component can be customized through several props:

Props:
* numbers: Array of numbers to be displayed in the dropdown for selecting the number of input fields.

## Contributing

Contributions are welcome! If you have any ideas, suggestions, or improvements, feel free to open an issue or submit a pull request.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.
