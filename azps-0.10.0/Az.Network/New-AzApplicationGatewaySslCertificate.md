---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 60d46a3d61f0799618107e9bc0727a3ff31fc337
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909730"
---
# <span data-ttu-id="4ec77-101">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4ec77-101">New-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="4ec77-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4ec77-102">SYNOPSIS</span></span>
<span data-ttu-id="4ec77-103">Создание SSL-сертификата для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="4ec77-103">Creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="4ec77-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4ec77-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslCertificate -Name <String> -CertificateFile <String> -Password <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ec77-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ec77-105">DESCRIPTION</span></span>
<span data-ttu-id="4ec77-106">Командлет **New-AzApplicationGatewaySslCertificate** создает SSL-сертификат для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="4ec77-106">The **New-AzApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="4ec77-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4ec77-107">EXAMPLES</span></span>

### <span data-ttu-id="4ec77-108">Пример 1: создание SSL-сертификата для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="4ec77-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="4ec77-109">Эта команда создает SSL-сертификат с именем Cert01 для шлюза приложений по умолчанию и сохраняет результат в переменной с именем $Cert.</span><span class="sxs-lookup"><span data-stu-id="4ec77-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

## <span data-ttu-id="4ec77-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4ec77-110">PARAMETERS</span></span>

### <span data-ttu-id="4ec77-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="4ec77-111">-CertificateFile</span></span>
<span data-ttu-id="4ec77-112">Указывает путь PFX-файла SSL-сертификата, который создает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="4ec77-112">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec77-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ec77-113">-DefaultProfile</span></span>
<span data-ttu-id="4ec77-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4ec77-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec77-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4ec77-115">-Name</span></span>
<span data-ttu-id="4ec77-116">Указывает имя SSL-сертификата, который создает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="4ec77-116">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec77-117">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="4ec77-117">-Password</span></span>
<span data-ttu-id="4ec77-118">Указывает пароль SSL, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="4ec77-118">Specifies the password of the SSL that this cmdlet creates.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec77-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ec77-119">CommonParameters</span></span>
<span data-ttu-id="4ec77-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4ec77-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ec77-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ec77-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ec77-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4ec77-122">INPUTS</span></span>

### <span data-ttu-id="4ec77-123">System. String</span><span class="sxs-lookup"><span data-stu-id="4ec77-123">System.String</span></span>

## <span data-ttu-id="4ec77-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ec77-124">OUTPUTS</span></span>

### <span data-ttu-id="4ec77-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4ec77-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="4ec77-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="4ec77-126">NOTES</span></span>

## <span data-ttu-id="4ec77-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ec77-127">RELATED LINKS</span></span>

[<span data-ttu-id="4ec77-128">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4ec77-128">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="4ec77-129">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4ec77-129">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="4ec77-130">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4ec77-130">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="4ec77-131">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4ec77-131">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


