---
title: HOW TO：使用 X.509 憑證解密 XML 元素
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- System.Security.Cryptography.EncryptedXml class
- XML encryption
- System.Security.Cryptography.X509Certificate2 class
- decryption
- X.509 certificates
- certificates, X.509 certificates
ms.assetid: bd015722-d88d-408d-8ca8-e4e475c441ed
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 72e5f1e72d3ce7ec954d61216bbac2e0e1b5a428
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59301200"
---
# <a name="how-to-decrypt-xml-elements-with-x509-certificates"></a>HOW TO：使用 X.509 憑證解密 XML 元素
您可以使用 <xref:System.Security.Cryptography.Xml> 命名空間中的類別來加密和解密 XML 文件內的項目。  XML 加密是交換或儲存加密 XML 資料的標準方法，不必擔心資料被輕易讀取。  如需 XML 加密標準的詳細資訊，請參閱全球資訊網協會 (W3C) 規格 XML 加密位於 <https://www.w3.org/TR/xmldsig-core/>。  
  
 此範例會解密使用中所述方法加密 XML 項目：[如何：使用 X.509 憑證加密 XML 元素](../../../docs/standard/security/how-to-encrypt-xml-elements-with-x-509-certificates.md)。  找到 <`EncryptedData`> 項目，解密該項目，並再將項目取代原始的純文字 XML 項目。  
  
 此程序的程式碼範例會使用來自目前使用者帳戶本機憑證存放區的 X.509 憑證解密 XML 項目。  此範例會使用<xref:System.Security.Cryptography.Xml.EncryptedXml.DecryptDocument%2A>方法，以自動擷取 X.509 憑證和解密金鑰儲存在工作階段 <`EncryptedKey`> 項目 <`EncryptedData`> 項目。  <xref:System.Security.Cryptography.Xml.EncryptedXml.DecryptDocument%2A> 方法接著會自動使用工作階段金鑰解密 XML 項目。  
  
 這個範例適合多個應用程式需要共用加密資料或應用程式需要在它執行時間之間儲存加密資料的情況。  
  
### <a name="to-decrypt-an-xml-element-with-an-x509-certificate"></a>使用 X.509 憑證解密 XML 項目  
  
1. 藉由從磁碟載入 XML 檔案，建立 <xref:System.Xml.XmlDocument> 物件。  <xref:System.Xml.XmlDocument> 物件會包含要解密的 XML 項目。  
  
     [!code-csharp[HowToDecryptXMLElementX509#2](../../../samples/snippets/csharp/VS_Snippets_CLR/HowToDecryptXMLElementX509/cs/sample.cs#2)]
     [!code-vb[HowToDecryptXMLElementX509#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/HowToDecryptXMLElementX509/vb/sample.vb#2)]  
  
2. 建立新的 <xref:System.Security.Cryptography.Xml.EncryptedXml> 物件，並傳遞 <xref:System.Xml.XmlDocument> 物件給建構函式。  
  
     [!code-csharp[HowToDecryptXMLElementX509#3](../../../samples/snippets/csharp/VS_Snippets_CLR/HowToDecryptXMLElementX509/cs/sample.cs#3)]
     [!code-vb[HowToDecryptXMLElementX509#3](../../../samples/snippets/visualbasic/VS_Snippets_CLR/HowToDecryptXMLElementX509/vb/sample.vb#3)]  
  
3. 使用 <xref:System.Security.Cryptography.Xml.EncryptedXml.DecryptDocument%2A> 方法解密 XML 文件。  
  
     [!code-csharp[HowToDecryptXMLElementX509#4](../../../samples/snippets/csharp/VS_Snippets_CLR/HowToDecryptXMLElementX509/cs/sample.cs#4)]
     [!code-vb[HowToDecryptXMLElementX509#4](../../../samples/snippets/visualbasic/VS_Snippets_CLR/HowToDecryptXMLElementX509/vb/sample.vb#4)]  
  
4. 儲存 <xref:System.Xml.XmlDocument> 物件。  
  
     [!code-csharp[HowToDecryptXMLElementX509#5](../../../samples/snippets/csharp/VS_Snippets_CLR/HowToDecryptXMLElementX509/cs/sample.cs#5)]
     [!code-vb[HowToDecryptXMLElementX509#5](../../../samples/snippets/visualbasic/VS_Snippets_CLR/HowToDecryptXMLElementX509/vb/sample.vb#5)]  
  
## <a name="example"></a>範例  
 這個範例假設名為 `"test.xml"` 的檔案已存在於和編譯程式相同的目錄中。  它同時也假設 `"test.xml"` 包含 `"creditcard"` 元素。  您可以將下列 XML 放入稱為 `test.xml` 的檔案，並使用它搭配此範例。  
  
```xml  
<root>  
    <creditcard>  
        <number>19834209</number>  
        <expiry>02/02/2002</expiry>  
    </creditcard>  
</root>  
```  
  
 [!code-csharp[HowToDecryptXMLElementX509#1](../../../samples/snippets/csharp/VS_Snippets_CLR/HowToDecryptXMLElementX509/cs/sample.cs#1)]
 [!code-vb[HowToDecryptXMLElementX509#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/HowToDecryptXMLElementX509/vb/sample.vb#1)]  
  
## <a name="compiling-the-code"></a>編譯程式碼  
  
-   若要編譯此範例，您需要包含 `System.Security.dll` 的參考。  
  
-   包含下列命名空間：<xref:System.Xml>、<xref:System.Security.Cryptography> 和 <xref:System.Security.Cryptography.Xml>。  
  
## <a name="net-framework-security"></a>.NET Framework 安全性  
 此範例中使用的 X.509 憑證僅供測試使用。  應用程式應該使用由受信任的憑證授權單位所產生的 X.509 憑證，或使用由 Microsoft Windows 憑證伺服器所產生的憑證。  
  
## <a name="see-also"></a>另請參閱

- <xref:System.Security.Cryptography.Xml>
- [如何：使用 X.509 憑證加密 XML 元素](../../../docs/standard/security/how-to-encrypt-xml-elements-with-x-509-certificates.md)
