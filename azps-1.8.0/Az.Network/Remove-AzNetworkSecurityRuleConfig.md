---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2E43D0D8-EF93-443B-AA8F-58C992026E95
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 1252c452cc6ad7996a8dcddcb915da251b0b5039
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730139"
---
# <span data-ttu-id="5b48e-101">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5b48e-101">Remove-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="5b48e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5b48e-102">SYNOPSIS</span></span>
<span data-ttu-id="5b48e-103">Удаление правила сетевой безопасности из группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="5b48e-103">Removes a network security rule from a network security group.</span></span>

## <span data-ttu-id="5b48e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5b48e-104">SYNTAX</span></span>

```
Remove-AzNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b48e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b48e-105">DESCRIPTION</span></span>
<span data-ttu-id="5b48e-106">Командлет **Remove-AzNetworkSecurityRuleConfig** удаляет конфигурацию правила безопасности сети из группы безопасности сети Azure.</span><span class="sxs-lookup"><span data-stu-id="5b48e-106">The **Remove-AzNetworkSecurityRuleConfig** cmdlet removes a network security rule configuration from an Azure network security group.</span></span>

## <span data-ttu-id="5b48e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5b48e-107">EXAMPLES</span></span>

### <span data-ttu-id="5b48e-108">Пример 1: Удаление конфигурации правила сетевой безопасности</span><span class="sxs-lookup"><span data-stu-id="5b48e-108">Example 1: Remove a network security rule configuration</span></span>
```
PS C:\>$rule1 = New-AzNetworkSecurityRuleConfig -Name "rdp-rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
PS C:\> $nsg = New-AzNetworkSecurityGroup -ResourceGroupName "TestRG" -Location "westus" -Name "NSG-FrontEnd" -SecurityRules $rule1
PS C:\> Remove-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg
PS C:\> $nsg | Set-AzureRmNetworkSecurityGroup
```

<span data-ttu-id="5b48e-109">Первая команда создает конфигурацию правила сетевой безопасности с именем RDP — правило, а затем сохраняет его в переменной $rule 1.</span><span class="sxs-lookup"><span data-stu-id="5b48e-109">The first command creates a network security rule configuration named rdp-rule, and then stores it in the $rule1 variable.</span></span>
<span data-ttu-id="5b48e-110">Вторая команда создает сетевую группу безопасности, используя правило в $rule 1, а затем сохраняет группу безопасности сети в переменной $nsg.</span><span class="sxs-lookup"><span data-stu-id="5b48e-110">The second command creates a network security group using the rule in $rule1, and then stores the network security group in the $nsg variable.</span></span>
<span data-ttu-id="5b48e-111">Третья команда удаляет конфигурацию правила сетевой безопасности RDP — правило из группы безопасности сети в $nsg.</span><span class="sxs-lookup"><span data-stu-id="5b48e-111">The third command removes the network security rule configuration named rdp-rule from the network security group in $nsg.</span></span>
<span data-ttu-id="5b48e-112">Команда "вперед" сохраняет изменения.</span><span class="sxs-lookup"><span data-stu-id="5b48e-112">The forth command saves the change.</span></span>

## <span data-ttu-id="5b48e-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5b48e-113">PARAMETERS</span></span>

### <span data-ttu-id="5b48e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b48e-114">-DefaultProfile</span></span>
<span data-ttu-id="5b48e-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5b48e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b48e-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5b48e-116">-Name</span></span>
<span data-ttu-id="5b48e-117">Указывает имя конфигурации правила сетевой безопасности, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5b48e-117">Specifies the name of the network security rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5b48e-118">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5b48e-118">-NetworkSecurityGroup</span></span>
<span data-ttu-id="5b48e-119">Указывает объект **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="5b48e-119">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="5b48e-120">Этот объект включает конфигурацию правила сетевой безопасности для удаления.</span><span class="sxs-lookup"><span data-stu-id="5b48e-120">This object contains the network security rule configuration to remove.</span></span>

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

### <span data-ttu-id="5b48e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b48e-121">CommonParameters</span></span>
<span data-ttu-id="5b48e-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5b48e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b48e-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b48e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b48e-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5b48e-124">INPUTS</span></span>

### <span data-ttu-id="5b48e-125">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5b48e-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="5b48e-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b48e-126">OUTPUTS</span></span>

### <span data-ttu-id="5b48e-127">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5b48e-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="5b48e-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="5b48e-128">NOTES</span></span>

## <span data-ttu-id="5b48e-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5b48e-129">RELATED LINKS</span></span>

[<span data-ttu-id="5b48e-130">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5b48e-130">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="5b48e-131">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5b48e-131">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="5b48e-132">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5b48e-132">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="5b48e-133">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5b48e-133">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="5b48e-134">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5b48e-134">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


