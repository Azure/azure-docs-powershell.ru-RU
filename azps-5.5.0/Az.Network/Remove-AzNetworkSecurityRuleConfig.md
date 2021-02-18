---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2E43D0D8-EF93-443B-AA8F-58C992026E95
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 7f5d41774af2f5ee74c5d343fa9b143801c139f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100225825"
---
# <span data-ttu-id="513e7-101">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="513e7-101">Remove-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="513e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="513e7-102">SYNOPSIS</span></span>
<span data-ttu-id="513e7-103">Удаляет правило безопасности сети из группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="513e7-103">Removes a network security rule from a network security group.</span></span>

## <span data-ttu-id="513e7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="513e7-104">SYNTAX</span></span>

```
Remove-AzNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="513e7-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="513e7-105">DESCRIPTION</span></span>
<span data-ttu-id="513e7-106">Командлет **Remove-AzNetworkSecurityRuleConfig** удаляет конфигурацию правила безопасности сети из группы безопасности сети Azure.</span><span class="sxs-lookup"><span data-stu-id="513e7-106">The **Remove-AzNetworkSecurityRuleConfig** cmdlet removes a network security rule configuration from an Azure network security group.</span></span>

## <span data-ttu-id="513e7-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="513e7-107">EXAMPLES</span></span>

### <span data-ttu-id="513e7-108">Пример 1. Удаление конфигурации правила безопасности сети</span><span class="sxs-lookup"><span data-stu-id="513e7-108">Example 1: Remove a network security rule configuration</span></span>
```
PS C:\>$rule1 = New-AzNetworkSecurityRuleConfig -Name "rdp-rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
PS C:\> $nsg = New-AzNetworkSecurityGroup -ResourceGroupName "TestRG" -Location "westus" -Name "NSG-FrontEnd" -SecurityRules $rule1
PS C:\> Remove-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg
PS C:\> $nsg | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="513e7-109">Первая команда создает конфигурацию правила безопасности сети с именем rdp-rule, а затем сохраняет ее в переменной $rule 1.</span><span class="sxs-lookup"><span data-stu-id="513e7-109">The first command creates a network security rule configuration named rdp-rule, and then stores it in the $rule1 variable.</span></span>
<span data-ttu-id="513e7-110">Вторая команда создает группу безопасности сети с помощью правила в $rule 1, а затем сохраняет группу безопасности сети в $nsg переменной.</span><span class="sxs-lookup"><span data-stu-id="513e7-110">The second command creates a network security group using the rule in $rule1, and then stores the network security group in the $nsg variable.</span></span>
<span data-ttu-id="513e7-111">Третья команда удаляет конфигурацию правила безопасности сети с именем rdp-rule из группы безопасности сети в $nsg.</span><span class="sxs-lookup"><span data-stu-id="513e7-111">The third command removes the network security rule configuration named rdp-rule from the network security group in $nsg.</span></span>
<span data-ttu-id="513e7-112">Команда, наименовав ее, сохранит изменения.</span><span class="sxs-lookup"><span data-stu-id="513e7-112">The forth command saves the change.</span></span>

## <span data-ttu-id="513e7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="513e7-113">PARAMETERS</span></span>

### <span data-ttu-id="513e7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="513e7-114">-DefaultProfile</span></span>
<span data-ttu-id="513e7-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="513e7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="513e7-116">-Name</span><span class="sxs-lookup"><span data-stu-id="513e7-116">-Name</span></span>
<span data-ttu-id="513e7-117">Указывает имя конфигурации правила безопасности сети, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="513e7-117">Specifies the name of the network security rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="513e7-118">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="513e7-118">-NetworkSecurityGroup</span></span>
<span data-ttu-id="513e7-119">Объект **NetworkSecurityGroup.**</span><span class="sxs-lookup"><span data-stu-id="513e7-119">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="513e7-120">Этот объект содержит конфигурацию правила безопасности сети, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="513e7-120">This object contains the network security rule configuration to remove.</span></span>

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

### <span data-ttu-id="513e7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="513e7-121">CommonParameters</span></span>
<span data-ttu-id="513e7-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="513e7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="513e7-123">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="513e7-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="513e7-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="513e7-124">INPUTS</span></span>

### <span data-ttu-id="513e7-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="513e7-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="513e7-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="513e7-126">OUTPUTS</span></span>

### <span data-ttu-id="513e7-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="513e7-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="513e7-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="513e7-128">NOTES</span></span>

## <span data-ttu-id="513e7-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="513e7-129">RELATED LINKS</span></span>

[<span data-ttu-id="513e7-130">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="513e7-130">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="513e7-131">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="513e7-131">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="513e7-132">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="513e7-132">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="513e7-133">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="513e7-133">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="513e7-134">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="513e7-134">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


