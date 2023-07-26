<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Breaking point store</title>
    <style>
        /* Styles for the modal */
        .modal {
            display: none;
            position: fixed;
            z-index: 1;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            overflow: auto;
            background-color: rgba(0, 0, 0, 0.5);
        }

        .modal-content {
            background-color: #f4f4f4;
            margin: 10% auto;
            padding: 20px;
            border: 1px solid #888;
            width: 80%;
        }

        .close-button {
            float: right;
            cursor: pointer;
        }

        /* Style for the receipt background color */
        .receipt-success {
            background-color: #c5f6c5; /* Green */
        }

        .receipt-fail {
            background-color: #f6c5c5; /* Red */
        }
    </style>
</head>
<body>
    <h1>Breaking point store</h1>
    <form onsubmit="showConfirmationPopup(event)">
        <label for="item">Select an item:</label>
        <select id="item" name="item">
            <option value="Cosmic">Cosmic</option>
            <option value="Mellow">Mellow</option>
            <option value="eternal">eternal</option>
            <option value="Phantom">Phantom</option>
            <option value="Aureus">Aureus</option>
            <option value="Jade">Jade</option>
            <option value="Radiant">Radiant</option>
            <!-- Add more items as needed -->
        </select>
        <br>
        <label for="quantity">Quantity:</label>
        <input type="number" id="quantity" name="quantity" min="1" value="1" oninput="calculateTotal()">
        <br>
        <p id="totalPrice">Total: 100 Robux</p>
        <input type="submit" value="Buy">
    </form>

    <!-- Modal for the confirmation message -->
    <div id="confirmationModal" class="modal">
        <div class="modal-content">
            <span class="close-button" onclick="closeConfirmationModal()">&times;</span>
            <p>Please buy this <a href="#" id="gamePassLink" target="_blank">game pass</a> the times of quantity you want.</p>
            <p>Then DM TheDevil#1055 for trade.</p>
            <button onclick="confirmPurchase()">Confirm Purchase</button>
        </div>
    </div>

    <!-- Modal for the receipt message -->
    <div id="receiptModal" class="modal">
        <div class="modal-content">
            <span class="close-button" onclick="closeReceiptModal()">&times;</span>
            <h2>THANK YOU FOR PURCHASING</h2>
            <p id="receiptMessage"></p>
            <!-- You can add more details or styling here as needed -->
        </div>
    </div>

    <script>
        let gamePassClicked = false; // Flag to track if the game pass link was clicked

        function calculateTotal() {
            const quantity = parseInt(document.getElementById('quantity').value, 10);
            const totalPrice = quantity * 100; // Custom pricing: 100 Robux per item
            document.getElementById('totalPrice').textContent = `Total: ${totalPrice} Robux`;
        }

        function showConfirmationPopup(event) {
            event.preventDefault();
            const item = document.getElementById('item').value;
            const quantity = document.getElementById('quantity').value;
            const gamePassLink = `https://web.roblox.com/game-pass/214704809/Buyrie`; // Replace with your actual game pass link

            // Show the confirmation modal and set the game pass link
            const confirmationModal = document.getElementById('confirmationModal');
            const gamePassLinkElement = document.getElementById('gamePassLink');
            gamePassLinkElement.href = `${gamePassLink}${quantity}`;
            confirmationModal.style.display = 'block';
        }

        function confirmPurchase() {
            if (gamePassClicked) {
                showReceiptPopup(true); // True indicates successful purchase
            } else {
                showReceiptPopup(false); // False indicates purchase failure (didn't click the link)
            }
        }

        function showReceiptPopup(successfulPurchase) {
            const item = document.getElementById('item').value;
            const quantity = document.getElementById('quantity').value;
            const totalRobux = parseInt(quantity) * 100;

            // Show the receipt modal and display the purchased item information
            const receiptModal = document.getElementById('receiptModal');
            const receiptMessage = document.getElementById('receiptMessage');

            if (successfulPurchase) {
                receiptModal.classList.add('receipt-success');
                receiptMessage.textContent = `Item: ${item}, Quantity: ${quantity}, Total Robux: ${totalRobux}`;
            } else {
                receiptModal.classList.add('receipt-fail');
                receiptMessage.textContent = "Did not pay, please click the link above to pay.";
            }

            receiptModal.style.display = 'block';
        }

        // Function to set the gamePassClicked flag when the game pass link is clicked
        document.getElementById('gamePassLink').addEventListener('click', function() {
            gamePassClicked = true;
        });

        // Function to close the confirmation modal
        function closeConfirmationModal() {
            const confirmationModal = document.getElementById('confirmationModal');
            confirmationModal.style.display = 'none';
        }

        // Function to close the receipt modal
        function closeReceiptModal() {
            const receiptModal = document.getElementById('receiptModal');
            receiptModal.style.display = 'none';
            // Reset modal color classes so that it doesn't affect the next purchase
            receiptModal.classList.remove('receipt-success', 'receipt-fail');
        }
    </script>
</body>
</html>

<p>It took a very long time to make, So I would extremly appriciate some tips that I can make more in the future, talk to me if you want to tip or have any feedback/sugestions, I am always online on discord TheDevil#1055 :)</p>



