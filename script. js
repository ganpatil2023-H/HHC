const form=document.getElementById("loginForm");
const email=document.getElementById("email");
const password=document.getElementById("password");
const emailError=document.getElementById("emailError");
const passwordError=document.getElementById("passwordError");
const message=document.getElementById("formMessage");
const button=document.getElementById("signInButton");

document.getElementById("togglePassword").addEventListener("click",()=>{
  const isPassword=password.type==="password";
  password.type=isPassword?"text":"password";
  document.getElementById("togglePassword").textContent=isPassword?"◉":"◉";
});

form.addEventListener("submit",(e)=>{
  e.preventDefault();
  emailError.textContent="";
  passwordError.textContent="";
  message.textContent="";
  let valid=true;

  if(!email.value.trim()){
    emailError.textContent="Please enter your email address.";
    valid=false;
  }else if(!/^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(email.value.trim())){
    emailError.textContent="Please enter a valid email address.";
    valid=false;
  }

  if(!password.value){
    passwordError.textContent="Please enter your password.";
    valid=false;
  }else if(password.value.length<6){
    passwordError.textContent="Password must be at least 6 characters.";
    valid=false;
  }

  if(!valid)return;

  button.disabled=true;
  button.innerHTML="Signing in…";
  setTimeout(()=>{
    button.disabled=false;
    button.innerHTML='Sign In <span>→</span>';
    message.textContent="Demo login validated. Connect your authentication API to enable real sign-in.";
  },700);
});

document.getElementById("forgot").addEventListener("click",(e)=>{
  e.preventDefault();
  message.textContent="Password recovery will be connected to your authentication service.";
});
document.getElementById("microsoft").addEventListener("click",()=>{
  message.textContent="Microsoft SSO is ready to be connected to your identity provider.";
});
document.getElementById("contact").addEventListener("click",(e)=>{
  e.preventDefault();
  message.textContent="Please contact your organization administrator for an account.";
});
