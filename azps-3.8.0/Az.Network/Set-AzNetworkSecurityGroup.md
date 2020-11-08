---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
ms.openlocfilehash: d7a13c27550b206bc1c8d8fa909cb5135df0db55
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066954"
---
# <span data-ttu-id="8c151-101">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8c151-101">Set-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="8c151-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8c151-102">SYNOPSIS</span></span>
<span data-ttu-id="8c151-103">Обновляет сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="8c151-103">Updates a network security group.</span></span>

## <span data-ttu-id="8c151-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8c151-104">SYNTAX</span></span>

```
Set-AzNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c151-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c151-105">DESCRIPTION</span></span>
<span data-ttu-id="8c151-106">Командлет **Set-AzNetworkSecurityGroup** обновляет группу безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="8c151-106">The **Set-AzNetworkSecurityGroup** cmdlet updates a network security group.</span></span>

## <span data-ttu-id="8c151-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8c151-107">EXAMPLES</span></span>

### <span data-ttu-id="8c151-108">Пример 1: обновление существующей группы безопасности сети</span><span class="sxs-lookup"><span data-stu-id="8c151-108">Example 1: Update an existing network security group</span></span>
```
PS C:\>Get-AzNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="8c151-109">Эта команда получает сетевую группу безопасности Azure с именем Nsg1 и добавляет правило сетевой безопасности с именем Rdp-Rule, чтобы разрешить Интернет-трафик для порта 3389 в полученный объект групповой группы безопасности с помощью Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="8c151-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="8c151-110">Эта команда сохраняет измененную группу сетевой безопасности Azure с помощью **Set-AzNetworkSecurityGroup**.</span><span class="sxs-lookup"><span data-stu-id="8c151-110">The command persists the modified Azure network security group using **Set-AzNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="8c151-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8c151-111">PARAMETERS</span></span>

### <span data-ttu-id="8c151-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8c151-112">-AsJob</span></span>
<span data-ttu-id="8c151-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8c151-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8c151-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c151-114">-DefaultProfile</span></span>
<span data-ttu-id="8c151-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8c151-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c151-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8c151-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="8c151-117">Указывает объект сетевой безопасности, представляющий состояние, в котором должна быть установлена сетевая группа безопасности.</span><span class="sxs-lookup"><span data-stu-id="8c151-117">Specifies a network security group object representing the state to which the network security group should be set.</span></span>

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

### <span data-ttu-id="8c151-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c151-118">-Confirm</span></span>
<span data-ttu-id="8c151-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8c151-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c151-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c151-120">-WhatIf</span></span>
<span data-ttu-id="8c151-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8c151-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8c151-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8c151-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c151-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c151-123">CommonParameters</span></span>
<span data-ttu-id="8c151-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8c151-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c151-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c151-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c151-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8c151-126">INPUTS</span></span>

### <span data-ttu-id="8c151-127">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8c151-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="8c151-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c151-128">OUTPUTS</span></span>

### <span data-ttu-id="8c151-129">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8c151-129">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="8c151-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="8c151-130">NOTES</span></span>

## <span data-ttu-id="8c151-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8c151-131">RELATED LINKS</span></span>

[<span data-ttu-id="8c151-132">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8c151-132">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="8c151-133">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8c151-133">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="8c151-134">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8c151-134">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)


