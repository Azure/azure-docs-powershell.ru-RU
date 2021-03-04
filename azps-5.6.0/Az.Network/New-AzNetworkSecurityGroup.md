---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A420B3E7-2FE9-4D0B-803E-AC28E5F23C59
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityGroup.md
ms.openlocfilehash: 001023fd313db4228d7fb1f155b5a686f9649277
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953928"
---
# <span data-ttu-id="5c1bb-101">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5c1bb-101">New-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="5c1bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c1bb-102">SYNOPSIS</span></span>
<span data-ttu-id="5c1bb-103">Создает группу безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="5c1bb-103">Creates a network security group.</span></span>

## <span data-ttu-id="5c1bb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5c1bb-104">SYNTAX</span></span>

```
New-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -Location <String>
 [-SecurityRules <PSSecurityRule[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c1bb-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c1bb-105">DESCRIPTION</span></span>
<span data-ttu-id="5c1bb-106">Командлет **New-AzNetworkSecurityGroup** создает группу безопасности сети Azure.</span><span class="sxs-lookup"><span data-stu-id="5c1bb-106">The **New-AzNetworkSecurityGroup** cmdlet creates an Azure network security group.</span></span>

## <span data-ttu-id="5c1bb-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5c1bb-107">EXAMPLES</span></span>

### <span data-ttu-id="5c1bb-108">Пример 1. Создание группы безопасности сети</span><span class="sxs-lookup"><span data-stu-id="5c1bb-108">Example 1: Create a new network security group</span></span>
```powershell
New-AzNetworkSecurityGroup -Name "nsg1" -ResourceGroupName "rg1"  -Location  "westus"
```

<span data-ttu-id="5c1bb-109">Эта команда создает новую группу безопасности сети Azure с именем "nsg1" в группе ресурсов "rg1" в расположении "westus".</span><span class="sxs-lookup"><span data-stu-id="5c1bb-109">This command creates a new Azure network security group named "nsg1" in resource group "rg1" in location "westus".</span></span>

### <span data-ttu-id="5c1bb-110">Пример 2. Создание подробной группы безопасности сети</span><span class="sxs-lookup"><span data-stu-id="5c1bb-110">Example 2: Create a detailed network security group</span></span>
```powershell
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80

$nsg = New-AzNetworkSecurityGroup -ResourceGroupName TestRG -Location westus -Name `
    "NSG-FrontEnd" -SecurityRules $rule1,$rule2
```

<span data-ttu-id="5c1bb-111">Шаг 1. Создание правила безопасности, разрешающих доступ из Интернета к порту 3389.</span><span class="sxs-lookup"><span data-stu-id="5c1bb-111">Step:1 Create a security rule allowing access from the Internet to port 3389.</span></span>
<span data-ttu-id="5c1bb-112">Шаг 2. Создание правила безопасности, разрешающих доступ из Интернета к порту 80.</span><span class="sxs-lookup"><span data-stu-id="5c1bb-112">Step:2 Create a security rule allowing access from the Internet to port 80.</span></span>
<span data-ttu-id="5c1bb-113">Шаг 3. Добавление созданных выше правил в новый NSG-имя NSG-FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="5c1bb-113">Step:3 Add the rules created above to a new NSG named NSG-FrontEnd.</span></span>

## <span data-ttu-id="5c1bb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c1bb-114">PARAMETERS</span></span>

### <span data-ttu-id="5c1bb-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5c1bb-115">-AsJob</span></span>
<span data-ttu-id="5c1bb-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5c1bb-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5c1bb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c1bb-117">-DefaultProfile</span></span>
<span data-ttu-id="5c1bb-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5c1bb-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c1bb-119">-Force</span><span class="sxs-lookup"><span data-stu-id="5c1bb-119">-Force</span></span>
<span data-ttu-id="5c1bb-120">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="5c1bb-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5c1bb-121">-Location</span><span class="sxs-lookup"><span data-stu-id="5c1bb-121">-Location</span></span>
<span data-ttu-id="5c1bb-122">Определяет регион, для которого нужно создать группу безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="5c1bb-122">Specifies the region for which to create a network security group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c1bb-123">-Name</span><span class="sxs-lookup"><span data-stu-id="5c1bb-123">-Name</span></span>
<span data-ttu-id="5c1bb-124">Имя группы безопасности сети, которая будет создаваться.</span><span class="sxs-lookup"><span data-stu-id="5c1bb-124">Specifies the name of the network security group to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c1bb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c1bb-125">-ResourceGroupName</span></span>
<span data-ttu-id="5c1bb-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5c1bb-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="5c1bb-127">Этот cmdlet создает группу безопасности сети в группе ресурсов, заданной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="5c1bb-127">This cmdlet creates a network security group in the resource group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c1bb-128">-SecurityRules</span><span class="sxs-lookup"><span data-stu-id="5c1bb-128">-SecurityRules</span></span>
<span data-ttu-id="5c1bb-129">Список объектов правил безопасности сети, которые нужно создать в группе безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="5c1bb-129">Specifies a list of network security rule objects to create in a network security group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSecurityRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c1bb-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="5c1bb-130">-Tag</span></span>
<span data-ttu-id="5c1bb-131">Пары "ключевое значение" в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="5c1bb-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5c1bb-132">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="5c1bb-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c1bb-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c1bb-133">-Confirm</span></span>
<span data-ttu-id="5c1bb-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="5c1bb-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c1bb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c1bb-135">-WhatIf</span></span>
<span data-ttu-id="5c1bb-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c1bb-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c1bb-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5c1bb-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c1bb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c1bb-138">CommonParameters</span></span>
<span data-ttu-id="5c1bb-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c1bb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c1bb-140">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c1bb-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c1bb-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5c1bb-141">INPUTS</span></span>

### <span data-ttu-id="5c1bb-142">System.String</span><span class="sxs-lookup"><span data-stu-id="5c1bb-142">System.String</span></span>

### <span data-ttu-id="5c1bb-143">Microsoft.Azure.Commands.Network.Models.PSSecurityRule[]</span><span class="sxs-lookup"><span data-stu-id="5c1bb-143">Microsoft.Azure.Commands.Network.Models.PSSecurityRule[]</span></span>

### <span data-ttu-id="5c1bb-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="5c1bb-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5c1bb-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5c1bb-145">OUTPUTS</span></span>

### <span data-ttu-id="5c1bb-146">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5c1bb-146">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="5c1bb-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5c1bb-147">NOTES</span></span>

## <span data-ttu-id="5c1bb-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5c1bb-148">RELATED LINKS</span></span>

[<span data-ttu-id="5c1bb-149">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5c1bb-149">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="5c1bb-150">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5c1bb-150">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

[<span data-ttu-id="5c1bb-151">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5c1bb-151">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)
