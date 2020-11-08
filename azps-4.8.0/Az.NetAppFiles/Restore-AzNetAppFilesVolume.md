---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/restore-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Restore-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Restore-AzNetAppFilesVolume.md
ms.openlocfilehash: 486bd44d3f48213fde6fb9b6c1d15a5683c1fd82
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235070"
---
# <span data-ttu-id="ccf18-101">Restore-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="ccf18-101">Restore-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="ccf18-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ccf18-102">SYNOPSIS</span></span>
<span data-ttu-id="ccf18-103">Восстановление или возврат тома в один из его снимков</span><span class="sxs-lookup"><span data-stu-id="ccf18-103">Restore/Revert a volume to one of its snapshots</span></span>

## <span data-ttu-id="ccf18-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ccf18-104">SYNTAX</span></span>

### <span data-ttu-id="ccf18-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ccf18-105">ByFieldsParameterSet (Default)</span></span>
```
Revert-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-SnapshotId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ccf18-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccf18-106">ByParentObjectParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccf18-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccf18-107">ByResourceIdParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccf18-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccf18-108">ByObjectParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccf18-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ccf18-109">DESCRIPTION</span></span>
<span data-ttu-id="ccf18-110">Восстановление или возврат тома в снимок, указанный в SnapshotId</span><span class="sxs-lookup"><span data-stu-id="ccf18-110">Restore/Revert a volume to the snapshot specified in the SnapshotId paramter</span></span>

## <span data-ttu-id="ccf18-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ccf18-111">EXAMPLES</span></span>

### <span data-ttu-id="ccf18-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ccf18-112">Example 1</span></span>
```powershell
PS C:\> Restore-AzNetAppFilesVolume -ResourceGroupName "MyRG" -Location "westus2" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -SnapshotId 7d6e4069-6c78-6c61-7bf6-c60968e45fbf
```

<span data-ttu-id="ccf18-113">Эта команда восстанавливает и возвращает MyVolume тома на один из его снимков с помощью snapshotId из 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span><span class="sxs-lookup"><span data-stu-id="ccf18-113">This command Restores/Reverts the volume MyVolume to one of its snapshots with the snapshotId of 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span></span>

## <span data-ttu-id="ccf18-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ccf18-114">PARAMETERS</span></span>

### <span data-ttu-id="ccf18-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="ccf18-115">-AccountName</span></span>
<span data-ttu-id="ccf18-116">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="ccf18-116">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf18-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccf18-117">-DefaultProfile</span></span>
<span data-ttu-id="ccf18-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ccf18-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf18-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ccf18-119">-InputObject</span></span>
<span data-ttu-id="ccf18-120">Объект тома, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="ccf18-120">The volume object to remove</span></span>

```yaml
Type: PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ccf18-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ccf18-121">-Name</span></span>
<span data-ttu-id="ccf18-122">Имя ANFого тома.</span><span class="sxs-lookup"><span data-stu-id="ccf18-122">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf18-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ccf18-123">-PassThru</span></span>
<span data-ttu-id="ccf18-124">Возвращает значение, показывающее, успешно восстановлен или отменен указанный том</span><span class="sxs-lookup"><span data-stu-id="ccf18-124">Return whether the specified volume was successfully restored/reverted</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf18-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="ccf18-125">-PoolName</span></span>
<span data-ttu-id="ccf18-126">Название пула ANF</span><span class="sxs-lookup"><span data-stu-id="ccf18-126">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf18-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="ccf18-127">-PoolObject</span></span>
<span data-ttu-id="ccf18-128">Объект пула, содержащий том, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="ccf18-128">The pool object containing the volume to remove</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ccf18-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccf18-129">-ResourceGroupName</span></span>
<span data-ttu-id="ccf18-130">Группа ресурсов ANFого тома</span><span class="sxs-lookup"><span data-stu-id="ccf18-130">The resource group of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf18-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ccf18-131">-ResourceId</span></span>
<span data-ttu-id="ccf18-132">Идентификатор ресурса ANFого тома.</span><span class="sxs-lookup"><span data-stu-id="ccf18-132">The resource id of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccf18-133">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="ccf18-133">-SnapshotId</span></span>
<span data-ttu-id="ccf18-134">SnapshotId снимка.</span><span class="sxs-lookup"><span data-stu-id="ccf18-134">SnapshotId of the snapshot.</span></span>
<span data-ttu-id="ccf18-135">Идентификатор UUID V4 используется для идентификации снимка</span><span class="sxs-lookup"><span data-stu-id="ccf18-135">UUID v4 used to identify the Snapshot</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf18-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ccf18-136">-Confirm</span></span>
<span data-ttu-id="ccf18-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ccf18-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf18-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccf18-138">-WhatIf</span></span>
<span data-ttu-id="ccf18-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ccf18-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccf18-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ccf18-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf18-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccf18-141">CommonParameters</span></span>
<span data-ttu-id="ccf18-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ccf18-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccf18-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ccf18-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccf18-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ccf18-144">INPUTS</span></span>

### <span data-ttu-id="ccf18-145">System. String</span><span class="sxs-lookup"><span data-stu-id="ccf18-145">System.String</span></span>

### <span data-ttu-id="ccf18-146">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="ccf18-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="ccf18-147">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="ccf18-147">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="ccf18-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ccf18-148">OUTPUTS</span></span>

### <span data-ttu-id="ccf18-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ccf18-149">System.Boolean</span></span>

## <span data-ttu-id="ccf18-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="ccf18-150">NOTES</span></span>

## <span data-ttu-id="ccf18-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ccf18-151">RELATED LINKS</span></span>
