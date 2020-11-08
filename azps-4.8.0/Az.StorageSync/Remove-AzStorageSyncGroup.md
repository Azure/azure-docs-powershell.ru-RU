---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
ms.openlocfilehash: dad4af4f954fae03a68728de928614a81eed5e5a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235211"
---
# <span data-ttu-id="4e7a7-101">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="4e7a7-101">Remove-AzStorageSyncGroup</span></span>

## <span data-ttu-id="4e7a7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e7a7-102">SYNOPSIS</span></span>
<span data-ttu-id="4e7a7-103">Эта команда удалит указанную группу синхронизации.</span><span class="sxs-lookup"><span data-stu-id="4e7a7-103">This command will delete the specified sync group.</span></span>

## <span data-ttu-id="4e7a7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e7a7-104">SYNTAX</span></span>

### <span data-ttu-id="4e7a7-105">StringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4e7a7-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4e7a7-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e7a7-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-InputObject] <PSSyncGroup> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e7a7-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e7a7-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e7a7-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e7a7-108">DESCRIPTION</span></span>
<span data-ttu-id="4e7a7-109">Эта команда удалит указанную группу синхронизации.</span><span class="sxs-lookup"><span data-stu-id="4e7a7-109">This command will delete the specified sync group.</span></span> <span data-ttu-id="4e7a7-110">Группа синхронизации может быть удалена только в том случае, если все содержащиеся в ней конечные точки удаляются первыми.</span><span class="sxs-lookup"><span data-stu-id="4e7a7-110">A sync group can only be removed when all of the contained endpoints are deleted first.</span></span>

## <span data-ttu-id="4e7a7-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e7a7-111">EXAMPLES</span></span>

### <span data-ttu-id="4e7a7-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4e7a7-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncGroup -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="4e7a7-113">Эта команда удалит группу синхронизации.</span><span class="sxs-lookup"><span data-stu-id="4e7a7-113">This command will remove the sync group.</span></span>

## <span data-ttu-id="4e7a7-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e7a7-114">PARAMETERS</span></span>

### <span data-ttu-id="4e7a7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e7a7-115">-AsJob</span></span>
<span data-ttu-id="4e7a7-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="4e7a7-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4e7a7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e7a7-117">-DefaultProfile</span></span>
<span data-ttu-id="4e7a7-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e7a7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e7a7-119">-Force</span><span class="sxs-lookup"><span data-stu-id="4e7a7-119">-Force</span></span>
<span data-ttu-id="4e7a7-120">Укажите, чтобы пропустить подтверждение этой команды.</span><span class="sxs-lookup"><span data-stu-id="4e7a7-120">Supply -Force to skip confirmation of this command.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e7a7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e7a7-121">-InputObject</span></span>
<span data-ttu-id="4e7a7-122">Объект ввода SyncGroup</span><span class="sxs-lookup"><span data-stu-id="4e7a7-122">SyncGroup Input Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e7a7-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4e7a7-123">-Name</span></span>
<span data-ttu-id="4e7a7-124">Имя SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="4e7a7-124">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: SyncGroupName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e7a7-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e7a7-125">-PassThru</span></span>
<span data-ttu-id="4e7a7-126">При нормальном выполнении этот командлет не возвращает значение в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="4e7a7-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="4e7a7-127">Если вы предоставляете параметр PassThru, командлет запишет значение в конвейер после успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="4e7a7-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="4e7a7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e7a7-128">-ResourceGroupName</span></span>
<span data-ttu-id="4e7a7-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4e7a7-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e7a7-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e7a7-130">-ResourceId</span></span>
<span data-ttu-id="4e7a7-131">Идентификатор ресурса SyncGroup</span><span class="sxs-lookup"><span data-stu-id="4e7a7-131">SyncGroup Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e7a7-132">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="4e7a7-132">-StorageSyncServiceName</span></span>
<span data-ttu-id="4e7a7-133">Имя StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="4e7a7-133">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e7a7-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e7a7-134">-Confirm</span></span>
<span data-ttu-id="4e7a7-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4e7a7-135">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e7a7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e7a7-136">-WhatIf</span></span>
<span data-ttu-id="4e7a7-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4e7a7-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4e7a7-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4e7a7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e7a7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e7a7-139">CommonParameters</span></span>
<span data-ttu-id="4e7a7-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e7a7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e7a7-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e7a7-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e7a7-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e7a7-142">INPUTS</span></span>

### <span data-ttu-id="4e7a7-143">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="4e7a7-143">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="4e7a7-144">System. String</span><span class="sxs-lookup"><span data-stu-id="4e7a7-144">System.String</span></span>

### <span data-ttu-id="4e7a7-145">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4e7a7-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4e7a7-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e7a7-146">OUTPUTS</span></span>

### <span data-ttu-id="4e7a7-147">System. Object</span><span class="sxs-lookup"><span data-stu-id="4e7a7-147">System.Object</span></span>
## <span data-ttu-id="4e7a7-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e7a7-148">NOTES</span></span>

## <span data-ttu-id="4e7a7-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e7a7-149">RELATED LINKS</span></span>
