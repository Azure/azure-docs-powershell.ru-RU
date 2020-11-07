---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
ms.openlocfilehash: f7c1f129d9a5f6f6bdd117597a2943567fb4001d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728481"
---
# <span data-ttu-id="2620b-101">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="2620b-101">Remove-AzStorageSyncGroup</span></span>

## <span data-ttu-id="2620b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2620b-102">SYNOPSIS</span></span>
<span data-ttu-id="2620b-103">Эта команда удалит указанную группу синхронизации.</span><span class="sxs-lookup"><span data-stu-id="2620b-103">This command will delete the specified sync group.</span></span>

## <span data-ttu-id="2620b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2620b-104">SYNTAX</span></span>

### <span data-ttu-id="2620b-105">StringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2620b-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2620b-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2620b-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-InputObject] <PSSyncGroup> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2620b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2620b-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2620b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2620b-108">DESCRIPTION</span></span>
<span data-ttu-id="2620b-109">Эта команда удалит указанную группу синхронизации.</span><span class="sxs-lookup"><span data-stu-id="2620b-109">This command will delete the specified sync group.</span></span> <span data-ttu-id="2620b-110">Группа синхронизации может быть удалена только в том случае, если все содержащиеся в ней конечные точки удаляются первыми.</span><span class="sxs-lookup"><span data-stu-id="2620b-110">A sync group can only be removed when all of the contained endpoints are deleted first.</span></span>

## <span data-ttu-id="2620b-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2620b-111">EXAMPLES</span></span>

### <span data-ttu-id="2620b-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2620b-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncGroup -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="2620b-113">Эта команда удалит группу синхронизации.</span><span class="sxs-lookup"><span data-stu-id="2620b-113">This command will remove the sync group.</span></span>

## <span data-ttu-id="2620b-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2620b-114">PARAMETERS</span></span>

### <span data-ttu-id="2620b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2620b-115">-AsJob</span></span>
<span data-ttu-id="2620b-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2620b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2620b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2620b-117">-DefaultProfile</span></span>
<span data-ttu-id="2620b-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2620b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2620b-119">-Force</span><span class="sxs-lookup"><span data-stu-id="2620b-119">-Force</span></span>
<span data-ttu-id="2620b-120">Укажите, чтобы пропустить подтверждение этой команды.</span><span class="sxs-lookup"><span data-stu-id="2620b-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="2620b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2620b-121">-InputObject</span></span>
<span data-ttu-id="2620b-122">Объект ввода SyncGroup</span><span class="sxs-lookup"><span data-stu-id="2620b-122">SyncGroup Input Object</span></span>

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

### <span data-ttu-id="2620b-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2620b-123">-Name</span></span>
<span data-ttu-id="2620b-124">Имя SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="2620b-124">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="2620b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2620b-125">-PassThru</span></span>
<span data-ttu-id="2620b-126">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="2620b-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="2620b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2620b-127">-ResourceGroupName</span></span>
<span data-ttu-id="2620b-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2620b-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="2620b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2620b-129">-ResourceId</span></span>
<span data-ttu-id="2620b-130">Идентификатор ресурса SyncGroup</span><span class="sxs-lookup"><span data-stu-id="2620b-130">SyncGroup Resource Id</span></span>

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

### <span data-ttu-id="2620b-131">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="2620b-131">-StorageSyncServiceName</span></span>
<span data-ttu-id="2620b-132">Имя StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="2620b-132">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="2620b-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2620b-133">-Confirm</span></span>
<span data-ttu-id="2620b-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2620b-134">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2620b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2620b-135">-WhatIf</span></span>
<span data-ttu-id="2620b-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2620b-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2620b-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2620b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2620b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2620b-138">CommonParameters</span></span>
<span data-ttu-id="2620b-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2620b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2620b-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2620b-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2620b-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2620b-141">INPUTS</span></span>

### <span data-ttu-id="2620b-142">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="2620b-142">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="2620b-143">System. String</span><span class="sxs-lookup"><span data-stu-id="2620b-143">System.String</span></span>

### <span data-ttu-id="2620b-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2620b-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2620b-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2620b-145">OUTPUTS</span></span>

### <span data-ttu-id="2620b-146">System. Object</span><span class="sxs-lookup"><span data-stu-id="2620b-146">System.Object</span></span>
## <span data-ttu-id="2620b-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="2620b-147">NOTES</span></span>

## <span data-ttu-id="2620b-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2620b-148">RELATED LINKS</span></span>
