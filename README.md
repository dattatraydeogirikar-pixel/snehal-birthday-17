<script>
// Hide letter and questions at the start
document.getElementById('letter').style.display = 'none';
document.getElementById('questions').style.display = 'none';
document.getElementById('finalMessage').style.display = 'none';

// Password to unlock letter
const password = "snehashay1303";

function checkPassword(){
  const input = document.getElementById('passwordInput').value;
  if(input === password){
    // Hide password section
    document.getElementById('passwordSection').style.display = 'none';
    // Show letter and questions
    document.getElementById('letter').style.display = 'block';
    document.getElementById('questions').style.display = 'block';
  } else {
    document.getElementById('passwordMsg').innerText = "Incorrect password. Try again!";
  }
}

function showFinal(){
  document.getElementById('questions').style.display = 'none';
  document.getElementById('finalMessage').style.display = 'block';
}
</script>
