---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 7f5dbd73158e5328ece78b1064a78ff5c4627035
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962803"
---
# <span data-ttu-id="9e2ad-101">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="9e2ad-101">Get-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="9e2ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e2ad-102">SYNOPSIS</span></span>
<span data-ttu-id="9e2ad-103">Получает сертификат проверки подлинности для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="9e2ad-103">Gets an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="9e2ad-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9e2ad-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAuthenticationCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e2ad-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e2ad-105">DESCRIPTION</span></span>
<span data-ttu-id="9e2ad-106">**Cmdlet Get-AzApplicationGatewayAuthenticationCertificate** получает сертификат проверки подлинности для шлюза приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="9e2ad-106">The **Get-AzApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="9e2ad-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9e2ad-107">EXAMPLES</span></span>

### <span data-ttu-id="9e2ad-108">Пример 1. Получить указанный сертификат проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="9e2ad-108">Example 1: Get a specified authentication certificate</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $cert = Get-AzApplicationGatewayAuthenticationCertificate -Name "cert01" -ApplicationGateway $appgw
```

<span data-ttu-id="9e2ad-109">Первая команда получает шлюз приложения appGwName и сохраняет его в переменной $appgw.</span><span class="sxs-lookup"><span data-stu-id="9e2ad-109">The first command gets the application gateway named appGwName and stores it in the $appgw variable.</span></span>
<span data-ttu-id="9e2ad-110">Вторая команда получает сертификат проверки подлинности с именем cert01 и сохраняет его в переменной $cert подлинности.</span><span class="sxs-lookup"><span data-stu-id="9e2ad-110">The second command gets the authentication certificate named cert01 and stores it in the $cert variable.</span></span>

## <span data-ttu-id="9e2ad-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e2ad-111">PARAMETERS</span></span>

### <span data-ttu-id="9e2ad-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9e2ad-112">-ApplicationGateway</span></span>
<span data-ttu-id="9e2ad-113">Указывает имя шлюза приложения, для которого этот cmdlet получает сертификат проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="9e2ad-113">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="9e2ad-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e2ad-114">-DefaultProfile</span></span>
<span data-ttu-id="9e2ad-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9e2ad-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e2ad-116">-Name</span><span class="sxs-lookup"><span data-stu-id="9e2ad-116">-Name</span></span>
<span data-ttu-id="9e2ad-117">Указывает имя сертификата проверки подлинности, который получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e2ad-117">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e2ad-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e2ad-118">CommonParameters</span></span>
<span data-ttu-id="9e2ad-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e2ad-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e2ad-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9e2ad-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e2ad-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9e2ad-121">INPUTS</span></span>

### <span data-ttu-id="9e2ad-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9e2ad-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9e2ad-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9e2ad-123">OUTPUTS</span></span>

### <span data-ttu-id="9e2ad-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="9e2ad-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="9e2ad-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9e2ad-125">NOTES</span></span>
* <span data-ttu-id="9e2ad-126">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="9e2ad-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="9e2ad-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9e2ad-127">RELATED LINKS</span></span>

[<span data-ttu-id="9e2ad-128">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="9e2ad-128">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="9e2ad-129">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="9e2ad-129">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="9e2ad-130">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="9e2ad-130">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="9e2ad-131">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="9e2ad-131">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


