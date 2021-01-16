---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDdosProtectionPlan.md
ms.openlocfilehash: 39d45085c7f53bfeec6e18f38602fca48a3cefa3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421756"
---
# <span data-ttu-id="94796-101">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="94796-101">New-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="94796-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94796-102">SYNOPSIS</span></span>
<span data-ttu-id="94796-103">Создает план защиты DDoS.</span><span class="sxs-lookup"><span data-stu-id="94796-103">Creates a DDoS protection plan.</span></span>

## <span data-ttu-id="94796-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="94796-104">SYNTAX</span></span>

```
New-AzDdosProtectionPlan -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94796-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94796-105">DESCRIPTION</span></span>
<span data-ttu-id="94796-106">С New-AzDdosProtectionPlan создается план защиты DDoS.</span><span class="sxs-lookup"><span data-stu-id="94796-106">The New-AzDdosProtectionPlan cmdlet creates a DDoS protection plan.</span></span>

## <span data-ttu-id="94796-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="94796-107">EXAMPLES</span></span>

### <span data-ttu-id="94796-108">Пример 1. Создание и связывать план защиты DDoS с новой виртуальной сетью</span><span class="sxs-lookup"><span data-stu-id="94796-108">Example 1: Create and associate a DDoS protection plan with a new virtual network</span></span>
```
D:\> $ddosProtectionPlan = New-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName -Location "West US"
D:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name SubnetName -AddressPrefix 10.0.1.0/24
D:\> $vnet = New-AzVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName -Location "West US" -AddressPrefix 10.0.0.0/16 -DnsServer 8.8.8.8 -Subnet $subnet -EnableDdoSProtection -DdosProtectionPlanId $ddosProtectionPlan.Id
```

<span data-ttu-id="94796-109">Во-первых, мы создадим план защиты DDoS с командой **New-AzDdosProtectionPlan.**</span><span class="sxs-lookup"><span data-stu-id="94796-109">First, we create a new DDoS Protection plan with the **New-AzDdosProtectionPlan** command.</span></span>
<span data-ttu-id="94796-110">Затем мы создадим виртуальную сеть с **new-AzVirtualNetwork** и укажите в параметре **DdosProtectionPlanId** ИД созданного плана.</span><span class="sxs-lookup"><span data-stu-id="94796-110">Then, we create a new virtual network with **New-AzVirtualNetwork** and we specify the ID of the newly created plan in the parameter **DdosProtectionPlanId**.</span></span> <span data-ttu-id="94796-111">В этом случае мы также можем указать параметр **EnableDdoSProtection,** так как виртуальная сеть была привязать к плану.</span><span class="sxs-lookup"><span data-stu-id="94796-111">In this case, since we are associating the virtual network with a plan, we can also specify the parameter **EnableDdoSProtection**.</span></span>

### <span data-ttu-id="94796-112">Пример 2. Создание и связывать план защиты DDoS с существующей виртуальной сетью</span><span class="sxs-lookup"><span data-stu-id="94796-112">Example 2: Create and associate a DDoS protection plan with an existing virtual network</span></span>
```
D:\> $ddosProtectionPlan = New-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName -Location "West US"
D:\> $vnet = Get-AzVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName
D:\> $vnet.DdosProtectionPlan = New-Object Microsoft.Azure.Commands.Network.Models.PSResourceId
D:\> $vnet.DdosProtectionPlan.Id = $ddosProtectionPlan.Id
D:\> $vnet.EnableDdosProtection = $true
D:\> $vnet | Set-AzVirtualNetwork


Name                   : VnetName
ResourceGroupName      : ResourceGroupName
Location               : westus
Id                     : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName
Etag                   : W/"fbf41754-3c13-43fd-bb5b-fcc37d5e1cbb"
ResourceGuid           : fcb7bc1e-ee0d-4005-b3f1-feda76e3756c
ProvisioningState      : Succeeded
Tags                   :
AddressSpace           : {
                           "AddressPrefixes": [
                             "10.0.0.0/16"
                           ]
                         }
DhcpOptions            : {
                           "DnsServers": [
                             "8.8.8.8"
                           ]
                         }
Subnets                : [
                           {
                             "Name": "SubnetName",
                             "Etag": "W/\"fbf41754-3c13-43fd-bb5b-fcc37d5e1cbb\"",
                             "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName/subnets/SubnetName",
                             "AddressPrefix": "10.0.1.0/24",
                             "IpConfigurations": [],
                             "ResourceNavigationLinks": [],
                             "ServiceEndpoints": [],
                             "ProvisioningState": "Succeeded"
                           }
                         ]
