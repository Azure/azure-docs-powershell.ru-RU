---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDdosProtectionPlan.md
ms.openlocfilehash: c565c78e7f95e02d3449a04f0a53f4b84ef7a9f5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244347"
---
# <span data-ttu-id="953e7-101">Remove-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="953e7-101">Remove-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="953e7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="953e7-102">SYNOPSIS</span></span>
<span data-ttu-id="953e7-103">Удаление плана защиты Distributed.</span><span class="sxs-lookup"><span data-stu-id="953e7-103">Removes a DDoS protection plan.</span></span>

## <span data-ttu-id="953e7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="953e7-104">SYNTAX</span></span>

```
Remove-AzDdosProtectionPlan -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="953e7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="953e7-105">DESCRIPTION</span></span>
<span data-ttu-id="953e7-106">Командлет Remove-AzDdosProtectionPlan удаляет план защиты Distributed.</span><span class="sxs-lookup"><span data-stu-id="953e7-106">The Remove-AzDdosProtectionPlan cmdlet removes a DDoS protection plan.</span></span>

## <span data-ttu-id="953e7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="953e7-107">EXAMPLES</span></span>

### <span data-ttu-id="953e7-108">Пример 1: Удаление пустого плана защиты Distributed</span><span class="sxs-lookup"><span data-stu-id="953e7-108">Example 1: Remove an empty DDoS protection plan</span></span>
```
D:\> Remove-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlan
```

<span data-ttu-id="953e7-109">В этом случае мы удалим план защиты Distributed, как указано.</span><span class="sxs-lookup"><span data-stu-id="953e7-109">In this case, we remove a DDoS protection plan as specified.</span></span>

### <span data-ttu-id="953e7-110">Пример 2: Удаление плана защиты Distributed, связанного с виртуальной сетью</span><span class="sxs-lookup"><span data-stu-id="953e7-110">Example 2: Remove a DDoS protection plan associated with a virtual network</span></span>
```
D:\> $vnet = Get-AzVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName
D:\> $vnet.DdosProtectionPlan = $null
D:\> $vnet.EnableDdosProtection = $false
D:\> $vnet | Set-AzVirtualNetwork


Name                   : VnetName
ResourceGroupName      : ResourceGroupName
Location               : westus
Id                     : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName
Etag                   : W/"65947351-747e-4686-aa8b-c40da58f6c8b"
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
                             "Etag": "W/\"65947351-747e-4686-aa8b-c40da58f6c8b\"",
                             "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName/subnets/SubnetName",
                             "AddressPrefix": "10.0.1.0/24",
                             "IpConfigurations": [],
                             "ResourceNavigationLinks": [],
                             "ServiceEndpoints": [],
                             "ProvisioningState": "Succeeded"
                           }
                         ]
VirtualNetworkPeerings : []
EnableDdosProtection   : false
DdosProtectionPlan     : null
EnableVmProtection     : false


D:\> Remove-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlan
```

<span data-ttu-id="953e7-111">Планы защиты Distributed невозможно удалить, если они связаны с виртуальной сетью.</span><span class="sxs-lookup"><span data-stu-id="953e7-111">DDoS protection plans cannot be deleted if they are associated with a virtual network.</span></span> <span data-ttu-id="953e7-112">Для начала необходимо разосоединить оба объекта.</span><span class="sxs-lookup"><span data-stu-id="953e7-112">So the first step is to disassociate both objects.</span></span> <span data-ttu-id="953e7-113">Здесь мы получаем самую обновленную версию виртуальной сети, связанную с планом, и установили для свойства **DdosProtectionPlan** пустое значение и флаг **EnableDdosProtection** (этот флаг не может быть истинным, но не планом).</span><span class="sxs-lookup"><span data-stu-id="953e7-113">Here, we get the most updated version of the virtual network associated with the plan, and we set the property **DdosProtectionPlan** to an empty value and the flag **EnableDdosProtection** (this flag cannot be true without a plan).</span></span>
<span data-ttu-id="953e7-114">Затем мы сохраняем новое состояние, перетаскивая локальную переменную на **Set-AzVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="953e7-114">Then, we persist the new state by piping the local variable into **Set-AzVirtualNetwork**.</span></span> <span data-ttu-id="953e7-115">На этом этапе план больше не связан с виртуальной сетью.</span><span class="sxs-lookup"><span data-stu-id="953e7-115">At this point, the plan is no longer associated with the virtual network.</span></span>
<span data-ttu-id="953e7-116">Если это последнее значение, связанное с планом, мы можем удалить план защиты Distributed с помощью команды Remove-AzDdosProtectionPlan.</span><span class="sxs-lookup"><span data-stu-id="953e7-116">If this is the last one associated with the plan, we can remove the DDoS protection plan by using the command Remove-AzDdosProtectionPlan.</span></span>

## <span data-ttu-id="953e7-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="953e7-117">PARAMETERS</span></span>

### <span data-ttu-id="953e7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="953e7-118">-DefaultProfile</span></span>
<span data-ttu-id="953e7-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="953e7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="953e7-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="953e7-120">-Name</span></span>
<span data-ttu-id="953e7-121">Указывает имя удаляемого плана защиты Distributed.</span><span class="sxs-lookup"><span data-stu-id="953e7-121">Specifies the name of the DDoS protection plan to be removed.</span></span>

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

### <span data-ttu-id="953e7-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="953e7-122">-PassThru</span></span>
<span data-ttu-id="953e7-123">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="953e7-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="953e7-124">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="953e7-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="953e7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="953e7-125">-ResourceGroupName</span></span>
<span data-ttu-id="953e7-126">Указывает группу ресурсов Distributed плана защиты, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="953e7-126">Specifies the resource group of the DDoS protection plan to be removed.</span></span>

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

### <span data-ttu-id="953e7-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="953e7-127">-Confirm</span></span>
<span data-ttu-id="953e7-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="953e7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="953e7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="953e7-129">-WhatIf</span></span>
<span data-ttu-id="953e7-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="953e7-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="953e7-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="953e7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="953e7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="953e7-132">CommonParameters</span></span>
<span data-ttu-id="953e7-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="953e7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="953e7-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="953e7-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="953e7-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="953e7-135">INPUTS</span></span>

### <span data-ttu-id="953e7-136">System. String</span><span class="sxs-lookup"><span data-stu-id="953e7-136">System.String</span></span>

## <span data-ttu-id="953e7-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="953e7-137">OUTPUTS</span></span>

### <span data-ttu-id="953e7-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="953e7-138">System.Boolean</span></span>

## <span data-ttu-id="953e7-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="953e7-139">NOTES</span></span>

## <span data-ttu-id="953e7-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="953e7-140">RELATED LINKS</span></span>

[<span data-ttu-id="953e7-141">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="953e7-141">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)

[<span data-ttu-id="953e7-142">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="953e7-142">Get-AzDdosProtectionPlan</span></span>](./Get-AzDdosProtectionPlan.md)

[<span data-ttu-id="953e7-143">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="953e7-143">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="953e7-144">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="953e7-144">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="953e7-145">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="953e7-145">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)