---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 865ab4ab3cca9d921fc8c40e9c6ae5cd03eaf00a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235492"
---
# <span data-ttu-id="9c9dd-101">Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="9c9dd-101">Remove-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="9c9dd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9c9dd-102">SYNOPSIS</span></span>
<span data-ttu-id="9c9dd-103">Удаляет набор записей из частной зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="9c9dd-103">Deletes a record set from a Private DNS zone.</span></span>

## <span data-ttu-id="9c9dd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9c9dd-104">SYNTAX</span></span>

### <span data-ttu-id="9c9dd-105">Поля (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9c9dd-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9c9dd-106">Смешивания</span><span class="sxs-lookup"><span data-stu-id="9c9dd-106">Mixed</span></span>
```
Remove-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c9dd-107">DataObject</span><span class="sxs-lookup"><span data-stu-id="9c9dd-107">Object</span></span>
```
Remove-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c9dd-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c9dd-108">ResourceId</span></span>
```
Remove-AzPrivateDnsRecordSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c9dd-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c9dd-109">DESCRIPTION</span></span>
<span data-ttu-id="9c9dd-110">Командлет Remove-AzPrivateDnsRecordSet удаляет набор записей из указанной зоны.</span><span class="sxs-lookup"><span data-stu-id="9c9dd-110">The Remove-AzPrivateDnsRecordSet cmdlet deletes the specified record set from the specified zone.</span></span> <span data-ttu-id="9c9dd-111">Невозможно удалить записи SOA, автоматически созданные в частной зоне Апекс.</span><span class="sxs-lookup"><span data-stu-id="9c9dd-111">You cannot delete SOA records that are automatically created at the private zone apex.</span></span> <span data-ttu-id="9c9dd-112">Вы можете передать в этот командлет объект набора записей с помощью оператора конвейера или как параметра или в качестве ResourceId.</span><span class="sxs-lookup"><span data-stu-id="9c9dd-112">You can pass a RecordSet object to this cmdlet by using the pipeline operator or as a parameter or as a ResourceId.</span></span> <span data-ttu-id="9c9dd-113">Чтобы определить набор записей по имени и типу, не используя объект RecordSet, необходимо передать зону как объект PSPrivateDnsZone с помощью оператора конвейера или в качестве параметра либо можно указать параметры ZoneName и ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="9c9dd-113">To identify a record set by name and type without using a RecordSet object, you must pass the zone as a PSPrivateDnsZone object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the ZoneName and ResourceGroupName parameters.</span></span> <span data-ttu-id="9c9dd-114">Вы можете использовать параметр Confirm и $ConfirmPreference переменной Windows PowerShell, чтобы указать, нужно ли командлету запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="9c9dd-114">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="9c9dd-115">При указании набора записей с помощью объекта RecordSet набор записей не удаляется, если он был изменен в службе Azure Private DNS, поскольку был получен объект локального набора записей.</span><span class="sxs-lookup"><span data-stu-id="9c9dd-115">When specifying the record set using a RecordSet object, the record set is not deleted if it has been changed in Azure Private DNS since the local RecordSet object was retrieved.</span></span> <span data-ttu-id="9c9dd-116">Это обеспечивает защиту для параллельных изменений.</span><span class="sxs-lookup"><span data-stu-id="9c9dd-116">This provides protection for concurrent changes.</span></span> <span data-ttu-id="9c9dd-117">Вы можете отключить этот параметр с помощью параметра overwrite, который удаляет набор записей независимо от текущих изменений.</span><span class="sxs-lookup"><span data-stu-id="9c9dd-117">You can suppress this by using the Overwrite parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="9c9dd-118">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9c9dd-118">EXAMPLES</span></span>

### <span data-ttu-id="9c9dd-119">Пример 1: удаление набор записей</span><span class="sxs-lookup"><span data-stu-id="9c9dd-119">Example 1: Remove a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="9c9dd-120">Первая команда получает указанный наборы записей и сохраняет ее в переменной $RecordSet. Вторая команда удаляет запись, указанную в $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="9c9dd-120">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="9c9dd-121">Пример 2: удаление набор записей и отключение всех подтверждений</span><span class="sxs-lookup"><span data-stu-id="9c9dd-121">Example 2: Remove a record set and suppress all confirmation</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzPrivateDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzPrivateDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="9c9dd-122">Первая команда получает указанный наборы записей.</span><span class="sxs-lookup"><span data-stu-id="9c9dd-122">The first command gets the specified record set.</span></span> <span data-ttu-id="9c9dd-123">Вторая команда удаляет наборы записей, даже если она была изменена.</span><span class="sxs-lookup"><span data-stu-id="9c9dd-123">The second command deletes the record set, even if it has changed in the meantime.</span></span> <span data-ttu-id="9c9dd-124">Запросы на подтверждение подавляются.</span><span class="sxs-lookup"><span data-stu-id="9c9dd-124">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="9c9dd-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9c9dd-125">PARAMETERS</span></span>

### <span data-ttu-id="9c9dd-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c9dd-126">-DefaultProfile</span></span>
<span data-ttu-id="9c9dd-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9c9dd-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c9dd-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9c9dd-128">-Name</span></span>
<span data-ttu-id="9c9dd-129">Имена записей в наборе записей (относительно имени зоны и без точки).</span><span class="sxs-lookup"><span data-stu-id="9c9dd-129">The name of the records in the record set (relative to the name of the zone and without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c9dd-130">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="9c9dd-130">-Overwrite</span></span>
<span data-ttu-id="9c9dd-131">Не используйте поле ETag в параметре RecordSet для проверки оптимистического параллелизма.</span><span class="sxs-lookup"><span data-stu-id="9c9dd-131">Do not use the ETag field of the RecordSet parameter for optimistic concurrency checks.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c9dd-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c9dd-132">-PassThru</span></span>
<span data-ttu-id="9c9dd-133">Используется для передачи результата (логического значения) операции Delete My Private Zone дальше вниз по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="9c9dd-133">Used for passing the result (boolean) of the operation delete private zone further down the pipeline.</span></span>

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

### <span data-ttu-id="9c9dd-134">-Набор записей</span><span class="sxs-lookup"><span data-stu-id="9c9dd-134">-RecordSet</span></span>
<span data-ttu-id="9c9dd-135">Настройка записи, в которую нужно добавить запись.</span><span class="sxs-lookup"><span data-stu-id="9c9dd-135">The record set in which to add the record.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c9dd-136">-RecordType</span><span class="sxs-lookup"><span data-stu-id="9c9dd-136">-RecordType</span></span>
<span data-ttu-id="9c9dd-137">Тип частных DNS-записей в наборе записей.</span><span class="sxs-lookup"><span data-stu-id="9c9dd-137">The type of Private DNS records in the record set.</span></span>

```yaml
Type: Microsoft.Azure.Management.PrivateDns.Models.RecordType
Parameter Sets: Fields, Mixed
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c9dd-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c9dd-138">-ResourceGroupName</span></span>
<span data-ttu-id="9c9dd-139">Группа ресурсов, к которой принадлежит зона.</span><span class="sxs-lookup"><span data-stu-id="9c9dd-139">The resource group to which the zone belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c9dd-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c9dd-140">-ResourceId</span></span>
<span data-ttu-id="9c9dd-141">Частный ResourceID (набор записей DNS).</span><span class="sxs-lookup"><span data-stu-id="9c9dd-141">Private DNS RecordSet ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c9dd-142">-Zone</span><span class="sxs-lookup"><span data-stu-id="9c9dd-142">-Zone</span></span>
<span data-ttu-id="9c9dd-143">Объект PrivateDnsZone, представляющий зону, в которой нужно создать набор записей.</span><span class="sxs-lookup"><span data-stu-id="9c9dd-143">The PrivateDnsZone object representing the zone in which to create the record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c9dd-144">-ИмяЗоны</span><span class="sxs-lookup"><span data-stu-id="9c9dd-144">-ZoneName</span></span>
<span data-ttu-id="9c9dd-145">Зона, в которой находится набор записей (без точки завершения).</span><span class="sxs-lookup"><span data-stu-id="9c9dd-145">The zone in which the record set exists (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c9dd-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c9dd-146">-Confirm</span></span>
<span data-ttu-id="9c9dd-147">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9c9dd-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c9dd-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c9dd-148">-WhatIf</span></span>
<span data-ttu-id="9c9dd-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9c9dd-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c9dd-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9c9dd-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c9dd-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c9dd-151">CommonParameters</span></span>
<span data-ttu-id="9c9dd-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9c9dd-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c9dd-153">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c9dd-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c9dd-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9c9dd-154">INPUTS</span></span>

### <span data-ttu-id="9c9dd-155">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="9c9dd-155">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="9c9dd-156">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="9c9dd-156">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

### <span data-ttu-id="9c9dd-157">System. String</span><span class="sxs-lookup"><span data-stu-id="9c9dd-157">System.String</span></span>

## <span data-ttu-id="9c9dd-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c9dd-158">OUTPUTS</span></span>

### <span data-ttu-id="9c9dd-159">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9c9dd-159">System.Boolean</span></span>

## <span data-ttu-id="9c9dd-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="9c9dd-160">NOTES</span></span>

## <span data-ttu-id="9c9dd-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9c9dd-161">RELATED LINKS</span></span>
