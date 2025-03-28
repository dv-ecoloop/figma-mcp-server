# Figma MCP Server

A simple local server for Figma's MCP (Model Context Protocol) development.

## Description

This repository provides a lightweight server implementation for developing and testing Figma MCP features locally. It uses the official `figma-developer-mcp` package to facilitate multiplayer collaboration features in Figma plugins.

## Prerequisites

- Node.js (v14 or higher)
- npm or Yarn

## Setup

1. Clone the repository:
   ```
   git clone https://github.com/dv-ecoloop/figma-mcp-server.git
   cd figma-mcp-server
   ```

2. Install dependencies:
   ```
   npm install
   # or
   yarn install
   ```

3. Configure environment variables:
   - Copy `.env.example` to `.env`
   - Add your Figma API key to the `.env` file

### Creating a Figma API Key

To generate a personal access token for Figma:

1. From the file browser in Figma, click the account menu in the top-left corner and select **Settings**
2. Select the **Security** tab
3. Scroll to the **Personal access tokens** section, then click **Generate new token**
4. Enter a name for your new token and press Return/Enter
5. Copy the token that is generated

**Note**: The token only displays immediately after being generated. If you navigate away from the page, you will not be able to copy the token and will have to generate a new one.

For more details, see the [Figma documentation on managing personal access tokens](https://help.figma.com/hc/en-us/articles/8085703771159-Manage-personal-access-tokens).

## Usage

Start the development server:

```
npm run dev
# or
yarn dev
```

The server will start on the port specified in your `.env` file (default: 3333).

## Configuration

- `FIGMA_API_KEY`: Your Figma API key (required)
- `PORT`: The port on which the server will run (default: 3333)

## Implementation Details

This project is built using the [Figma-Context-MCP](https://github.com/GLips/Figma-Context-MCP) library, which provides tools for interfacing with Figma's API through the Model Context Protocol. This allows AI coding agents like Cursor to access Figma layout information.

## License

MIT
