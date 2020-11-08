---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/new-azsippool
schema: 2.0.0
ms.openlocfilehash: 2b04c5c1eb4d0a2b79543bf81bbfc02d1f0fb4ad
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076884"
---
# <span data-ttu-id="b7025-101">New-AzsIPPool</span><span class="sxs-lookup"><span data-stu-id="b7025-101">New-AzsIPPool</span></span>

## <span data-ttu-id="b7025-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b7025-102">SYNOPSIS</span></span>
<span data-ttu-id="b7025-103">Создание пула IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="b7025-103">Create an IP pool.</span></span>
<span data-ttu-id="b7025-104">После создания пул IP-адресов не может быть удален.</span><span class="sxs-lookup"><span data-stu-id="b7025-104">Once created an IP pool cannot be deleted.</span></span>

## <span data-ttu-id="b7025-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b7025-105">SYNTAX</span></span>

### <span data-ttu-id="b7025-106">CreateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b7025-106">CreateExpanded (Default)</span></span>
```
New-AzsIPPool -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-AddressPrefix <String>] [-EndIPAddress <String>]
 [-NumberOfAllocatedIPAddress <Int64>] [-NumberOfIPAddress <Int64>] [-NumberOfIPAddressesInTransition <Int64>]
 [-StartIPAddress <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b7025-107">Заново</span><span class="sxs-lookup"><span data-stu-id="b7025-107">Create</span></span>
```
New-AzsIPPool -Name <String> -Pool <IIPPool> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="b7025-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7025-108">DESCRIPTION</span></span>
<span data-ttu-id="b7025-109">Создание пула IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="b7025-109">Create an IP pool.</span></span>
<span data-ttu-id="b7025-110">После создания пул IP-адресов не может быть удален.</span><span class="sxs-lookup"><span data-stu-id="b7025-110">Once created an IP pool cannot be deleted.</span></span>

## <span data-ttu-id="b7025-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b7025-111">EXAMPLES</span></span>

### <span data-ttu-id="b7025-112">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="b7025-112">Example 1:</span></span>
```powershell
PS C:\> New-AzsIpPool -Name IpPool4 -StartIpAddress ***.***.***.*** -EndIpAddress ***.***.***.*** -AddressPrefix ***.***.***.***/24

```

<span data-ttu-id="b7025-113">Создание нового пула IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="b7025-113">Create a new IP pool.</span></span>



## <span data-ttu-id="b7025-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b7025-114">PARAMETERS</span></span>

### <span data-ttu-id="b7025-115">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b7025-115">-AddressPrefix</span></span>
<span data-ttu-id="b7025-116">Префикс адреса.</span><span class="sxs-lookup"><span data-stu-id="b7025-116">The address prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b7025-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7025-117">-AsJob</span></span>
<span data-ttu-id="b7025-118">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="b7025-118">Run the command as a job</span></span>

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

### <span data-ttu-id="b7025-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7025-119">-DefaultProfile</span></span>
<span data-ttu-id="b7025-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b7025-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b7025-121">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="b7025-121">-EndIPAddress</span></span>
<span data-ttu-id="b7025-122">Конечный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="b7025-122">The ending IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b7025-123">-Location</span><span class="sxs-lookup"><span data-stu-id="b7025-123">-Location</span></span>
<span data-ttu-id="b7025-124">Область, в которой расположен ресурс.</span><span class="sxs-lookup"><span data-stu-id="b7025-124">The region where the resource is located.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b7025-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b7025-125">-Name</span></span>
<span data-ttu-id="b7025-126">Имя пула IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="b7025-126">IP pool name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b7025-127">-Wait</span><span class="sxs-lookup"><span data-stu-id="b7025-127">-NoWait</span></span>
<span data-ttu-id="b7025-128">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="b7025-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b7025-129">-NumberOfAllocatedIPAddress</span><span class="sxs-lookup"><span data-stu-id="b7025-129">-NumberOfAllocatedIPAddress</span></span>
<span data-ttu-id="b7025-130">Количество выделенных в данный момент IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="b7025-130">The number of currently allocated IP addresses.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b7025-131">-NumberOfIPAddress</span><span class="sxs-lookup"><span data-stu-id="b7025-131">-NumberOfIPAddress</span></span>
<span data-ttu-id="b7025-132">Общее количество IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="b7025-132">The total number of IP addresses.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b7025-133">-NumberOfIPAddressesInTransition</span><span class="sxs-lookup"><span data-stu-id="b7025-133">-NumberOfIPAddressesInTransition</span></span>
<span data-ttu-id="b7025-134">Текущее число IP-адресов в переходе.</span><span class="sxs-lookup"><span data-stu-id="b7025-134">The current number of IP addresses in transition.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b7025-135">-Пул</span><span class="sxs-lookup"><span data-stu-id="b7025-135">-Pool</span></span>
<span data-ttu-id="b7025-136">Этот ресурс определяет диапазон IP-адресов, на основе которых будут выделяться адреса для узлов в подсети.</span><span class="sxs-lookup"><span data-stu-id="b7025-136">This resource defines the range of IP addresses from which addresses are allocated for nodes within a subnet.</span></span>
<span data-ttu-id="b7025-137">Для конструирования щелкните раздел заметок о свойствах пула и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="b7025-137">To construct, see NOTES section for POOL properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IIPPool
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="b7025-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7025-138">-ResourceGroupName</span></span>
<span data-ttu-id="b7025-139">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b7025-139">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b7025-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="b7025-140">-StartIPAddress</span></span>
<span data-ttu-id="b7025-141">Начальный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="b7025-141">The starting IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b7025-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b7025-142">-SubscriptionId</span></span>
<span data-ttu-id="b7025-143">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b7025-143">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b7025-144">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="b7025-144">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b7025-145">-Тег</span><span class="sxs-lookup"><span data-stu-id="b7025-145">-Tag</span></span>
<span data-ttu-id="b7025-146">Список пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="b7025-146">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b7025-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7025-147">-Confirm</span></span>
<span data-ttu-id="b7025-148">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b7025-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7025-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7025-149">-WhatIf</span></span>
<span data-ttu-id="b7025-150">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b7025-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7025-151">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b7025-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7025-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7025-152">CommonParameters</span></span>
<span data-ttu-id="b7025-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b7025-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7025-154">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7025-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7025-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b7025-155">INPUTS</span></span>

