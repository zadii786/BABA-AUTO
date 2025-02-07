function showPaymentOptions(productName, price) {
    const productInfo = document.getElementById("productInfo");
    productInfo.innerHTML = `You are purchasing <strong>${productName}</strong> for <strong>${price} PKR</strong>.`;
    
    const paymentPopup = new bootstrap.Modal(document.getElementById("paymentPopup"));
    paymentPopup.show();
    
    const whatsappBtn = document.getElementById("whatsappBtn");
    whatsappBtn.onclick = function() {
        window.location.href = `https://wa.me/923001234567?text=I want to buy ${productName} for ${price} PKR.`;
    };
}

function closePopup() {
    const paymentPopup = bootstrap.Modal.getInstance(document.getElementById("paymentPopup"));
    paymentPopup.hide();
}

// Function to display truck images
document.addEventListener("DOMContentLoaded", function() {
    const truckImages = [
        "truck1.jpg", "truck2.jpg", "truck3.jpg", "truck4.jpg", "truck5.jpg",
        "truck6.jpg", "truck7.jpg", "truck8.jpg", "truck9.jpg", "truck10.jpg"
    ];

    const truckGallery = document.getElementById("truckGallery");

    truckImages.forEach(image => {
        const imgElement = document.createElement("img");
        imgElement.src = image;
        imgElement.alt = "Truck Image";
        imgElement.classList.add("truck-image");
        truckGallery.appendChild(imgElement);
    });
});
