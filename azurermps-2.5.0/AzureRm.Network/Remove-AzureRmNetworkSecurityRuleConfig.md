---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2E43D0D8-EF93-443B-AA8F-58C992026E95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworksecurityruleconfig
schema: 2.0.0
ms.openlocfilehash: 9aed668c977fc1156e2a52723273b1d6d37fba71
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914029"
---
# <span data-ttu-id="1afe6-101">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1afe6-101">Remove-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="1afe6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1afe6-102">SYNOPSIS</span></span>
<span data-ttu-id="1afe6-103">Удаление правила сетевой безопасности из группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="1afe6-103">Removes a network security rule from a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1afe6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1afe6-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1afe6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1afe6-105">DESCRIPTION</span></span>
<span data-ttu-id="1afe6-106">Командлет **Remove-AzureRmNetworkSecurityRuleConfig** удаляет конфигурацию правила безопасности сети из группы безопасности сети Azure.</span><span class="sxs-lookup"><span data-stu-id="1afe6-106">The **Remove-AzureRmNetworkSecurityRuleConfig** cmdlet removes a network security rule configuration from an Azure network security group.</span></span>

## <span data-ttu-id="1afe6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1afe6-107">EXAMPLES</span></span>

### <span data-ttu-id="1afe6-108">Пример 1: Удаление конфигурации правила сетевой безопасности</span><span class="sxs-lookup"><span data-stu-id="1afe6-108">Example 1: Remove a network security rule configuration</span></span>
```
PS C:\>$rule1 = New-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
PS C:\> $nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName "TestRG" -Location "westus" -Name "NSG-FrontEnd" -SecurityRules $rule1
PS C:\> Remove-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg
```

<span data-ttu-id="1afe6-109">Первая команда создает конфигурацию правила сетевой безопасности с именем RDP — правило, а затем сохраняет его в переменной $rule 1.</span><span class="sxs-lookup"><span data-stu-id="1afe6-109">The first command creates a network security rule configuration named rdp-rule, and then stores it in the $rule1 variable.</span></span>

<span data-ttu-id="1afe6-110">Вторая команда создает сетевую группу безопасности, используя правило в $rule 1, а затем сохраняет группу безопасности сети в переменной $nsg.</span><span class="sxs-lookup"><span data-stu-id="1afe6-110">The second command creates a network security group using the rule in $rule1, and then stores the network security group in the $nsg variable.</span></span>

<span data-ttu-id="1afe6-111">Третья команда удаляет конфигурацию правила сетевой безопасности RDP — правило из группы безопасности сети в $nsg.</span><span class="sxs-lookup"><span data-stu-id="1afe6-111">The third command removes the network security rule configuration named rdp-rule from the network security group in $nsg.</span></span>

## <span data-ttu-id="1afe6-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1afe6-112">PARAMETERS</span></span>

### <span data-ttu-id="1afe6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1afe6-113">-DefaultProfile</span></span>
<span data-ttu-id="1afe6-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1afe6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1afe6-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1afe6-115">-Name</span></span>
<span data-ttu-id="1afe6-116">Указывает имя конфигурации правила сетевой безопасности, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="1afe6-116">Specifies the name of the network security rule configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1afe6-117">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1afe6-117">-NetworkSecurityGroup</span></span>
<span data-ttu-id="1afe6-118">Указывает объект **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="1afe6-118">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="1afe6-119">Этот объект включает конфигурацию правила сетевой безопасности для удаления.</span><span class="sxs-lookup"><span data-stu-id="1afe6-119">This object contains the network security rule configuration to remove.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1afe6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1afe6-120">CommonParameters</span></span>
<span data-ttu-id="1afe6-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1afe6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1afe6-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1afe6-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1afe6-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1afe6-123">INPUTS</span></span>

### <span data-ttu-id="1afe6-124">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1afe6-124">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="1afe6-125">Параметр "NetworkSecurityGroup" принимает значение типа "PSNetworkSecurityGroup" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="1afe6-125">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="1afe6-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1afe6-126">OUTPUTS</span></span>

### <span data-ttu-id="1afe6-127">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1afe6-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="1afe6-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="1afe6-128">NOTES</span></span>

## <span data-ttu-id="1afe6-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1afe6-129">RELATED LINKS</span></span>

[<span data-ttu-id="1afe6-130">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1afe6-130">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="1afe6-131">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1afe6-131">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="1afe6-132">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1afe6-132">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="1afe6-133">New-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1afe6-133">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="1afe6-134">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1afe6-134">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)


