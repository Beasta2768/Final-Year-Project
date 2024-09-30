
<%*  
// Sets up Top of file info
let typeTitle = ""
const topic = await tp.system.prompt("Please enter the topic")
const week = await tp.system.prompt("Please enter the week") 
const type =  await tp.system.suggester(["Online", "In Person", "Workshop", "Tutorial"], ["Online", "In Person", "Workshop", "Tutorial"]) 

// Determines typeTitle
if (type == "Online" || type == "In Person"){
	typeTitle = "Lecture";
} else {
	typeTitle = type
}
await tp.file.rename( "Week "+ week +" (" + typeTitle + ") " + topic ) 
let content =  "\n Topic::" + topic + "\n Date:: " + tp.file.creation_date("DD/MM/YY")  + "\n Week:: " +  week + "\n Type::" + type

// gets all the week folders
const folders = this.app.vault.getAllLoadedFiles().filter(i => i.children).map(folder => folder.path).filter(week => week.includes("Week") && ! week.includes("Images"));
const folderChoicePath = await tp.system.suggester(folders, folders);
if (folderChoicePath != null ){
	new Notice (folderChoicePath +" Selected", 5000)
	// Get all the files in the folder
	const files = app.vault.getMarkdownFiles();
	const filesInFolder = new Array();
	console.log("folderChoicePath: " + `${folderChoicePath}`)
	files.forEach((file) => {
	//console.log("file.path: " + `${file.path}`)
	if (file.path.includes(folderChoicePath+"/")) {
		filesInFolder.push(file.basename)
	};
	})
	// List of files from that week  to be added to md file
	const filesList = new Array();
	filesInFolder.forEach((file) => {
		//console.log(file)
		filesList.push('\n - [[' + file + ']]')
	});
	
	content += "\n\n Last Weeks Notes" + filesList.sort((a, b) => a.toLowerCase().localeCompare(b.toLowerCase())).join('')
}
	content +=  "\n# " + topic
	await tp.file.cursor_append(content)

_%>