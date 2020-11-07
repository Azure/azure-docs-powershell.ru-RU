---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 465567242c0ff13ea695c767cf1dda7f04f54174
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910108"
---
# <span data-ttu-id="bd240-101">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bd240-101">Get-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="bd240-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bd240-102">SYNOPSIS</span></span>
<span data-ttu-id="bd240-103">Возвращает сертификат для проверки подлинности для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="bd240-103">Gets an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="bd240-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bd240-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAuthenticationCertificate [-Name <String>]
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd240-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd240-105">DESCRIPTION</span></span>
<span data-ttu-id="bd240-106">Командлет **Get-AzApplicationGatewayAuthenticationCertificate** получает сертификат проверки подлинности для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="bd240-106">The **Get-AzApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="bd240-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bd240-107">EXAMPLES</span></span>

### <span data-ttu-id="bd240-108">1:</span><span class="sxs-lookup"><span data-stu-id="bd240-108">1:</span></span>
```

```

## <span data-ttu-id="bd240-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bd240-109">PARAMETERS</span></span>

### <span data-ttu-id="bd240-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bd240-110">-ApplicationGateway</span></span>
<span data-ttu-id="bd240-111">Указывает имя шлюза приложений, для которого этот командлет получает сертификат проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="bd240-111">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd240-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd240-112">-DefaultProfile</span></span>
<span data-ttu-id="bd240-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bd240-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd240-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bd240-114">-Name</span></span>
<span data-ttu-id="bd240-115">Указывает имя сертификата проверки подлинности, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="bd240-115">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd240-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd240-116">CommonParameters</span></span>
<span data-ttu-id="bd240-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bd240-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd240-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd240-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd240-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bd240-119">INPUTS</span></span>

### <span data-ttu-id="bd240-120">System. String</span><span class="sxs-lookup"><span data-stu-id="bd240-120">System.String</span></span>

## <span data-ttu-id="bd240-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd240-121">OUTPUTS</span></span>

### <span data-ttu-id="bd240-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bd240-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="bd240-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="bd240-123">NOTES</span></span>
* <span data-ttu-id="bd240-124">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="bd240-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="bd240-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd240-125">RELATED LINKS</span></span>

[<span data-ttu-id="bd240-126">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bd240-126">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="bd240-127">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bd240-127">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="bd240-128">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bd240-128">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="bd240-129">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bd240-129">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


