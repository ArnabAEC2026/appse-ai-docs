---
slug: /platform/key-concepts/nodes/built-in/base64-decode
title: Base64 Decode
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

The Base64 Decode node in APPSe AI is a built-in node that allows you to convert a Base64 string back into its original format. Many applications and APIs return files in a Base64 string format. This node helps decode that data into a text format that can be used in other nodes in your workflow.


1. From the selection screen, choose the Base64 Decode node.
<img src="\img\platform\key-concepts\nodes\built-in\base64-decode\selection-screen.png" alt="selection screen" width="700"/>

2. Connect it with a node that provides a Base64 string output.
<img src="\img\platform\key-concepts\nodes\built-in\base64-decode\select-a-desired-node.png" alt="select a desired node" width="700"/>

## Configuration

### Steps to Use Different File Types in the Base64 Node
 
Select the type of file you want to decode.

<Tabs>
<TabItem value="pdf" label="PDF" default>

#### Steps to Use the Base64 Node for PDF Files

3. Under **Type**, select the PDF format you want to decode.
<img src="\img\platform\key-concepts\nodes\built-in\base64-decode\select-type.jpg" alt="select type" width="700"/>


4. In the Base64 String field, enter or map the Base64-encoded string of the PDF you want to decode.
<img src="\img\platform\key-concepts\nodes\built-in\base64-decode\Continue1.png" alt="continue" width="700"/>

5. Click **Continue**, then run the node to decode the data.

6. After execution, the decoded PDF will be available as output for the next node in the workflow.
```json
[
	{
		"output": {
			"page_1": {
				"content": "Purchase Order Printing\nPage: 1\nPurchase Order\nP.O. Number: 1000 Order Date: 2/14/2026\nAccount #: A-1000\nORDERED BY: Fire Tailed\n421 Hobbs Street, Tampa, FL 33619-7880\nPhone: (813) 684-1782 --- Fax: (813) 654-4272\nVendor: Annin & Company, PO Box 847660, Boston, MA 02284-7660\nShip To: Fire Tailed, 421 Hobbs Street, Tampa, FL 33619\nOrdered Unit Cost Amount Item Name\n2.00 100.0 200.0 carbomer\nNet Order: 400.00\nSales Tax: 0.00\nFreight: 0.00\nOrder Total: 400.00\nPlease Ship 02/15/26 Destination\nOrder Balance: 400.00\nLess Prepaid: 0.00",
				"text": "Purchase Order Printing\nPage: 1\nPurchase Order\nP.O. Number: 1000 Order Date: 2/14/2026\nAccount #: A-1000\nORDERED BY: Fire Tailed\n421 Hobbs Street, Tampa, FL 33619-7880\nPhone: (813) 684-1782 --- Fax: (813) 654-4272\nVendor: Annin & Company, PO Box 847660, Boston, MA 02284-7660\nShip To: Fire Tailed, 421 Hobbs Street, Tampa, FL 33619\nOrdered Unit Cost Amount Item Name\n2.00 100.0 200.0 carbomer\nNet Order: 400.00\nSales Tax: 0.00\nFreight: 0.00\nOrder Total: 400.00\nPlease Ship 02/15/26 Destination\nOrder Balance: 400.00\nLess Prepaid: 0.00",
				"images_text": []
			}
		},
		"processing_time": 0.12,
		"pages_processed": 1
	}
]
```

:::note

The Base64 node currently supports only the PDF files that are **NOT** protected by a password.

:::

#### Example 
#### Input

Use a valid Base64 string for the selected PDF file type (sample shown below).

<img src="\img\platform\key-concepts\nodes\built-in\base64-decode\Input of PDF.jpg" width="700" />

#### Configuration

Provide the Base64-encoded string of the selected PDF in the **Base64 String** field.

<img src="\img\platform\key-concepts\nodes\built-in\base64-decode\continue.jpg" alt="pdf configuration" width="700" />

#### Output

The output displays the extracted PDF content in a structured response, which you can map to the next node.

<img src="\img\platform\key-concepts\nodes\built-in\base64-decode\PDF-Output.jpg" alt="output" width="700"/>

----------------

</TabItem>
<TabItem value="image" label="Image">

#### Steps to Use the Base64 Node for Image Files

3. Under **Type**, select the image format you want to decode.
<img src="\img\platform\key-concepts\nodes\built-in\base64-decode\Base64N-CNTNUE5.jpg" width="700" />

4. In the Base64 String field, enter or map the Base64-encoded string of the image you want to decode.

<img src="\img\platform\key-concepts\nodes\built-in\base64-decode\ExampleConfig.jpg" width="700" />

5. Click **Continue**, then run the node to decode the data.

6. After execution, the decoded image will be available as output for the next node in the workflow.
```json
[
	{
		"output": {
			"extracted_text": "Contrast\nDesign Principle\nContrast is an important element\nof graphic design because it\nallows different elements to\nstand out and grab attention.\nebaqdesign"
		},
		"processing_time": 5.37,
		"pages_processed": 1
	}
]
```

:::note
The Base64 node supports the following image file types: **PNG, JPG, JPEG, GIF, BMP, WEBP**.

:::

#### Example

#### Input

The following is a sample PNG image that will be used as input for this example.

<img src="\img\platform\key-concepts\nodes\built-in\base64-decode\Image-Input.jpg" width="700" />

#### Configuration

Provide the Base64-encoded string of the selected image in the **Base64 String** field.

<img src="\img\platform\key-concepts\nodes\built-in\base64-decode\ExampleConfig.jpg" width="700" />

#### Output

The output displays the decoded image text/content in JSON format, which you can map to the next node.

<img src="\img\platform\key-concepts\nodes\built-in\base64-decode\Base64N-Result6.jpg" width="700" />

</TabItem>
</Tabs>


