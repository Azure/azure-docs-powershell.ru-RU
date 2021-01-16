---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 02416fdb18f01c9a2af6c091b0be109b479ce45d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98390943"
---
# <span data-ttu-id="aa9c9-101">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="aa9c9-101">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="aa9c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa9c9-102">SYNOPSIS</span></span>
<span data-ttu-id="aa9c9-103">Удаляет сертификат проверки подлинности из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="aa9c9-103">Removes an authentication certificate from an application gateway.</span></span>

## <span data-ttu-id="aa9c9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="aa9c9-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAuthenticationCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa9c9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa9c9-105">DESCRIPTION</span></span>
<span data-ttu-id="aa9c9-106">**Cmdlet Remove-AzApplicationGatewayAuthenticationCertificate** удаляет сертификат проверки подлинности из шлюза приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="aa9c9-106">The **Remove-AzApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="aa9c9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="aa9c9-107">EXAMPLES</span></span>

### <span data-ttu-id="aa9c9-108">Пример 1. Удаление сертификата проверки подлинности из шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="aa9c9-108">Example 1: Remove an authentication certificate from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="aa9c9-109">Первая команда получает шлюз приложения appGwName и сохраняет результат в переменной $appgw.</span><span class="sxs-lookup"><span data-stu-id="aa9c9-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="aa9c9-110">Вторая команда удаляет сертификат проверки подлинности с именем cert01 из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="aa9c9-110">The second command removes the authentication certificate named cert01 from the application gateway.</span></span>
<span data-ttu-id="aa9c9-111">Третья команда обновляет шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="aa9c9-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="aa9c9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa9c9-112">PARAMETERS</span></span>

### <span data-ttu-id="aa9c9-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="aa9c9-113">-ApplicationGateway</span></span>
<span data-ttu-id="aa9c9-114">Указывает имя шлюза приложения, из которого этот cmdlet удаляет сертификат проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="aa9c9-114">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="aa9c9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa9c9-115">-DefaultProfile</span></span>
<span data-ttu-id="aa9c9-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aa9c9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa9c9-117">-Name</span><span class="sxs-lookup"><span data-stu-id="aa9c9-117">-Name</span></span>
<span data-ttu-id="aa9c9-118">Указывает имя сертификата проверки подлинности, который удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa9c9-118">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="aa9c9-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa9c9-119">-Confirm</span></span>
<span data-ttu-id="aa9c9-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa9c9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa9c9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa9c9-121">-WhatIf</span></span>
<span data-ttu-id="aa9c9-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa9c9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa9c9-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="aa9c9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa9c9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa9c9-124">CommonParameters</span></span>
<span data-ttu-id="aa9c9-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa9c9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa9c9-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa9c9-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa9c9-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aa9c9-127">INPUTS</span></span>

### <span data-ttu-id="aa9c9-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="aa9c9-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="aa9c9-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="aa9c9-129">OUTPUTS</span></span>

### <span data-ttu-id="aa9c9-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="aa9c9-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="aa9c9-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="aa9c9-131">NOTES</span></span>
* <span data-ttu-id="aa9c9-132">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="aa9c9-132">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="aa9c9-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aa9c9-133">RELATED LINKS</span></span>

[<span data-ttu-id="aa9c9-134">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="aa9c9-134">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="aa9c9-135">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="aa9c9-135">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="aa9c9-136">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="aa9c9-136">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="aa9c9-137">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="aa9c9-137">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