### <span data-ttu-id="b7025-156">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. Api20160501. IIPPool</span><span class="sxs-lookup"><span data-stu-id="b7025-156">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IIPPool</span></span>

## <span data-ttu-id="b7025-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7025-157">OUTPUTS</span></span>

### <span data-ttu-id="b7025-158">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. Api20160501. IIPPool</span><span class="sxs-lookup"><span data-stu-id="b7025-158">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IIPPool</span></span>



## <span data-ttu-id="b7025-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="b7025-159">NOTES</span></span>

<span data-ttu-id="b7025-160">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b7025-160">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b7025-161">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b7025-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b7025-162">ПУЛ <IIPPool> : этот ресурс определяет диапазон IP-адресов, на основе которых будут выделяться адреса для узлов в подсети.</span><span class="sxs-lookup"><span data-stu-id="b7025-162">POOL <IIPPool>: This resource defines the range of IP addresses from which addresses are allocated for nodes within a subnet.</span></span>
  - <span data-ttu-id="b7025-163">`[Location <String>]`: Область, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="b7025-163">`[Location <String>]`: The region where the resource is located.</span></span>
  - <span data-ttu-id="b7025-164">`[Tag <IResourceTags>]`: Список пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="b7025-164">`[Tag <IResourceTags>]`: List of key-value pairs.</span></span>
    - <span data-ttu-id="b7025-165">`[(Any) <String>]`: Это указывает на то, что в этот объект можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="b7025-165">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="b7025-166">`[AddressPrefix <String>]`: Префикс адреса.</span><span class="sxs-lookup"><span data-stu-id="b7025-166">`[AddressPrefix <String>]`: The address prefix.</span></span>
  - <span data-ttu-id="b7025-167">`[EndIPAddress <String>]`: Конечный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="b7025-167">`[EndIPAddress <String>]`: The ending IP address.</span></span>
  - <span data-ttu-id="b7025-168">`[NumberOfAllocatedIPAddresses <Int64?>]`: Количество выделенных в настоящее время IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="b7025-168">`[NumberOfAllocatedIPAddresses <Int64?>]`: The number of currently allocated IP addresses.</span></span>
  - <span data-ttu-id="b7025-169">`[NumberOfIPAddresses <Int64?>]`: Общее число IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="b7025-169">`[NumberOfIPAddresses <Int64?>]`: The total number of IP addresses.</span></span>
  - <span data-ttu-id="b7025-170">`[NumberOfIPAddressesInTransition <Int64?>]`: Текущее число IP-адресов в переходе.</span><span class="sxs-lookup"><span data-stu-id="b7025-170">`[NumberOfIPAddressesInTransition <Int64?>]`: The current number of IP addresses in transition.</span></span>
  - <span data-ttu-id="b7025-171">`[StartIPAddress <String>]`: Начальный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="b7025-171">`[StartIPAddress <String>]`: The starting IP address.</span></span>

## <span data-ttu-id="b7025-172">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b7025-172">RELATED LINKS</span></span>
