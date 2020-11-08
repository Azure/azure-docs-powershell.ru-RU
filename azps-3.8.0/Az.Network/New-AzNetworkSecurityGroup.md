---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A420B3E7-2FE9-4D0B-803E-AC28E5F23C59
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityGroup.md
ms.openlocfilehash: 1ad99522e93587b2f335ae35478aedbc6cc36e88
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066530"
---
# <span data-ttu-id="e148a-101">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e148a-101">New-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="e148a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e148a-102">SYNOPSIS</span></span>
<span data-ttu-id="e148a-103">Создание группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="e148a-103">Creates a network security group.</span></span>

## <span data-ttu-id="e148a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e148a-104">SYNTAX</span></span>

```
New-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -Location <String>
 [-SecurityRules <PSSecurityRule[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e148a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e148a-105">DESCRIPTION</span></span>
<span data-ttu-id="e148a-106">Командлет **New-AzNetworkSecurityGroup** создает группу сетевой безопасности Azure.</span><span class="sxs-lookup"><span data-stu-id="e148a-106">The **New-AzNetworkSecurityGroup** cmdlet creates an Azure network security group.</span></span>

## <span data-ttu-id="e148a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e148a-107">EXAMPLES</span></span>

### <span data-ttu-id="e148a-108">1: создание новой группы безопасности сети</span><span class="sxs-lookup"><span data-stu-id="e148a-108">1: Create a new network security group</span></span>
```
New-AzNetworkSecurityGroup -Name "nsg1" -ResourceGroupName "rg1"  -Location  "westus"
```

<span data-ttu-id="e148a-109">Эта команда создает новую группу сетевой безопасности Azure с именем "nsg1" в группе ресурсов "Rg1" в расположении "westus".</span><span class="sxs-lookup"><span data-stu-id="e148a-109">This command creates a new Azure network security group named "nsg1" in resource group "rg1" in location "westus".</span></span>

### <span data-ttu-id="e148a-110">2. Создание подробной группы безопасности сети</span><span class="sxs-lookup"><span data-stu-id="e148a-110">2: Create a detailed network security group</span></span>
```
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP"
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP"
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80

$nsg = New-AzNetworkSecurityGroup -ResourceGroupName TestRG -Location westus -Name
    "NSG-FrontEnd" -SecurityRules $rule1,$rule2
```

<span data-ttu-id="e148a-111">Шаг: 1 Создайте правило безопасности, разрешающее доступ через Интернет к порту 3389.</span><span class="sxs-lookup"><span data-stu-id="e148a-111">Step:1 Create a security rule allowing access from the Internet to port 3389.</span></span>
<span data-ttu-id="e148a-112">Шаг: 2 Создайте правило безопасности, разрешающее доступ через Интернет к порту 80.</span><span class="sxs-lookup"><span data-stu-id="e148a-112">Step:2 Create a security rule allowing access from the Internet to port 80.</span></span>
<span data-ttu-id="e148a-113">Шаг: 3 Добавьте правила, созданные выше, в новый NSG с именем NSG-переднего плана.</span><span class="sxs-lookup"><span data-stu-id="e148a-113">Step:3 Add the rules created above to a new NSG named NSG-FrontEnd.</span></span>

## <span data-ttu-id="e148a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e148a-114">PARAMETERS</span></span>

### <span data-ttu-id="e148a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e148a-115">-AsJob</span></span>
<span data-ttu-id="e148a-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e148a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e148a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e148a-117">-DefaultProfile</span></span>
<span data-ttu-id="e148a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e148a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e148a-119">-Force</span><span class="sxs-lookup"><span data-stu-id="e148a-119">-Force</span></span>
<span data-ttu-id="e148a-120">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="e148a-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e148a-121">-Location</span><span class="sxs-lookup"><span data-stu-id="e148a-121">-Location</span></span>
<span data-ttu-id="e148a-122">Указывает регион, для которого нужно создать группу безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="e148a-122">Specifies the region for which to create a network security group.</span></span>

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

### <span data-ttu-id="e148a-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e148a-123">-Name</span></span>
<span data-ttu-id="e148a-124">Указывает имя группы безопасности сети, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="e148a-124">Specifies the name of the network security group to create.</span></span>

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

### <span data-ttu-id="e148a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e148a-125">-ResourceGroupName</span></span>
<span data-ttu-id="e148a-126">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e148a-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="e148a-127">Этот командлет создает группу безопасности сети в группе ресурсов, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="e148a-127">This cmdlet creates a network security group in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e148a-128">-SecurityRules</span><span class="sxs-lookup"><span data-stu-id="e148a-128">-SecurityRules</span></span>
<span data-ttu-id="e148a-129">Указывает список объектов правил сетевой безопасности для создания в группе безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="e148a-129">Specifies a list of network security rule objects to create in a network security group.</span></span>

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

### <span data-ttu-id="e148a-130">-Тег</span><span class="sxs-lookup"><span data-stu-id="e148a-130">-Tag</span></span>
<span data-ttu-id="e148a-131">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="e148a-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e148a-132">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="e148a-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e148a-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e148a-133">-Confirm</span></span>
<span data-ttu-id="e148a-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e148a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e148a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e148a-135">-WhatIf</span></span>
<span data-ttu-id="e148a-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e148a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e148a-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e148a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e148a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e148a-138">CommonParameters</span></span>
<span data-ttu-id="e148a-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e148a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e148a-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e148a-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e148a-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e148a-141">INPUTS</span></span>

### <span data-ttu-id="e148a-142">System. String</span><span class="sxs-lookup"><span data-stu-id="e148a-142">System.String</span></span>

### <span data-ttu-id="e148a-143">Microsoft. Azure. Commands. Network. Models. PSSecurityRule []</span><span class="sxs-lookup"><span data-stu-id="e148a-143">Microsoft.Azure.Commands.Network.Models.PSSecurityRule[]</span></span>

### <span data-ttu-id="e148a-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e148a-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e148a-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e148a-145">OUTPUTS</span></span>

### <span data-ttu-id="e148a-146">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e148a-146">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="e148a-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="e148a-147">NOTES</span></span>

## <span data-ttu-id="e148a-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e148a-148">RELATED LINKS</span></span>

[<span data-ttu-id="e148a-149">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e148a-149">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="e148a-150">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e148a-150">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

[<span data-ttu-id="e148a-151">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e148a-151">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)
