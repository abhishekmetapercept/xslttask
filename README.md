<?xml version="1.0"?>
<?xml version="1.0" encoding="UTF-8"?> 
<?xml-stylesheet type="text/xsl "href="Rule.xsl" ?> 
<html>
  <body>
 <h1 align="center"> Full Table</h1> 
   <table border="3" align="center" > 
   <tr> 
    <th>Book id</th> 
    <th>Author</th> 
    <th>Title</th> 
    <th>Genre</th>
     <th>Price</th>
     <th>Publish_date</th>
     <th>Description</th>
   </tr> 
    <xsl:for-each select="catalog/book"> 
   <tr> 
    <td><xsl:value-of select="book id"/></td> 
    <td><xsl:value-of select="author"/></td> 
    <td><xsl:value-of select="title"/></td> 
    <td><xsl:value-of select="genre"/></td> 
     <td><xsl:value-of select="price"/></td> 
     <td><xsl:value-of select="publish_date"/></td> 
     <td><xsl:value-of select="description"/></td> 
   </tr> 
    </xsl:for-each> 
    </table> 
    
    
    
    
    
    
    
    
    
    
    
    
    <h1 align="center">Table with price more than 10</h1> 
   <table border="3" align="center" > 
   <tr> 
    <th>Book id</th> 
    <th>Author</th> 
    <th>Title</th> 
    <th>Genre</th>
     <th>Price</th>
     <th>Publish_date</th>
     <th>Description</th>
   </tr> 
    <xsl:for-each select="catalog/book"> 
        <xsl:if test="price>10"> 
   <tr> 
    <td><xsl:value-of select="book id"/></td> 
    <td><xsl:value-of select="author"/></td> 
    <td><xsl:value-of select="title"/></td> 
    <td><xsl:value-of select="genre"/></td> 
     <td><xsl:value-of select="price"/></td> 
     <td><xsl:value-of select="publish_date"/></td> 
     <td><xsl:value-of select="description"/></td> 
   </tr> 
    </xsl:for-each> 
    </table> 
  
  
  
  
  
  
  
  
  
  
  
  
  
  <h1 align="center">Table with Gambardella, Matthew</h1> 
   <table border="3" align="center" > 
   <tr> 
    <th>Book id</th> 
    <th>Author</th> 
    <th>Title</th> 
    <th>Genre</th>
     <th>Price</th>
     <th>Publish_date</th>
     <th>Description</th>
   </tr> 
    <xsl:for-each select="catalog/book[author='Gambardella, Matthew']"> 
  
   <tr> 
    <td><xsl:value-of select="book id"/></td> 
    <td><xsl:value-of select="author"/></td> 
    <td><xsl:value-of select="title"/></td> 
    <td><xsl:value-of select="genre"/></td> 
     <td><xsl:value-of select="price"/></td> 
     <td><xsl:value-of select="publish_date"/></td> 
     <td><xsl:value-of select="description"/></td> 
   </tr> 
    </xsl:for-each> 
    </table> 
  
  
 
 
 
 
 
 
 
 
 
  <h1 align="center">Table with Author and Book Title</h1> 
   <table border="3" align="center" > 
   <tr>  
    <th>Author</th> 
    <th>Book Title</th>
   </tr> 
    <xsl:for-each select="catalog/book"> 
   <tr> 
    <td><xsl:value-of select="author"/></td> 
    <td><xsl:value-of select="title"/></td> 
   </tr> 
    </xsl:for-each> 
    </table> 
  
  
  
  
  
  
  
 
 
 
    <h1 align="center">Highlighted Table</h1> 
   <table border="3" align="center" > 
   <tr> 
    <th>Book id</th> 
    <th>Author</th> 
    <th>Title</th> 
    <th>Genre</th>
     <th>Price</th>
     <th>Publish_date</th>
     <th>Description</th>
   </tr> 
    <xsl:for-each select="catalog/book"> 
        <xsl:if test="author=Gambardella, Matthew"> 
   <tr> 
    <td><xsl:value-of select="book id"/></td> 
    <td><xsl:value-of select="author"/></td> 
    <td><xsl:value-of select="title"/></td> 
    <td><xsl:value-of select="genre"/></td> 
     <td><xsl:value-of select="price"/></td> 
     <td><xsl:value-of select="publish_date"/></td> 
     <td><xsl:value-of select="description"/></td> 
     <xsl:choose>
      <xsl:when test="price > 10">
         <td bgcolor="#ff00ff">
        
<xsl:for-each select="catalog">
         </td>
      </xsl:when>
      <xsl:otherwise>
        
<td><xsl:for-each select="catalog"></td>
      </xsl:otherwise>
      </xsl:choose>
 
   </tr> 
    </xsl:for-each> 
    </table> 
    












 <h1 align="center">Table with Author, Book Title and price</h1> 
   <table border="3" align="center" > 
   <tr>  
    <th>Author</th> 
    <th>Book Title</th>
    <th>Price</th>
   </tr> 
       <xsl:for-each select="catalog/book"> 
   <tr> 
    <td><xsl:value-of select="author"/></td> 
    <td><xsl:value-of select="title"/></td> 
    <td><xsl:value-of select="price"/></td>
   </tr> 
    </xsl:for-each> 
    </table> 
  
  
</body>
</html>
</xsl:template>
</xsl:stylesheet>
