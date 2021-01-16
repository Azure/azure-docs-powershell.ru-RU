---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: fbab2b1b9887fa7a5d509b46909f29eb741959bd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391007"
---
# <span data-ttu-id="69f05-101">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="69f05-101">Get-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="69f05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69f05-102">SYNOPSIS</span></span>
<span data-ttu-id="69f05-103">Получает сертификат проверки подлинности для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="69f05-103">Gets an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="69f05-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="69f05-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAuthenticationCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69f05-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="69f05-105">DESCRIPTION</span></span>
<span data-ttu-id="69f05-106">**Cmdlet Get-AzApplicationGatewayAuthenticationCertificate** получает сертификат проверки подлинности для шлюза приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="69f05-106">The **Get-AzApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="69f05-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="69f05-107">EXAMPLES</span></span>

### <span data-ttu-id="69f05-108">Пример 1. Получить указанный сертификат проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="69f05-108">Example 1: Get a specified authentication certificate</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $pool = Get-AzApplicationGatewayBackendAddressPool -Name "pool01" -ApplicationGateway $appgw
```

<span data-ttu-id="69f05-109">Первая команда получает шлюз приложения appGwName и сохраняет его в переменной $appgw.</span><span class="sxs-lookup"><span data-stu-id="69f05-109">The first command gets the application gateway named appGwName and stores it in the $appgw variable.</span></span>
<span data-ttu-id="69f05-110">Вторая команда получает сертификат проверки подлинности с именем pool01 и сохраняет его в переменной $pool подлинности.</span><span class="sxs-lookup"><span data-stu-id="69f05-110">The second command gets the authentication certificate named pool01 and stores it in the $pool variable.</span></span>

## <span data-ttu-id="69f05-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69f05-111">PARAMETERS</span></span>

### <span data-ttu-id="69f05-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="69f05-112">-ApplicationGateway</span></span>
<span data-ttu-id="69f05-113">Указывает имя шлюза приложения, для которого этот cmdlet получает сертификат проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="69f05-113">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="69f05-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69f05-114">-DefaultProfile</span></span>
<span data-ttu-id="69f05-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="69f05-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69f05-116">-Name</span><span class="sxs-lookup"><span data-stu-id="69f05-116">-Name</span></span>
<span data-ttu-id="69f05-117">Указывает имя сертификата проверки подлинности, который получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69f05-117">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="69f05-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69f05-118">CommonParameters</span></span>
<span data-ttu-id="69f05-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69f05-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69f05-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69f05-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69f05-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="69f05-121">INPUTS</span></span>

### <span data-ttu-id="69f05-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="69f05-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="69f05-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="69f05-123">OUTPUTS</span></span>

### <span data-ttu-id="69f05-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="69f05-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="69f05-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="69f05-125">NOTES</span></span>
* <span data-ttu-id="69f05-126">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="69f05-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="69f05-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="69f05-127">RELATED LINKS</span></span>

[<span data-ttu-id="69f05-128">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="69f05-128">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="69f05-129">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="69f05-129">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="69f05-130">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="69f05-130">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="69f05-131">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="69f05-131">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


