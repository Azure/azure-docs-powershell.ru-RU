---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: 3ef8248f90e24da8818a0fa1a8ff6b05970be397
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556579"
---
# <span data-ttu-id="fc0af-101">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fc0af-101">Set-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="fc0af-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fc0af-102">SYNOPSIS</span></span>
<span data-ttu-id="fc0af-103">Задает состояние цели для сетевой группы безопасности.</span><span class="sxs-lookup"><span data-stu-id="fc0af-103">Sets the goal state for a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc0af-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fc0af-104">SYNTAX</span></span>

```
Set-AzureRmNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc0af-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc0af-105">DESCRIPTION</span></span>
<span data-ttu-id="fc0af-106">Командлет **Set-AzureRmNetworkSecurityGroup** задает состояние цели для группы безопасности сети Azure.</span><span class="sxs-lookup"><span data-stu-id="fc0af-106">The **Set-AzureRmNetworkSecurityGroup** cmdlet sets the goal state for an Azure network security group.</span></span>

## <span data-ttu-id="fc0af-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fc0af-107">EXAMPLES</span></span>

### <span data-ttu-id="fc0af-108">Пример 1: Установка состояния цели для сетевой группы безопасности</span><span class="sxs-lookup"><span data-stu-id="fc0af-108">Example 1: Set the goal state for a network security group</span></span>
```
PS C:\>Get-AzureRmNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzureRmNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzureRmNetworkSecurityGroup
```

<span data-ttu-id="fc0af-109">Эта команда получает сетевую группу безопасности Azure с именем Nsg1 и добавляет правило сетевой безопасности с именем Rdp-Rule, чтобы разрешить Интернет-трафик для порта 3389 в полученный объект групповой группы безопасности с помощью Add-AzureRmNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="fc0af-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzureRmNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="fc0af-110">Эта команда сохраняет измененную группу сетевой безопасности Azure с помощью **Set-AzureRmNetworkSecurityGroup**.</span><span class="sxs-lookup"><span data-stu-id="fc0af-110">The command persists the modified Azure network security group using **Set-AzureRmNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="fc0af-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fc0af-111">PARAMETERS</span></span>

### <span data-ttu-id="fc0af-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fc0af-112">-AsJob</span></span>
<span data-ttu-id="fc0af-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="fc0af-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fc0af-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc0af-114">-DefaultProfile</span></span>
<span data-ttu-id="fc0af-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fc0af-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc0af-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fc0af-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="fc0af-117">Объект Network Security Group, представляющий состояние цели, на которое командлет задает сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="fc0af-117">A network security group object representing the goal state to which the cmdlet sets the network security group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc0af-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc0af-118">-Confirm</span></span>
<span data-ttu-id="fc0af-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fc0af-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc0af-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc0af-120">-WhatIf</span></span>
<span data-ttu-id="fc0af-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fc0af-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fc0af-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fc0af-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc0af-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc0af-123">CommonParameters</span></span>
<span data-ttu-id="fc0af-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fc0af-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc0af-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc0af-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc0af-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fc0af-126">INPUTS</span></span>

### <span data-ttu-id="fc0af-127">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fc0af-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>
<span data-ttu-id="fc0af-128">Параметры: NetworkSecurityGroup (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fc0af-128">Parameters: NetworkSecurityGroup (ByValue)</span></span>

## <span data-ttu-id="fc0af-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc0af-129">OUTPUTS</span></span>

### <span data-ttu-id="fc0af-130">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fc0af-130">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="fc0af-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="fc0af-131">NOTES</span></span>

## <span data-ttu-id="fc0af-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fc0af-132">RELATED LINKS</span></span>

[<span data-ttu-id="fc0af-133">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fc0af-133">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="fc0af-134">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fc0af-134">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="fc0af-135">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fc0af-135">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)


