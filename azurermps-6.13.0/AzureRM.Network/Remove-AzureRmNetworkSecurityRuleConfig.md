---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2E43D0D8-EF93-443B-AA8F-58C992026E95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: d6ca2ac1e091e3576af51ba8f1a2f50676994ce1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568467"
---
# <span data-ttu-id="e49d3-101">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e49d3-101">Remove-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="e49d3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e49d3-102">SYNOPSIS</span></span>
<span data-ttu-id="e49d3-103">Удаление правила сетевой безопасности из группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="e49d3-103">Removes a network security rule from a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e49d3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e49d3-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e49d3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e49d3-105">DESCRIPTION</span></span>
<span data-ttu-id="e49d3-106">Командлет **Remove-AzureRmNetworkSecurityRuleConfig** удаляет конфигурацию правила безопасности сети из группы безопасности сети Azure.</span><span class="sxs-lookup"><span data-stu-id="e49d3-106">The **Remove-AzureRmNetworkSecurityRuleConfig** cmdlet removes a network security rule configuration from an Azure network security group.</span></span>

## <span data-ttu-id="e49d3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e49d3-107">EXAMPLES</span></span>

### <span data-ttu-id="e49d3-108">Пример 1: Удаление конфигурации правила сетевой безопасности</span><span class="sxs-lookup"><span data-stu-id="e49d3-108">Example 1: Remove a network security rule configuration</span></span>
```
PS C:\>$rule1 = New-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
PS C:\> $nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName "TestRG" -Location "westus" -Name "NSG-FrontEnd" -SecurityRules $rule1
PS C:\> Remove-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg
```

<span data-ttu-id="e49d3-109">Первая команда создает конфигурацию правила сетевой безопасности с именем RDP — правило, а затем сохраняет его в переменной $rule 1.</span><span class="sxs-lookup"><span data-stu-id="e49d3-109">The first command creates a network security rule configuration named rdp-rule, and then stores it in the $rule1 variable.</span></span>
<span data-ttu-id="e49d3-110">Вторая команда создает сетевую группу безопасности, используя правило в $rule 1, а затем сохраняет группу безопасности сети в переменной $nsg.</span><span class="sxs-lookup"><span data-stu-id="e49d3-110">The second command creates a network security group using the rule in $rule1, and then stores the network security group in the $nsg variable.</span></span>
<span data-ttu-id="e49d3-111">Третья команда удаляет конфигурацию правила сетевой безопасности RDP — правило из группы безопасности сети в $nsg.</span><span class="sxs-lookup"><span data-stu-id="e49d3-111">The third command removes the network security rule configuration named rdp-rule from the network security group in $nsg.</span></span>

## <span data-ttu-id="e49d3-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e49d3-112">PARAMETERS</span></span>

### <span data-ttu-id="e49d3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e49d3-113">-DefaultProfile</span></span>
<span data-ttu-id="e49d3-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e49d3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e49d3-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e49d3-115">-Name</span></span>
<span data-ttu-id="e49d3-116">Указывает имя конфигурации правила сетевой безопасности, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e49d3-116">Specifies the name of the network security rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e49d3-117">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e49d3-117">-NetworkSecurityGroup</span></span>
<span data-ttu-id="e49d3-118">Указывает объект **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="e49d3-118">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="e49d3-119">Этот объект включает конфигурацию правила сетевой безопасности для удаления.</span><span class="sxs-lookup"><span data-stu-id="e49d3-119">This object contains the network security rule configuration to remove.</span></span>

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

### <span data-ttu-id="e49d3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e49d3-120">CommonParameters</span></span>
<span data-ttu-id="e49d3-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e49d3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e49d3-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e49d3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e49d3-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e49d3-123">INPUTS</span></span>

### <span data-ttu-id="e49d3-124">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e49d3-124">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>
<span data-ttu-id="e49d3-125">Параметры: NetworkSecurityGroup (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e49d3-125">Parameters: NetworkSecurityGroup (ByValue)</span></span>

## <span data-ttu-id="e49d3-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e49d3-126">OUTPUTS</span></span>

### <span data-ttu-id="e49d3-127">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e49d3-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="e49d3-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="e49d3-128">NOTES</span></span>

## <span data-ttu-id="e49d3-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e49d3-129">RELATED LINKS</span></span>

[<span data-ttu-id="e49d3-130">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e49d3-130">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="e49d3-131">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e49d3-131">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="e49d3-132">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e49d3-132">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="e49d3-133">New-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e49d3-133">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="e49d3-134">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e49d3-134">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)


