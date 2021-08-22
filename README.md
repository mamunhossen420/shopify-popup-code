# shopify-popup-code

<html>
<head>
<button id="contact-modal-button" class="btn sign-up-bank-btn">sign up now <br> via bank transfer</button> 
<script type="text/javascript" src="https://cdn.jsdelivr.net/npm/emailjs-com@2/dist/email.min.js"></script>


<div id="modal-contact-dark-overlay"> </div>
<div id="contact-modal-container">
	<div id="contact-modal">
		<button id="contact-modal-exit">&#x2715;</button>
		<p id="modal-success-message"></p>
		<div id="contact-modal-form-content">
			
		</div>
	</div>
</div>
</head>
<body>


<script>
const showOverlay = () => document.querySelector("#modal-contact-dark-overlay").style.display = "block";
const showModal = () => document.querySelector("#contact-modal-container").style.display = "block";
const hideOverlay = () => document.querySelector("#modal-contact-dark-overlay").style.display = "none";
const hideModal = () => document.querySelector("#contact-modal-container").style.display = "none";

// Open the Modal Window
document.querySelector("#contact-modal-button").onclick = function(){
showOverlay();
showModal();
}

// Close the Modal Window by clicking the X
document.getElementById("contact-modal-exit").onclick = function(){
hideOverlay();
hideModal();
}

// Close the Modal Window by clicking outside the box
window.onclick = function(event) {
if(event.target === document.querySelector('#contact-modal-container')) {
hideOverlay();
hideModal();
}
}
</script>


<style>
@media only screen and (max-width: 768px) {
  div#contact-modal-container {
	width:97%;
    right: 0;
    left: 0;
	margin:auto;
   }
  #contact-modal{
	  width:97%;
	  max-width:97%;
	}
}

  
#modal-contact-dark-overlay {
  display: none;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.7);
  overflow: auto;
  animation-name: animateopacity;
  animation-duration: 0.5s;
}
@keyframes animateopacity {
  from {background-color: rgba(0, 0, 0, 0.0)}
  to {background-color: rgba(0, 0, 0, 0.7)}
}
#contact-modal-container {
	position: absolute;
    top: -700%;
    left: -45%;
    right: 50%;
    bottom: 0;
    z-index: 9999;
}
#contact-modal {
  position: relative;
  margin: 0 auto;
  background-color: white;
  width: 500px;
  height: auto;
  padding: 15px 20px;
  animation: drop-in 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275);
  transform: translate(0%, -25%);
  top: 25%;
}
#contact-modal-exit {
  position: absolute;
  right: 20px;
  border:none;
  background:none;
  font-size: 18px;
}
.hide-modal-content {
	display: none;
}
 .contact-modal-form-content form{
	width:100% !important;
 }
 
  @media only screen and (min-width: 768px){
	  form#create_customer {
	   width: 100% !important;
	}
}
	
 #contact-modal-button{
  	font-size:14px !important;
    font-family: 'poppins';
    font-weight: 400;
	padding:10px 30px !important;
	line-height: 17px !important;
	transition:all 0.2s !important;
	border:2px solid white !important;
    background: #890609;
    color: white;
    text-transform: capitalize;
}
 #contact-modal-button:hover{
  	background-color:transparent;
	color:white !important;
	transform: scale(.9);
	transition:all 0.2s !important;
	border-color:#890609 !important;
}
</style>
</body>
</html>
