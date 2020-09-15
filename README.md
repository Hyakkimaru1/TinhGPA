# TinhGPA
Tinh diem GPA tren portal


#script:\
const tbody = document.getElementsByTagName('tbody')[1];\
let sum = 0;\
let tt = 0;\
for (let index = 0;index < tbody.childElementCount;index++){\
 &nbsp;if (!tbody.children[index].children[1].innerText.includes('Anh văn') &&\
      !tbody.children[index].children[1].innerText.includes('Giáo dục quốc phòng') && \
      !tbody.children[index].children[1].innerText.includes('Thể dục'))\
  {\
      tt+= +tbody.children[index].children[2].innerText;\
      sum+= (+tbody.children[index].children[5].innerText*+tbody.children[index].children[2].innerText);\
  }\
}\

console.log("GPA: ",sum/tt);
