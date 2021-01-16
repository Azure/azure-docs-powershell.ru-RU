---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
ms.openlocfilehash: d7a13c27550b206bc1c8d8fa909cb5135df0db55
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402159"
---
# <span data-ttu-id="77aa0-101">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="77aa0-101">Set-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="77aa0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77aa0-102">SYNOPSIS</span></span>
<span data-ttu-id="77aa0-103">Обновляет группу безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="77aa0-103">Updates a network security group.</span></span>

## <span data-ttu-id="77aa0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="77aa0-104">SYNTAX</span></span>

```
Set-AzNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77aa0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="77aa0-105">DESCRIPTION</span></span>
<span data-ttu-id="77aa0-106">Командлет **Set-AzNetworkSecurityGroup** обновляет группу безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="77aa0-106">The **Set-AzNetworkSecurityGroup** cmdlet updates a network security group.</span></span>

## <span data-ttu-id="77aa0-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="77aa0-107">EXAMPLES</span></span>

### <span data-ttu-id="77aa0-108">Пример 1. Обновление существующей группы безопасности сети</span><span class="sxs-lookup"><span data-stu-id="77aa0-108">Example 1: Update an existing network security group</span></span>
```
PS C:\>Get-AzNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="77aa0-109">Эта команда получает группу безопасности сети Azure с именем Nsg1 и добавляет правило безопасности сети Rdp-Rule, чтобы разрешить интернет-трафик при порте 3389 к извлечению объекта группы безопасности сети с помощью Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="77aa0-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="77aa0-110">Команда сохраняет измененную группу безопасности сети Azure с помощью **Set-AzNetworkSecurityGroup.**</span><span class="sxs-lookup"><span data-stu-id="77aa0-110">The command persists the modified Azure network security group using **Set-AzNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="77aa0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77aa0-111">PARAMETERS</span></span>

### <span data-ttu-id="77aa0-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77aa0-112">-AsJob</span></span>
<span data-ttu-id="77aa0-113">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="77aa0-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="77aa0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77aa0-114">-DefaultProfile</span></span>
<span data-ttu-id="77aa0-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="77aa0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77aa0-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="77aa0-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="77aa0-117">Определяет объект группы безопасности сети, представляющий состояние, в котором должна быть установлена группа безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="77aa0-117">Specifies a network security group object representing the state to which the network security group should be set.</span></span>

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

### <span data-ttu-id="77aa0-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="77aa0-118">-Confirm</span></span>
<span data-ttu-id="77aa0-119">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="77aa0-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77aa0-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77aa0-120">-WhatIf</span></span>
<span data-ttu-id="77aa0-121">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77aa0-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="77aa0-122">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="77aa0-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77aa0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77aa0-123">CommonParameters</span></span>
<span data-ttu-id="77aa0-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77aa0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77aa0-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77aa0-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77aa0-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="77aa0-126">INPUTS</span></span>

### <span data-ttu-id="77aa0-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="77aa0-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="77aa0-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="77aa0-128">OUTPUTS</span></span>

### <span data-ttu-id="77aa0-129">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="77aa0-129">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="77aa0-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="77aa0-130">NOTES</span></span>

## <span data-ttu-id="77aa0-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="77aa0-131">RELATED LINKS</span></span>

[<span data-ttu-id="77aa0-132">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="77aa0-132">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="77aa0-133">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="77aa0-133">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="77aa0-134">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="77aa0-134">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

