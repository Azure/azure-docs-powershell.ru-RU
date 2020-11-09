---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: fbab2b1b9887fa7a5d509b46909f29eb741959bd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248366"
---
# <span data-ttu-id="2837a-101">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="2837a-101">Get-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="2837a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2837a-102">SYNOPSIS</span></span>
<span data-ttu-id="2837a-103">Возвращает сертификат для проверки подлинности для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="2837a-103">Gets an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="2837a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2837a-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAuthenticationCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2837a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2837a-105">DESCRIPTION</span></span>
<span data-ttu-id="2837a-106">Командлет **Get-AzApplicationGatewayAuthenticationCertificate** получает сертификат проверки подлинности для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="2837a-106">The **Get-AzApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="2837a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2837a-107">EXAMPLES</span></span>

### <span data-ttu-id="2837a-108">Пример 1: получение указанного сертификата для проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="2837a-108">Example 1: Get a specified authentication certificate</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $pool = Get-AzApplicationGatewayBackendAddressPool -Name "pool01" -ApplicationGateway $appgw
```

<span data-ttu-id="2837a-109">Первая команда получает шлюз приложения с именем appGwName и сохраняет его в переменной $appgw.</span><span class="sxs-lookup"><span data-stu-id="2837a-109">The first command gets the application gateway named appGwName and stores it in the $appgw variable.</span></span>
<span data-ttu-id="2837a-110">Вторая команда получает сертификат для проверки подлинности с именем pool01 и сохраняет его в переменной $pool.</span><span class="sxs-lookup"><span data-stu-id="2837a-110">The second command gets the authentication certificate named pool01 and stores it in the $pool variable.</span></span>

## <span data-ttu-id="2837a-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2837a-111">PARAMETERS</span></span>

### <span data-ttu-id="2837a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2837a-112">-ApplicationGateway</span></span>
<span data-ttu-id="2837a-113">Указывает имя шлюза приложений, для которого этот командлет получает сертификат проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="2837a-113">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="2837a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2837a-114">-DefaultProfile</span></span>
<span data-ttu-id="2837a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2837a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2837a-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2837a-116">-Name</span></span>
<span data-ttu-id="2837a-117">Указывает имя сертификата проверки подлинности, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2837a-117">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="2837a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2837a-118">CommonParameters</span></span>
<span data-ttu-id="2837a-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2837a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2837a-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2837a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2837a-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2837a-121">INPUTS</span></span>

### <span data-ttu-id="2837a-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2837a-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2837a-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2837a-123">OUTPUTS</span></span>

### <span data-ttu-id="2837a-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="2837a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="2837a-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="2837a-125">NOTES</span></span>
* <span data-ttu-id="2837a-126">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="2837a-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="2837a-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2837a-127">RELATED LINKS</span></span>

[<span data-ttu-id="2837a-128">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="2837a-128">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="2837a-129">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="2837a-129">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="2837a-130">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="2837a-130">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="2837a-131">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="2837a-131">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)