VirtualNetworkPeerings : []
EnableDdosProtection   : true
DdosProtectionPlan     : {
                           "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName"
                         }
EnableVmProtection     : false
```

<span data-ttu-id="94796-113">Во-первых, мы создадим план защиты DDoS с командой **New-AzDdosProtectionPlan.**</span><span class="sxs-lookup"><span data-stu-id="94796-113">First, we create a new DDoS Protection plan with the **New-AzDdosProtectionPlan** command.</span></span>
<span data-ttu-id="94796-114">Во-вторых, мы получаем наиболее обновленную версию виртуальной сети, которая нам требуется связать с планом.</span><span class="sxs-lookup"><span data-stu-id="94796-114">Second, we get the most updated version of the virtual network we want to associate with the plan.</span></span> <span data-ttu-id="94796-115">Мы обновляем свойство **DdosProtectionPlan** с объектом **PSResourceId,** содержащим ссылку на его ID.</span><span class="sxs-lookup"><span data-stu-id="94796-115">We update the property **DdosProtectionPlan** with a **PSResourceId** object containing a reference to the ID of the newly created plan.</span></span> <span data-ttu-id="94796-116">В этом случае, если связать виртуальную сеть с планом защиты DDoS, можно также установить для **флага EnableDdosProtection** истинное.</span><span class="sxs-lookup"><span data-stu-id="94796-116">In this case, if we associate the virtual network with a DDoS protection plan, we can also set the flag **EnableDdosProtection** to true.</span></span>
<span data-ttu-id="94796-117">Наконец, мы сохраним новое состояние путем перенастройки локальной переменной в **Set-AzVirtualNetwork.**</span><span class="sxs-lookup"><span data-stu-id="94796-117">Finally, we persist the new state by piping the local variable into **Set-AzVirtualNetwork**.</span></span>

## <span data-ttu-id="94796-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94796-118">PARAMETERS</span></span>

### <span data-ttu-id="94796-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94796-119">-AsJob</span></span>
<span data-ttu-id="94796-120">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="94796-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="94796-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94796-121">-DefaultProfile</span></span>
<span data-ttu-id="94796-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="94796-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94796-123">-Location</span><span class="sxs-lookup"><span data-stu-id="94796-123">-Location</span></span>
<span data-ttu-id="94796-124">Определяет расположение создаемого плана защиты DDoS.</span><span class="sxs-lookup"><span data-stu-id="94796-124">Specifies the location of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="94796-125">-Name</span><span class="sxs-lookup"><span data-stu-id="94796-125">-Name</span></span>
<span data-ttu-id="94796-126">Имя плана защиты DDoS, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="94796-126">Specifies the name of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="94796-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94796-127">-ResourceGroupName</span></span>
<span data-ttu-id="94796-128">Группа ресурсов в плане защиты DDoS, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="94796-128">Specifies the resource group of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="94796-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="94796-129">-Tag</span></span>
<span data-ttu-id="94796-130">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="94796-130">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="94796-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94796-131">-Confirm</span></span>
<span data-ttu-id="94796-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94796-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94796-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94796-133">-WhatIf</span></span>
<span data-ttu-id="94796-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94796-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94796-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="94796-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94796-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94796-136">CommonParameters</span></span>
<span data-ttu-id="94796-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94796-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94796-138">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94796-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94796-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="94796-139">INPUTS</span></span>

### <span data-ttu-id="94796-140">System.String</span><span class="sxs-lookup"><span data-stu-id="94796-140">System.String</span></span>

### <span data-ttu-id="94796-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="94796-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="94796-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="94796-142">OUTPUTS</span></span>

### <span data-ttu-id="94796-143">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="94796-143">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="94796-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="94796-144">NOTES</span></span>

## <span data-ttu-id="94796-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94796-145">RELATED LINKS</span></span>

[<span data-ttu-id="94796-146">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="94796-146">Get-AzDdosProtectionPlan</span></span>](./Get-AzDdosProtectionPlan.md)

[<span data-ttu-id="94796-147">Remove-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="94796-147">Remove-AzDdosProtectionPlan</span></span>](./Remove-AzDdosProtectionPlan.md)

[<span data-ttu-id="94796-148">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="94796-148">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="94796-149">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="94796-149">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="94796-150">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="94796-150">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)