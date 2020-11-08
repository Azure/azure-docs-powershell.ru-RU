---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 02416fdb18f01c9a2af6c091b0be109b479ce45d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234967"
---
# <span data-ttu-id="690e0-101">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="690e0-101">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="690e0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="690e0-102">SYNOPSIS</span></span>
<span data-ttu-id="690e0-103">Удаляет сертификат проверки подлинности из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="690e0-103">Removes an authentication certificate from an application gateway.</span></span>

## <span data-ttu-id="690e0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="690e0-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAuthenticationCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="690e0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="690e0-105">DESCRIPTION</span></span>
<span data-ttu-id="690e0-106">Командлет **Remove-AzApplicationGatewayAuthenticationCertificate** Удаляет сертификат для проверки подлинности из шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="690e0-106">The **Remove-AzApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="690e0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="690e0-107">EXAMPLES</span></span>

### <span data-ttu-id="690e0-108">Пример 1: Удаление сертификата для проверки подлинности из шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="690e0-108">Example 1: Remove an authentication certificate from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="690e0-109">Первая команда получает шлюз приложения с именем appGwName и сохраняет результат в переменной $appgw.</span><span class="sxs-lookup"><span data-stu-id="690e0-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="690e0-110">Вторая команда удаляет сертификат проверки подлинности с именем cert01 из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="690e0-110">The second command removes the authentication certificate named cert01 from the application gateway.</span></span>
<span data-ttu-id="690e0-111">Третья команда обновляет шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="690e0-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="690e0-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="690e0-112">PARAMETERS</span></span>

### <span data-ttu-id="690e0-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="690e0-113">-ApplicationGateway</span></span>
<span data-ttu-id="690e0-114">Указывает имя шлюза приложений, из которого этот командлет удаляет сертификат для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="690e0-114">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="690e0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="690e0-115">-DefaultProfile</span></span>
<span data-ttu-id="690e0-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="690e0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="690e0-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="690e0-117">-Name</span></span>
<span data-ttu-id="690e0-118">Указывает имя сертификата для проверки подлинности, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="690e0-118">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="690e0-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="690e0-119">-Confirm</span></span>
<span data-ttu-id="690e0-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="690e0-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="690e0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="690e0-121">-WhatIf</span></span>
<span data-ttu-id="690e0-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="690e0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="690e0-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="690e0-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="690e0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="690e0-124">CommonParameters</span></span>
<span data-ttu-id="690e0-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="690e0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="690e0-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="690e0-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="690e0-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="690e0-127">INPUTS</span></span>

### <span data-ttu-id="690e0-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="690e0-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="690e0-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="690e0-129">OUTPUTS</span></span>

### <span data-ttu-id="690e0-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="690e0-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="690e0-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="690e0-131">NOTES</span></span>
* <span data-ttu-id="690e0-132">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="690e0-132">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="690e0-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="690e0-133">RELATED LINKS</span></span>

[<span data-ttu-id="690e0-134">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="690e0-134">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="690e0-135">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="690e0-135">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="690e0-136">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="690e0-136">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="690e0-137">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="690e0-137">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


