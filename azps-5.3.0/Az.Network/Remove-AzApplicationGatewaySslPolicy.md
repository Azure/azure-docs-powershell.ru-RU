---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A308E4DD-49FA-4905-94A7-CEA3AAEC3959
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: ac48531402f474db07ed811b6c2dac2f9a1f233f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98425268"
---
# <span data-ttu-id="6884d-101">Remove-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="6884d-101">Remove-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="6884d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6884d-102">SYNOPSIS</span></span>
<span data-ttu-id="6884d-103">Удаляет политику SSL из шлюза приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="6884d-103">Removes an SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="6884d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6884d-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6884d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6884d-105">DESCRIPTION</span></span>
<span data-ttu-id="6884d-106">Этот Remove-AzApplicationGatewaySslPolicy удаляет SSL-политику из шлюза приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="6884d-106">The Remove-AzApplicationGatewaySslPolicy cmdlet removes SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="6884d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6884d-107">EXAMPLES</span></span>

### <span data-ttu-id="6884d-108">Пример 1. Удаление политики SSL из шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="6884d-108">Example 1: Remove an SSL policy from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGW = Remove-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="6884d-109">Эта команда удаляет политику SSL из шлюза приложения ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="6884d-109">This command removes the SSL policy from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="6884d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6884d-110">PARAMETERS</span></span>

### <span data-ttu-id="6884d-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6884d-111">-ApplicationGateway</span></span>
<span data-ttu-id="6884d-112">Указывает шлюз приложения, из которого этот cmdlet удаляет политику SSL.</span><span class="sxs-lookup"><span data-stu-id="6884d-112">Specifies the application gateway from which this cmdlet removes SSL policy.</span></span>

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

### <span data-ttu-id="6884d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6884d-113">-DefaultProfile</span></span>
<span data-ttu-id="6884d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6884d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6884d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6884d-115">-Force</span></span>
<span data-ttu-id="6884d-116">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="6884d-116">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6884d-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6884d-117">-Confirm</span></span>
<span data-ttu-id="6884d-118">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6884d-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6884d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6884d-119">-WhatIf</span></span>
<span data-ttu-id="6884d-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6884d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6884d-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6884d-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6884d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6884d-122">CommonParameters</span></span>
<span data-ttu-id="6884d-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6884d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6884d-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6884d-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6884d-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6884d-125">INPUTS</span></span>

### <span data-ttu-id="6884d-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6884d-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6884d-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6884d-127">OUTPUTS</span></span>

### <span data-ttu-id="6884d-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6884d-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6884d-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6884d-129">NOTES</span></span>
<span data-ttu-id="6884d-130">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="6884d-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="6884d-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6884d-131">RELATED LINKS</span></span>

[<span data-ttu-id="6884d-132">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="6884d-132">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="6884d-133">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="6884d-133">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="6884d-134">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="6884d-134">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

