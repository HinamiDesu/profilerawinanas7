<template>
  <div>
    <Navbar />
    <section class="text-center detail">
    <h1>Contact</h1>
    
        <table style="width:100%; text-align: center">
            <tr>
                <td>
                    <!-- Form: https://developer.mozilla.org/en-US/docs/Web/HTML/Element#forms -->
                    <form action="mailto:abhisit_u@bu.ac.th" method="POST" enctype="text/plain">
                        <label for="yourName">{{Your_Name}}:</label>
                        <input type="text" id="yourName" name="yourName" value="">
                        <br>
                        <label for="yourEmail">{{Your_Email}}:</label>
                        <input type="email" id="yourEmail" name="yourEmail" value="">
                        <br>
                        <br />
                        <label for="yourMessage">{{Your_Message}}:</label>
                        <br>
                        <textarea id="yourMessage" name="yourMessage" cols="30" rows="10"></textarea>
                        <br>
                        <input type="submit" name="">
                        <br>
                        <p>Address:{{address}}</p>
                        <br>
                        <p>Email: <a href="mailto:rawinan@bumail.net">{{Email}}</a></p>
                        <br>
                        <p>Number: {{number}}</p>
                    </form>
                </td>
                    <!--Reference Social Media Icons of Awesome 4-->
                    <link rel="stylesheet"
                        href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css"> 
                    
            </tr>
        </table>
    </section>
  </div>
</template>

<script>
import Navbar from '../components/Navbar.vue'
export default {
    components: { Navbar },
    data (){
        return {
            Your_Name : 'Your Name',
            Your_Email : 'Your Email',
            Your_Message :'Your Message',
            Email : 'rawinan.kaew@bumail.net',
            address : 'Pathum Thani,Thailand',
            number : '-',
        }
    }

}
</script>

<style>

</style>