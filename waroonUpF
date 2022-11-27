let uploadFile ={}

$('input[type="file"]').on('change',function(e){   
  var x = e.target
  console.log(x)
  console.log(this)
  
  let files = []
        for(var i=0; i<x.files.length; i++){
     files.push(x.files[i])
  }
  console.log(files)
  files.forEach((file,i)=>{
    let reader = new FileReader()
    reader.onloadend = (e)=>{
      uploadFile[x.getAttribute('id')+(i+1)]={
        data:e.target.result.split(',')[1],
        name:file.name,
        type:file.type
      }
    }
    reader.readAsDataURL(file)
   })
  })
