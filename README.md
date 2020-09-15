# TinhGPA
Tinh diem GPA tren portal


<h3>script:</h3>\
const tbody = document.getElementsByTagName('tbody')[1];\
let sum = 0;\
let tt = 0;\
for (let index = 0;index < tbody.childElementCount;index++){\
 &nbsp;&emsp;if (!tbody.children[index].children[1].innerText.includes('Anh văn') &&\
      &emsp;&emsp;!tbody.children[index].children[1].innerText.includes('Giáo dục quốc phòng') && \
      &emsp;&emsp;!tbody.children[index].children[1].innerText.includes('Thể dục'))\
  &emsp;&emsp;{\
      &emsp;&emsp;&emsp;tt+= +tbody.children[index].children[2].innerText;\
      &emsp;&emsp;&emsp;sum+= (+tbody.children[index].children[5].innerText*+tbody.children[index].children[2].innerText);\
  &emsp;&emsp;}\
}

console.log("GPA: ",sum/tt);
