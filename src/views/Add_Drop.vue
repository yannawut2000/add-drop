<script setup>
import {ref} from "vue";

const stuID=ref("");
const stuName=ref("");

</script>

<template>

    <div class="container py-4">
      
    
        <h2>คำร้องขอโอนย้ายสาขาวิชาต่างคณะ</h2>
        <h2>สำหรับหลักสูตร 4 ปี และหลักสูตร 4ปีเทียบเข้าเรียน(2ปี)</h2>
    </div>

  <form>
   <div class="intomju">
    <h3>เขียนที่  มหาวิทยาลัยแม่โจ้ </h3>
    <h3>วันที่ <input type="numbar" v-model=day name="day" id="day" min="0" max="31" step="10"  maxlength="2" required>
        เดือน<input type="month" v-model=month name="month" id="month" maxlength="2" required>
        พ.ศ. <input type="year" v-model=year name="year" id="year" maxlength="4" required></h3>
   </div>
  
   
   <div class="intomju_2">
      <b>เรื่อง</b>   ขอโอนย้ายสาขาวิชาต่างคณะ
   </div>

   <div class="intomju_3">
    <b>เรียน</b>   คณบดีคณะ <select nname="" id="">
  <option>วิทยาศาสตร์</option>
  <option>บริหาร</option>
  <option>ท่องเที่ยว</option>
  <option>ศิลปศาสตร์</option>
</select>
   </div>

   <div class="intomju_4">
    <b>สิ่งที่แนบมาด้วย</b>   ใบรายงานผมการศึกษา
   </div>

   
   <div class="myname">
      <b>ข้าพเจ้า</b>  <select stumyName="" id="stumyName">
    <option>นาย</option>
    <option>นาง</option>
    <option>นางสาว</option>
    </select>
    ชื่อ-นามสกุล.<input type="text" v-model=stuName name="stuName" id="stuName" maxlength="100" required>
   </div>


   <div class="mynumbar">
      <b>รหัสนักศึกษา.</b>  <input type="text" v-model=stuID name="stuID" id="stuID" required>


         <b>หมายเลยโทรศัพท์.</b><input type="text" v-model=stuNum name="stuNum" id="stuNum" maxlength="10" required>


        <b>ระบบหลักสูตร</b> <select fourorfive="" id="fourorfive">
        <option>4-5 ปี</option>
        <option>4ปีเทียบเข้าเรียน(2ปี)</option></select>


        <b>ภาคเรียน</b> <select yy="" id="yy">
        <option>ภาคปกติ</option>
        <option>ภาคสมทบ</option> </select>
        <br>
        <br>
        
        <b>สาขาวิชา</b> <input type="text" v-model=stustacy name="stdstacy" id="stustacy" maxlength="100" required>
        <b>คณะ</b> <input type="text" v-model=stustacy_2 name="stdstacy_2" id="stustacy_2" maxlength="100" required>
          <br>
          <br>
          มีความประสงค์จะขอโอนย้ายไปสาขาวิชา<input type="text" v-model=stustacy_what name="stdstacy_what" id="stustacy_what" maxlength="100" required>
          เนื่องจาก<input type="text" v-model=stustacy_why name="stdstacy_why" id="stustacy_why"  required>

          <br>
          <br>
          ทั้งนี้ ข้าพเจ้ามีคุณสมบัติครบถ้วนในการขอย้ายสาขาวิชา  ดังนี้  คือ<br><br>
          <b><ins>หลักสูตร  4  เทียบเข้าเรียน(2ปี)</ins></b><br><br>
          -  ได้ศึกษาตามแผนการศึกษาในสาขาวิชาเดิมมาแล้วไม่น้อยกว่า  <b><ins>1  ภาคการศึกษาปกติ</ins></b><br><br>
          -  มีหน่วยกิตสะสมไม่น้อยกว่า  <b><ins>30</ins></b>  หน่วยกิต  และมีแต้มระดับคะแนนเฉลี่ยสะสม <b><ins>1  ไม่น้อยกว่า  2.00</ins></b><br>
   
          
          <br>
          <br>
          <b><ins>หลักสูตร  4  เทียบเข้าเรียน</ins></b><br><br>
          -  ได้ศึกษาตามแผนการศึกษาในสาขาวิชาเดิมมาแล้วไม่น้อยกว่า  <b><ins>2  ภาคการศึกษาปกติ</ins></b><br><br>
          -  มีหน่วยกิตสะสมไม่น้อยกว่า  <b><ins>30</ins></b>  หน่วยกิต  และมีแต้มระดับคะแนนเฉลี่ยสะสม <b><ins>1  ไม่น้อยกว่า  2.00</ins></b><br>
          <br>และยื่นคำร้องโอนย้ายสาขาวิชาภายในคณะก่อนวันที่
          <input type="numbar" v-model=day_2 name="day_2" id="day_2" min="0" max="31" step="10"  maxlength="2" required>
        เดือน<input type="month" v-model=month_2 name="month_2" id="month_2" maxlength="2" required>
        พ.ศ. <input type="year" v-model=year_2 name="year_2" id="year_2" maxlength="4" required>
          <br><br>
          จึงเรียนมาเพื่อโปรดพิจารณาอนุมัติ<br>
          <h4>ขอแสดงความนับถือ<br> <input type="text" v-model=stuName_End name="stuName_End" id="stuName_End"  required><br>
          นักศึกษา<br><br>

          <input type="submit" name="senner" value="ยืนยันลาออก"> </h4>
   
   </div>


  
  
  
  

  

 

  


รายชื่อทั้งหมดที่ถูกบันทึก
{{day}} {{ month }} {{ year }}  {{ stuName}}  {{ stuID }} {{ stuNum }} {{ stustacy }} {{ stustacy_2 }} {{ stustacy_what }} {{ stustacy_why }}
</form>
</template>

<style scoped>

</style>
