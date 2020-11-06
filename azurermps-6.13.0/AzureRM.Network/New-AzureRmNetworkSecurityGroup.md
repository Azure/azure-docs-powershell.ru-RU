---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A420B3E7-2FE9-4D0B-803E-AC28E5F23C59
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: 1ffcad92a50cc332fdcab71337112b8d0c436388
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565854"
---
# <span data-ttu-id="19c23-101">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="19c23-101">New-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="19c23-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="19c23-102">SYNOPSIS</span></span>
<span data-ttu-id="19c23-103">Создание группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="19c23-103">Creates a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19c23-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="19c23-104">SYNTAX</span></span>

```
New-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -Location <String>
 [-SecurityRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSecurityRule]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="19c23-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19c23-105">DESCRIPTION</span></span>
<span data-ttu-id="19c23-106">Командлет **New-AzureRmNetworkSecurityGroup** создает группу сетевой безопасности Azure.</span><span class="sxs-lookup"><span data-stu-id="19c23-106">The **New-AzureRmNetworkSecurityGroup** cmdlet creates an Azure network security group.</span></span>

## <span data-ttu-id="19c23-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="19c23-107">EXAMPLES</span></span>

### <span data-ttu-id="19c23-108">1: создание новой группы безопасности сети</span><span class="sxs-lookup"><span data-stu-id="19c23-108">1: Create a new network security group</span></span>
```
New-AzureRmNetworkSecurityGroup -Name "nsg1" -ResourceGroupName "rg1"  -Location  "westus"
```

<span data-ttu-id="19c23-109">Эта команда создает новую группу сетевой безопасности Azure с именем "nsg1" в группе ресурсов "Rg1" в расположении "westus".</span><span class="sxs-lookup"><span data-stu-id="19c23-109">This command creates a new Azure network security group named "nsg1" in resource group "rg1" in location "westus".</span></span>

### <span data-ttu-id="19c23-110">2. Создание подробной группы безопасности сети</span><span class="sxs-lookup"><span data-stu-id="19c23-110">2: Create a detailed network security group</span></span>
```
$rule1 = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP"
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$rule2 = New-AzureRmNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP"
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80

$nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName TestRG -Location westus -Name
    "NSG-FrontEnd" -SecurityRules $rule1,$rule2
```

<span data-ttu-id="19c23-111">Шаг: 1 Создайте правило безопасности, разрешающее доступ через Интернет к порту 3389.</span><span class="sxs-lookup"><span data-stu-id="19c23-111">Step:1 Create a security rule allowing access from the Internet to port 3389.</span></span>
<span data-ttu-id="19c23-112">Шаг: 2 Создайте правило безопасности, разрешающее доступ через Интернет к порту 80.</span><span class="sxs-lookup"><span data-stu-id="19c23-112">Step:2 Create a security rule allowing access from the Internet to port 80.</span></span>
<span data-ttu-id="19c23-113">Шаг: 3 Добавьте правила, созданные выше, в новый NSG с именем NSG-переднего плана.</span><span class="sxs-lookup"><span data-stu-id="19c23-113">Step:3 Add the rules created above to a new NSG named NSG-FrontEnd.</span></span>

## <span data-ttu-id="19c23-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="19c23-114">PARAMETERS</span></span>

### <span data-ttu-id="19c23-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="19c23-115">-AsJob</span></span>
<span data-ttu-id="19c23-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="19c23-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="19c23-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19c23-117">-DefaultProfile</span></span>
<span data-ttu-id="19c23-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="19c23-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19c23-119">-Force</span><span class="sxs-lookup"><span data-stu-id="19c23-119">-Force</span></span>
<span data-ttu-id="19c23-120">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="19c23-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="19c23-121">-Location</span><span class="sxs-lookup"><span data-stu-id="19c23-121">-Location</span></span>
<span data-ttu-id="19c23-122">Указывает регион, для которого нужно создать группу безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="19c23-122">Specifies the region for which to create a network security group.</span></span>

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

### <span data-ttu-id="19c23-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="19c23-123">-Name</span></span>
<span data-ttu-id="19c23-124">Указывает имя группы безопасности сети, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="19c23-124">Specifies the name of the network security group to create.</span></span>

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

### <span data-ttu-id="19c23-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19c23-125">-ResourceGroupName</span></span>
<span data-ttu-id="19c23-126">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="19c23-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="19c23-127">Этот командлет создает группу безопасности сети в группе ресурсов, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="19c23-127">This cmdlet creates a network security group in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="19c23-128">-SecurityRules</span><span class="sxs-lookup"><span data-stu-id="19c23-128">-SecurityRules</span></span>
<span data-ttu-id="19c23-129">Указывает список объектов правил сетевой безопасности для создания в группе безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="19c23-129">Specifies a list of network security rule objects to create in a network security group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSecurityRule]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19c23-130">-Тег</span><span class="sxs-lookup"><span data-stu-id="19c23-130">-Tag</span></span>
<span data-ttu-id="19c23-131">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="19c23-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="19c23-132">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="19c23-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="19c23-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19c23-133">-Confirm</span></span>
<span data-ttu-id="19c23-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="19c23-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19c23-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19c23-135">-WhatIf</span></span>
<span data-ttu-id="19c23-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="19c23-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19c23-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="19c23-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19c23-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19c23-138">CommonParameters</span></span>
<span data-ttu-id="19c23-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="19c23-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19c23-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19c23-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19c23-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="19c23-141">INPUTS</span></span>

### <span data-ttu-id="19c23-142">System. String</span><span class="sxs-lookup"><span data-stu-id="19c23-142">System.String</span></span>

### <span data-ttu-id="19c23-143">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSSecurityRule, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="19c23-143">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSSecurityRule, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="19c23-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="19c23-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="19c23-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="19c23-145">OUTPUTS</span></span>

### <span data-ttu-id="19c23-146">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="19c23-146">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="19c23-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="19c23-147">NOTES</span></span>

## <span data-ttu-id="19c23-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19c23-148">RELATED LINKS</span></span>

[<span data-ttu-id="19c23-149">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="19c23-149">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="19c23-150">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="19c23-150">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="19c23-151">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="19c23-151">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)
