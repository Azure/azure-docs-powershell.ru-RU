---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: ad318c776662ebaeab3192ca584aa2aad7f2e20a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563888"
---
# <span data-ttu-id="20173-101">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="20173-101">New-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="20173-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="20173-102">SYNOPSIS</span></span>
<span data-ttu-id="20173-103">Создание SSL-сертификата для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="20173-103">Creates an SSL certificate for an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20173-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="20173-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySslCertificate -Name <String> -CertificateFile <String> -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20173-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="20173-105">DESCRIPTION</span></span>
<span data-ttu-id="20173-106">Командлет **New-AzureRmApplicationGatewaySslCertificate** создает SSL-сертификат для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="20173-106">The **New-AzureRmApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="20173-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="20173-107">EXAMPLES</span></span>

### <span data-ttu-id="20173-108">Пример 1: создание SSL-сертификата для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="20173-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\>$Cert = New-AzureRmApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password "Password01"
```

<span data-ttu-id="20173-109">Эта команда создает SSL-сертификат с именем Cert01 для шлюза приложений по умолчанию и сохраняет результат в переменной с именем $Cert.</span><span class="sxs-lookup"><span data-stu-id="20173-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

## <span data-ttu-id="20173-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="20173-110">PARAMETERS</span></span>

### <span data-ttu-id="20173-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="20173-111">-CertificateFile</span></span>
<span data-ttu-id="20173-112">Указывает путь PFX-файла SSL-сертификата, который создает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="20173-112">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20173-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="20173-113">-Name</span></span>
<span data-ttu-id="20173-114">Указывает имя SSL-сертификата, который создает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="20173-114">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20173-115">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="20173-115">-Password</span></span>
<span data-ttu-id="20173-116">Указывает пароль SSL, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="20173-116">Specifies the password of the SSL that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20173-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20173-117">-DefaultProfile</span></span>
<span data-ttu-id="20173-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="20173-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20173-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20173-119">CommonParameters</span></span>
<span data-ttu-id="20173-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="20173-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20173-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20173-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20173-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="20173-122">INPUTS</span></span>

### <span data-ttu-id="20173-123">System. String</span><span class="sxs-lookup"><span data-stu-id="20173-123">System.String</span></span>

## <span data-ttu-id="20173-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="20173-124">OUTPUTS</span></span>

### <span data-ttu-id="20173-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="20173-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="20173-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="20173-126">NOTES</span></span>

## <span data-ttu-id="20173-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="20173-127">RELATED LINKS</span></span>

[<span data-ttu-id="20173-128">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="20173-128">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="20173-129">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="20173-129">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="20173-130">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="20173-130">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="20173-131">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="20173-131">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


