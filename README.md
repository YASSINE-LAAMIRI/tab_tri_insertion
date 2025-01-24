# tab_tri_insertion



ALGORITHM tri_insertion
VAR
    n:INTEGER
BEGIN
    write("Entrez la taille du tableau : ");
    read(n);

   //remplissage du tableau
    write("Entrez les elements du tableau : ");
    FOR i FROM 0 TO n-1 DO
        read(tab[i]);
    END

    //tri par insertion
    FOR i FROM 1 TO n-1 step 1 DO
        x:=tab[i];
        j:=i-1;
        WHILE j>=0 AND tab[j]>x DO
            tab[j+1]:=tab[j];
            j:=j-1;
        END WHILE
        tab[j+1]:=x;
    END FOR

    //affichage du tableau trié
    write("Le tableau trié est : ");
    FOR i FROM 0 TO n-1 DO
        write(tab[i]);

END
