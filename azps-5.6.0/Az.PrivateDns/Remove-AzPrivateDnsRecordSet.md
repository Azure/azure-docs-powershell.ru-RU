---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/powershell/module/az.privatedns/remove-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordSet.md
ms.openlocfilehash: d54b2952c617782ec30193372b430785c0a8b79d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965576"
---
# <span data-ttu-id="039a4-101">Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="039a4-101">Remove-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="039a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="039a4-102">SYNOPSIS</span></span>
<span data-ttu-id="039a4-103">Удаляет набор записей из зоны частных DNS.</span><span class="sxs-lookup"><span data-stu-id="039a4-103">Deletes a record set from a Private DNS zone.</span></span>

## <span data-ttu-id="039a4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="039a4-104">SYNTAX</span></span>

### <span data-ttu-id="039a4-105">Поля (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="039a4-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="039a4-106">Смешанный</span><span class="sxs-lookup"><span data-stu-id="039a4-106">Mixed</span></span>
```
Remove-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="039a4-107">Объект</span><span class="sxs-lookup"><span data-stu-id="039a4-107">Object</span></span>
```
Remove-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="039a4-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="039a4-108">ResourceId</span></span>
```
Remove-AzPrivateDnsRecordSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="039a4-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="039a4-109">DESCRIPTION</span></span>
<span data-ttu-id="039a4-110">Этот Remove-AzPrivateDnsRecordSet удаляет указанный набор записей из указанной зоны.</span><span class="sxs-lookup"><span data-stu-id="039a4-110">The Remove-AzPrivateDnsRecordSet cmdlet deletes the specified record set from the specified zone.</span></span> <span data-ttu-id="039a4-111">Записи SOA, автоматически созданные в закрытой зоне, удалить нельзя.</span><span class="sxs-lookup"><span data-stu-id="039a4-111">You cannot delete SOA records that are automatically created at the private zone apex.</span></span> <span data-ttu-id="039a4-112">Передать объект RecordSet этому cmdlet можно с помощью оператора конвейера, параметра или resourceId.</span><span class="sxs-lookup"><span data-stu-id="039a4-112">You can pass a RecordSet object to this cmdlet by using the pipeline operator or as a parameter or as a ResourceId.</span></span> <span data-ttu-id="039a4-113">Чтобы определить запись, заданную по имени и типу, без использования объекта RecordSet, необходимо передать эту зону в качестве объекта PSPrivateDnsZone с помощью оператора конвейера или параметра либо указать параметры ZoneName и ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="039a4-113">To identify a record set by name and type without using a RecordSet object, you must pass the zone as a PSPrivateDnsZone object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the ZoneName and ResourceGroupName parameters.</span></span> <span data-ttu-id="039a4-114">Параметр Confirm и переменная $ConfirmPreference Windows PowerShell можно использовать для управления запросом на подтверждение с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="039a4-114">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="039a4-115">При указании набора записей с использованием объекта RecordSet набор записей не удаляется, если он был изменен в частных DNS Azure после извлечения локального объекта RecordSet.</span><span class="sxs-lookup"><span data-stu-id="039a4-115">When specifying the record set using a RecordSet object, the record set is not deleted if it has been changed in Azure Private DNS since the local RecordSet object was retrieved.</span></span> <span data-ttu-id="039a4-116">Это обеспечивает защиту от одновременного изменения.</span><span class="sxs-lookup"><span data-stu-id="039a4-116">This provides protection for concurrent changes.</span></span> <span data-ttu-id="039a4-117">Вы можете скрыть это с помощью параметра Overwrite, который удаляет набор записей независимо от одновременного изменения.</span><span class="sxs-lookup"><span data-stu-id="039a4-117">You can suppress this by using the Overwrite parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="039a4-118">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="039a4-118">EXAMPLES</span></span>

### <span data-ttu-id="039a4-119">Пример 1. Удаление набора записей</span><span class="sxs-lookup"><span data-stu-id="039a4-119">Example 1: Remove a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="039a4-120">Первая команда получает указанный набор записей, а затем сохраняет его в $RecordSet переменной. Вторая команда удаляет набор записей в $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="039a4-120">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="039a4-121">Пример 2. Удаление набора записей и подавления всего подтверждения</span><span class="sxs-lookup"><span data-stu-id="039a4-121">Example 2: Remove a record set and suppress all confirmation</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzPrivateDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzPrivateDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="039a4-122">Первая команда получает указанный набор записей.</span><span class="sxs-lookup"><span data-stu-id="039a4-122">The first command gets the specified record set.</span></span> <span data-ttu-id="039a4-123">Вторая команда удаляет набор записей, даже если он изменился до этого времени.</span><span class="sxs-lookup"><span data-stu-id="039a4-123">The second command deletes the record set, even if it has changed in the meantime.</span></span> <span data-ttu-id="039a4-124">Запросы на подтверждение будут подавляться.</span><span class="sxs-lookup"><span data-stu-id="039a4-124">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="039a4-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="039a4-125">PARAMETERS</span></span>

### <span data-ttu-id="039a4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="039a4-126">-DefaultProfile</span></span>
<span data-ttu-id="039a4-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="039a4-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="039a4-128">-Name</span><span class="sxs-lookup"><span data-stu-id="039a4-128">-Name</span></span>
<span data-ttu-id="039a4-129">Имена записей в наборе записей (относительно имени зоны и без конечной точки).</span><span class="sxs-lookup"><span data-stu-id="039a4-129">The name of the records in the record set (relative to the name of the zone and without a terminating dot).</span></span>

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

### <span data-ttu-id="039a4-130">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="039a4-130">-Overwrite</span></span>
<span data-ttu-id="039a4-131">Не используйте поле ETag параметра RecordSet для оптимистических проверок concurrency.</span><span class="sxs-lookup"><span data-stu-id="039a4-131">Do not use the ETag field of the RecordSet parameter for optimistic concurrency checks.</span></span>

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

### <span data-ttu-id="039a4-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="039a4-132">-PassThru</span></span>
<span data-ttu-id="039a4-133">Используется для передачи результата (boolean) операции удаления частной зоны далее по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="039a4-133">Used for passing the result (boolean) of the operation delete private zone further down the pipeline.</span></span>

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

### <span data-ttu-id="039a4-134">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="039a4-134">-RecordSet</span></span>
<span data-ttu-id="039a4-135">Набор записей, в который нужно добавить запись.</span><span class="sxs-lookup"><span data-stu-id="039a4-135">The record set in which to add the record.</span></span>

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

### <span data-ttu-id="039a4-136">-RecordType</span><span class="sxs-lookup"><span data-stu-id="039a4-136">-RecordType</span></span>
<span data-ttu-id="039a4-137">Тип личных записей DNS в наборе.</span><span class="sxs-lookup"><span data-stu-id="039a4-137">The type of Private DNS records in the record set.</span></span>

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

### <span data-ttu-id="039a4-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="039a4-138">-ResourceGroupName</span></span>
<span data-ttu-id="039a4-139">Группа ресурсов, к которой относится зона.</span><span class="sxs-lookup"><span data-stu-id="039a4-139">The resource group to which the zone belongs.</span></span>

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

### <span data-ttu-id="039a4-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="039a4-140">-ResourceId</span></span>
<span data-ttu-id="039a4-141">Private DNS RecordSet ResourceID.</span><span class="sxs-lookup"><span data-stu-id="039a4-141">Private DNS RecordSet ResourceID.</span></span>

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

### <span data-ttu-id="039a4-142">-Zone</span><span class="sxs-lookup"><span data-stu-id="039a4-142">-Zone</span></span>
<span data-ttu-id="039a4-143">Объект PrivateDnsZone, представляющий зону, в которой создается набор записей.</span><span class="sxs-lookup"><span data-stu-id="039a4-143">The PrivateDnsZone object representing the zone in which to create the record set.</span></span>

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

### <span data-ttu-id="039a4-144">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="039a4-144">-ZoneName</span></span>
<span data-ttu-id="039a4-145">Зона, в которой существует набор записей (без точки, которая заканчивается).</span><span class="sxs-lookup"><span data-stu-id="039a4-145">The zone in which the record set exists (without a terminating dot).</span></span>

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

### <span data-ttu-id="039a4-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="039a4-146">-Confirm</span></span>
<span data-ttu-id="039a4-147">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="039a4-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="039a4-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="039a4-148">-WhatIf</span></span>
<span data-ttu-id="039a4-149">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="039a4-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="039a4-150">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="039a4-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="039a4-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="039a4-151">CommonParameters</span></span>
<span data-ttu-id="039a4-152">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="039a4-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="039a4-153">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="039a4-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="039a4-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="039a4-154">INPUTS</span></span>

### <span data-ttu-id="039a4-155">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="039a4-155">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="039a4-156">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="039a4-156">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

### <span data-ttu-id="039a4-157">System.String</span><span class="sxs-lookup"><span data-stu-id="039a4-157">System.String</span></span>

## <span data-ttu-id="039a4-158">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="039a4-158">OUTPUTS</span></span>

### <span data-ttu-id="039a4-159">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="039a4-159">System.Boolean</span></span>

## <span data-ttu-id="039a4-160">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="039a4-160">NOTES</span></span>

## <span data-ttu-id="039a4-161">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="039a4-161">RELATED LINKS</span></span>
