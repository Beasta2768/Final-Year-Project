<%*  
// gets all the week folders

const type = await tp.system.suggester(["Last Lecture", "Next Lecture"],["Last Lecture", "Next Lecture"])

const folders = this.app.vault.getAllLoadedFiles().filter(i => i.children).map(folder => folder.path).filter(week => week.includes("Week") && ! week.includes("Images"));

const folderChoicePath = await tp.system.suggester(folders, folders);

if (folderChoicePath != null ){
	new Notice (folderChoicePath +" Selected", 5000)
	// Get all the files in the folder
	const files = app.vault.getMarkdownFiles();
	const filesInFolder = new Array();
	console.log("folderChoicePath: " + `${folderChoicePath}`)
	files.forEach((file) => {
	if (file.path.includes(folderChoicePath+"/")) {
		filesInFolder.push(file.basename)
	};
	})
	// List of files from that week  to be added to md file
	const file = await tp.system.suggester(filesInFolder,filesInFolder)
	// Sets Link text
	let content = "";
	if (type === "Last Lecture"){
		content = "[["+ file +"|Last Lecture]]\n";
	} else {
		content = "[["+ file +"|Next Lecture]]\n";
	} 
	
	// appends lecture link to cursor
	await tp.file.cursor_append(content)

}
_%>