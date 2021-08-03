<template>
  <div class="form-container">
      <form>
          <div class="form-control">
             <label for="email">Email</label>
             <input type="email" class="email" v-model="email"/>
          </div>
           <div class="form-control">
             <label for="password">Password</label>
             <input type="password" class="password" v-model="password"/>
          </div>

          <div class="form-control">
               <label for="role">Role</label>
                <select id="role" v-model="role">
                    <option value="developer">Web Developer</option>
                    <option value="designer">Web Designer</option>
                </select>
          </div>

            <div class="accept">
                <input type="checkbox" id="policy" v-model="accept"/>
                <label for="policy">Accept terms and conditions</label>
            </div>

            <div class="programLanguage">
                <div class="program">
                    <input type="checkbox" value="python" v-model="names"/>
                    <label>Python</label>
                    
                </div>
                <div class="program"> 
                    <input type="checkbox" value="java" v-model="names"/>
                    <label>Java</label>
                    
                </div>
                  <div class="program">
                    <input type="checkbox" value="php" v-model="names"/>
                    <label>Php</label>
                </div>

            </div>
            <div class="gendergp">
                <input type="radio" id="male" value="male" v-model="gender"/>
                <label for="male">Male</label>
                <input type="radio" id="female" value="female" v-model="gender"/>
                <label for="female">Female</label>
            </div>

            <div class="form-control">
                <label for="skill">Skills</label>
                <input type="text" id="skill" @keyup="addSkills" v-model="skill"/>
            </div>
            
        
      </form>
      
  </div>
  <h3>Email-{{email}}</h3>
  <h3>Password-{{password}}</h3>
  <h3>Role-{{role}}</h3>
  <h3>Accept-{{accept}}</h3>
  <h3>Selected Programming Language:{{names}}</h3>
  <h3>Gender-{{gender}}</h3>
  <h3>Skill-{{skill}}</h3>
  <h3>SkillsArray-{{skills}}</h3>
</template>

<script>
export default {
    data(){
        return {
            email:"zarli@gmail.com",
            password:"12345",
            role:'developer',
            accept:true,
            names:["python"],
            gender:'male',
            skill:'',
            skills:[]
        }
    },
    methods:{
        addSkills(e){
        //    console.log(e.key);
        if(e.key===','){
            this.skills.push(this.skill);
            this.skill=''
        }
        }
    }
}
</script>

<style scoped> 
      *{
          box-sizing: border-box;
      }
     .form-container{
         /* height: 500px; */
         width: 400px;
         box-shadow: 0px 10px 10px rgba(0,0,0,0.4);
         padding:20px 20px;
         margin:auto;
     }
     .form-control{
         width:100%;

         position: relative;
     }
     .form-control label{
          color:rgb(5, 17, 180);
          display: block;
          margin: 7px;
     }
     
     .form-control input,.form-control select{
         width:100%;
         padding:5px;
         margin:0px 0px 10px 0px;
         border:0;
         border-bottom: 2px solid pink;
         background-color:transparent;
     }
     .accept{
        margin-bottom: 2px;
        padding:10px 0px;
     }
     .program{
        margin-bottom: 2px;
        padding:6px 0px;
     }
     .gendergp{
         margin: 5px 0px;
     }
    
</style>