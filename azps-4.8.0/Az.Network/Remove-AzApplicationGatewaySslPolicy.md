---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A308E4DD-49FA-4905-94A7-CEA3AAEC3959
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: ac48531402f474db07ed811b6c2dac2f9a1f233f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244109"
---
# <span data-ttu-id="74859-101">Remove-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="74859-101">Remove-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="74859-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="74859-102">SYNOPSIS</span></span>
<span data-ttu-id="74859-103">Удаляет политику SSL из шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="74859-103">Removes an SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="74859-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="74859-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74859-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="74859-105">DESCRIPTION</span></span>
<span data-ttu-id="74859-106">Командлет Remove-AzApplicationGatewaySslPolicy удаляет политику SSL из шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="74859-106">The Remove-AzApplicationGatewaySslPolicy cmdlet removes SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="74859-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="74859-107">EXAMPLES</span></span>

### <span data-ttu-id="74859-108">Пример 1: Удаление политики SSL из шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="74859-108">Example 1: Remove an SSL policy from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGW = Remove-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="74859-109">Эта команда удаляет политику SSL с шлюза приложений с именем ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="74859-109">This command removes the SSL policy from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="74859-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="74859-110">PARAMETERS</span></span>

### <span data-ttu-id="74859-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="74859-111">-ApplicationGateway</span></span>
<span data-ttu-id="74859-112">Указывает шлюз приложений, с которого этот командлет удаляет политику SSL.</span><span class="sxs-lookup"><span data-stu-id="74859-112">Specifies the application gateway from which this cmdlet removes SSL policy.</span></span>

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

### <span data-ttu-id="74859-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74859-113">-DefaultProfile</span></span>
<span data-ttu-id="74859-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="74859-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74859-115">-Force</span><span class="sxs-lookup"><span data-stu-id="74859-115">-Force</span></span>
<span data-ttu-id="74859-116">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="74859-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="74859-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="74859-117">-Confirm</span></span>
<span data-ttu-id="74859-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="74859-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74859-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74859-119">-WhatIf</span></span>
<span data-ttu-id="74859-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="74859-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74859-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="74859-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74859-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74859-122">CommonParameters</span></span>
<span data-ttu-id="74859-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="74859-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74859-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74859-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74859-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="74859-125">INPUTS</span></span>

### <span data-ttu-id="74859-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="74859-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="74859-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="74859-127">OUTPUTS</span></span>

### <span data-ttu-id="74859-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="74859-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="74859-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="74859-129">NOTES</span></span>
<span data-ttu-id="74859-130">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="74859-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="74859-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="74859-131">RELATED LINKS</span></span>

[<span data-ttu-id="74859-132">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="74859-132">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="74859-133">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="74859-133">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="74859-134">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="74859-134">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

