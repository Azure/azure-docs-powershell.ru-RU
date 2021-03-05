---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D788B84-0179-4A35-AC35-27C6F5FECB39
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: b8e74c8630dc7f5ba0cd3633314b416ca9a3e39e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986726"
---
# <span data-ttu-id="2606c-101">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2606c-101">Remove-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="2606c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2606c-102">SYNOPSIS</span></span>
<span data-ttu-id="2606c-103">Удаляет SSL-сертификат из шлюза приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="2606c-103">Removes an SSL certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="2606c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2606c-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2606c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2606c-105">DESCRIPTION</span></span>
<span data-ttu-id="2606c-106">При этом из шлюза приложения Azure удаляется **SSL-сертификат Remove-AzApplicationGateWaySslCertificate.**</span><span class="sxs-lookup"><span data-stu-id="2606c-106">The **Remove-AzApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="2606c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2606c-107">EXAMPLES</span></span>

### <span data-ttu-id="2606c-108">Пример 1. Удаление SSL-сертификата из шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="2606c-108">Example 1: Remove an SSL certificate from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert02"
```

<span data-ttu-id="2606c-109">Первая команда получает шлюз приложения ApplicationGateway01 и сохраняет результат в переменной с $AppGW.</span><span class="sxs-lookup"><span data-stu-id="2606c-109">The first command gets the application gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="2606c-110">Вторая команда удаляет SSL-сертификат с именем Cert02 из шлюза приложения, $AppGW переменной.</span><span class="sxs-lookup"><span data-stu-id="2606c-110">The second command removes the SSL certificate named Cert02 from the application gateway stored in the $AppGW variable.</span></span>

## <span data-ttu-id="2606c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2606c-111">PARAMETERS</span></span>

### <span data-ttu-id="2606c-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2606c-112">-ApplicationGateway</span></span>
<span data-ttu-id="2606c-113">Указывает шлюз приложения, из которого этот cmdlet удаляет SSL-сертификат.</span><span class="sxs-lookup"><span data-stu-id="2606c-113">Specifies the application gateway from which this cmdlet removes an SSL certificate.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2606c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2606c-114">-DefaultProfile</span></span>
<span data-ttu-id="2606c-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2606c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2606c-116">-Name</span><span class="sxs-lookup"><span data-stu-id="2606c-116">-Name</span></span>
<span data-ttu-id="2606c-117">Указывает имя SSL-сертификата, который удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2606c-117">Specifies the name of an SSL certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2606c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2606c-118">CommonParameters</span></span>
<span data-ttu-id="2606c-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2606c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2606c-120">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2606c-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2606c-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2606c-121">INPUTS</span></span>

### <span data-ttu-id="2606c-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2606c-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2606c-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2606c-123">OUTPUTS</span></span>

### <span data-ttu-id="2606c-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2606c-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2606c-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2606c-125">NOTES</span></span>

## <span data-ttu-id="2606c-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2606c-126">RELATED LINKS</span></span>

[<span data-ttu-id="2606c-127">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2606c-127">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="2606c-128">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2606c-128">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="2606c-129">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2606c-129">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="2606c-130">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2606c-130">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


