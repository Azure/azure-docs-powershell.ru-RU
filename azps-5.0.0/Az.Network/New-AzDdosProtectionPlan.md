---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDdosProtectionPlan.md
ms.openlocfilehash: 39d45085c7f53bfeec6e18f38602fca48a3cefa3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248547"
---
# <span data-ttu-id="720b3-101">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="720b3-101">New-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="720b3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="720b3-102">SYNOPSIS</span></span>
<span data-ttu-id="720b3-103">Создание плана защиты Distributed.</span><span class="sxs-lookup"><span data-stu-id="720b3-103">Creates a DDoS protection plan.</span></span>

## <span data-ttu-id="720b3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="720b3-104">SYNTAX</span></span>

```
New-AzDdosProtectionPlan -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="720b3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="720b3-105">DESCRIPTION</span></span>
<span data-ttu-id="720b3-106">Командлет New-AzDdosProtectionPlan создает план защиты Distributed.</span><span class="sxs-lookup"><span data-stu-id="720b3-106">The New-AzDdosProtectionPlan cmdlet creates a DDoS protection plan.</span></span>

## <span data-ttu-id="720b3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="720b3-107">EXAMPLES</span></span>

### <span data-ttu-id="720b3-108">Пример 1: создание и связывание плана защиты Distributed с новой виртуальной сетью</span><span class="sxs-lookup"><span data-stu-id="720b3-108">Example 1: Create and associate a DDoS protection plan with a new virtual network</span></span>
```
D:\> $ddosProtectionPlan = New-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName -Location "West US"
D:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name SubnetName -AddressPrefix 10.0.1.0/24
D:\> $vnet = New-AzVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName -Location "West US" -AddressPrefix 10.0.0.0/16 -DnsServer 8.8.8.8 -Subnet $subnet -EnableDdoSProtection -DdosProtectionPlanId $ddosProtectionPlan.Id
```

<span data-ttu-id="720b3-109">Для начала мы создаем новый план защиты Distributed с помощью команды **New-AzDdosProtectionPlan** .</span><span class="sxs-lookup"><span data-stu-id="720b3-109">First, we create a new DDoS Protection plan with the **New-AzDdosProtectionPlan** command.</span></span>
<span data-ttu-id="720b3-110">Затем мы создаем новую виртуальную сеть с помощью **New-AzVirtualNetwork** и указываем идентификатор вновь созданного плана в параметре **DdosProtectionPlanId**.</span><span class="sxs-lookup"><span data-stu-id="720b3-110">Then, we create a new virtual network with **New-AzVirtualNetwork** and we specify the ID of the newly created plan in the parameter **DdosProtectionPlanId**.</span></span> <span data-ttu-id="720b3-111">В этом случае, поскольку мы связывающи виртуальную сеть с планом, мы можем также указать параметр **EnableDdoSProtection**.</span><span class="sxs-lookup"><span data-stu-id="720b3-111">In this case, since we are associating the virtual network with a plan, we can also specify the parameter **EnableDdoSProtection**.</span></span>

### <span data-ttu-id="720b3-112">Пример 2: создание и связывание плана защиты Distributed с существующим виртуальным сетевым подключением</span><span class="sxs-lookup"><span data-stu-id="720b3-112">Example 2: Create and associate a DDoS protection plan with an existing virtual network</span></span>
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

<span data-ttu-id="720b3-113">Для начала мы создаем новый план защиты Distributed с помощью команды **New-AzDdosProtectionPlan** .</span><span class="sxs-lookup"><span data-stu-id="720b3-113">First, we create a new DDoS Protection plan with the **New-AzDdosProtectionPlan** command.</span></span>
<span data-ttu-id="720b3-114">Во вторых, мы получаем самую новую версию виртуальной сети, которую нужно связать с планом.</span><span class="sxs-lookup"><span data-stu-id="720b3-114">Second, we get the most updated version of the virtual network we want to associate with the plan.</span></span> <span data-ttu-id="720b3-115">Мы обновляем свойство **DdosProtectionPlan** с помощью объекта **PSResourceId** , содержащего ссылку на идентификатор созданного плана.</span><span class="sxs-lookup"><span data-stu-id="720b3-115">We update the property **DdosProtectionPlan** with a **PSResourceId** object containing a reference to the ID of the newly created plan.</span></span> <span data-ttu-id="720b3-116">В этом случае, если мы связываем виртуальную сеть с планом защиты Distributed, мы также можем задать для **EnableDdosProtection** флага значение true.</span><span class="sxs-lookup"><span data-stu-id="720b3-116">In this case, if we associate the virtual network with a DDoS protection plan, we can also set the flag **EnableDdosProtection** to true.</span></span>
<span data-ttu-id="720b3-117">Наконец, мы сохраняем новое состояние, направив локальную переменную в **Set-AzVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="720b3-117">Finally, we persist the new state by piping the local variable into **Set-AzVirtualNetwork**.</span></span>

## <span data-ttu-id="720b3-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="720b3-118">PARAMETERS</span></span>

### <span data-ttu-id="720b3-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="720b3-119">-AsJob</span></span>
<span data-ttu-id="720b3-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="720b3-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="720b3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="720b3-121">-DefaultProfile</span></span>
<span data-ttu-id="720b3-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="720b3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="720b3-123">-Location</span><span class="sxs-lookup"><span data-stu-id="720b3-123">-Location</span></span>
<span data-ttu-id="720b3-124">Указывает расположение плана защиты Distributed, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="720b3-124">Specifies the location of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="720b3-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="720b3-125">-Name</span></span>
<span data-ttu-id="720b3-126">Указывает имя плана защиты Distributed, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="720b3-126">Specifies the name of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="720b3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="720b3-127">-ResourceGroupName</span></span>
<span data-ttu-id="720b3-128">Указывает группу ресурсов для плана защиты Distributed, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="720b3-128">Specifies the resource group of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="720b3-129">-Тег</span><span class="sxs-lookup"><span data-stu-id="720b3-129">-Tag</span></span>
<span data-ttu-id="720b3-130">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="720b3-130">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="720b3-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="720b3-131">-Confirm</span></span>
<span data-ttu-id="720b3-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="720b3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="720b3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="720b3-133">-WhatIf</span></span>
<span data-ttu-id="720b3-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="720b3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="720b3-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="720b3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="720b3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="720b3-136">CommonParameters</span></span>
<span data-ttu-id="720b3-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="720b3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="720b3-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="720b3-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="720b3-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="720b3-139">INPUTS</span></span>

### <span data-ttu-id="720b3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="720b3-140">System.String</span></span>

### <span data-ttu-id="720b3-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="720b3-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="720b3-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="720b3-142">OUTPUTS</span></span>

### <span data-ttu-id="720b3-143">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="720b3-143">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="720b3-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="720b3-144">NOTES</span></span>

## <span data-ttu-id="720b3-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="720b3-145">RELATED LINKS</span></span>

[<span data-ttu-id="720b3-146">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="720b3-146">Get-AzDdosProtectionPlan</span></span>](./Get-AzDdosProtectionPlan.md)

[<span data-ttu-id="720b3-147">Remove-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="720b3-147">Remove-AzDdosProtectionPlan</span></span>](./Remove-AzDdosProtectionPlan.md)

[<span data-ttu-id="720b3-148">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="720b3-148">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="720b3-149">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="720b3-149">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="720b3-150">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="720b3-150">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)