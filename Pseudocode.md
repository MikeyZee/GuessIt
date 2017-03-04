BEGIN MAINPROGRAM
	Get difficulty
		CASEWHERE difficulty is
			"Easy": gennum = Random(50 - 1) + 1
			"Medium": gennum = Random(100 - 1) + 1
			"Hard": gennum = Random(200 - 1) + 1
		ENDCASE
		WHILE guess != gennum
			Get guess
				if guess > gennum THEN
					Output “Lower”
				ELSE
					Output “Higher”
				ENDIF
		ENDWHILE
	Output “YOU WIN!!”
END
