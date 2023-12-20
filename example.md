---
layout: default
---

<style>
/* Add CSS styles here */
/* Your existing styles here */
.table-container {
  position: relative;
  overflow: hidden;
}

.table-container:hover .floating-table {
  transform: translateY(-10px);
  transition: transform 0.3s ease-in-out;
  box-shadow: 0px 8px 16px rgba(0, 0, 0, 0.2);
  background-color: #fff;
}

.floating-table {
  position: relative;
  z-index: 1;
  transition: transform 0.3s ease-in-out;
  border-collapse: collapse;
  margin: 0;
}

.floating-table th,
.floating-table td {
  padding: 8px 12px;
  border: 1px solid #ccc;
}

</style>

Text can be **bold**, _italic_, or ~~strikethrough~~.

[Link to another page](./another-page.html).

<!-- Add a container for the table -->
<div class="table-container">
  <table class="floating-table">
    <!-- Your table content here -->
    <thead>
      <tr>
        <th>Head1</th>
        <th>Head Two</th>
        <th>Three</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>ok</td>
        <td>good swedish fish</td>
        <td>nice</td>
      </tr>
      <tr>
        <td>out of stock</td>
        <td>good and plenty</td>
        <td>nice</td>
      </tr>
      <tr>
        <td>ok</td>
        <td>good `oreos`</td>
        <td>hmm</td>
      </tr>
      <tr>
        <td>ok</td>
        <td>good `zoute` drop</td>
        <td>yumm</td>
      </tr>
    </tbody>
  </table>
</div>

There should be whitespace between paragraphs.

There should be whitespace between paragraphs. We recommend including a README, or a file with information about your project.

# Header 1

This is a normal paragraph following a header. GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere.

<!-- The rest of your Markdown content... -->
