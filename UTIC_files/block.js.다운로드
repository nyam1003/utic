function SourceBlock(processKey, mouseRightClick, cotnextmenu, drag, select, statuslink) {
	this.bProcessKey = processKey ? false : true;
	this.bMouseRightClick = mouseRightClick ? false : true;
	this.bContextmenu = cotnextmenu ? false : true;
	this.bDragable = drag ? false : true;
	this.bSelectable = select ? false : true;
	this.bStatusLink = statuslink ? false : true;

	// 다른창에 띄우기(ctrl + n) & 새로고침(ctrl + r) & 뒤로가기(8) & F1~F12(112~123)
	this.blockProcessKey = function() {
		if ((event.ctrlKey == true && (event.keyCode == 78 || event.keyCode == 82))
				|| (event.keyCode >= 112 && event.keyCode <= 123)) {
			event.keyCode = 0;
			event.cancelBubble = true;
			event.returnValue = false;
		}
	};

	this.blockMouseClick = function() {
		if (event.button == 2)
			return;
	};

	this.blockContextmenu = function() {
		return false;
	};

	this.blockDrag = function() {
		return false;
	};

	this.blockSelect = function() {
		return false;
	};

	blockStatusLink = function() {
		window.status = "www.utic.go.kr";
	};

	if (this.bProcessKey){
		document.onkeydown = this.blockProcessKey;
	}
	if (this.bMouseRightClick){
		document.onmousedown = this.blockMouseClick;
	}
	if (this.bContextmenu){
		document.oncontextmenu = this.blockContextmenu;
	}
	if (this.bDragable){
		document.ondragstart = this.blockDrag;
	}
	if (this.bSelectable){
		document.onselectstart = this.blockSelect;
	}
	if (this.bStatusLink){
		blockStatusLink();
	}
}
