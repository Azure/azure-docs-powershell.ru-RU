---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
ms.openlocfilehash: dad4af4f954fae03a68728de928614a81eed5e5a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414540"
---
# <span data-ttu-id="f72eb-101">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="f72eb-101">Remove-AzStorageSyncGroup</span></span>

## <span data-ttu-id="f72eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f72eb-102">SYNOPSIS</span></span>
<span data-ttu-id="f72eb-103">Эта команда удалит указанную группу синхронизации.</span><span class="sxs-lookup"><span data-stu-id="f72eb-103">This command will delete the specified sync group.</span></span>

## <span data-ttu-id="f72eb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f72eb-104">SYNTAX</span></span>

### <span data-ttu-id="f72eb-105">StringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f72eb-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f72eb-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f72eb-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-InputObject] <PSSyncGroup> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f72eb-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f72eb-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f72eb-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f72eb-108">DESCRIPTION</span></span>
<span data-ttu-id="f72eb-109">Эта команда удалит указанную группу синхронизации.</span><span class="sxs-lookup"><span data-stu-id="f72eb-109">This command will delete the specified sync group.</span></span> <span data-ttu-id="f72eb-110">Группу синхронизации можно удалить только в том случае, если сначала удаляются все содержащиеся в ней конечные точки.</span><span class="sxs-lookup"><span data-stu-id="f72eb-110">A sync group can only be removed when all of the contained endpoints are deleted first.</span></span>

## <span data-ttu-id="f72eb-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f72eb-111">EXAMPLES</span></span>

### <span data-ttu-id="f72eb-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f72eb-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncGroup -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="f72eb-113">Эта команда удалит группу синхронизации.</span><span class="sxs-lookup"><span data-stu-id="f72eb-113">This command will remove the sync group.</span></span>

## <span data-ttu-id="f72eb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f72eb-114">PARAMETERS</span></span>

### <span data-ttu-id="f72eb-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f72eb-115">-AsJob</span></span>
<span data-ttu-id="f72eb-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f72eb-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f72eb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f72eb-117">-DefaultProfile</span></span>
<span data-ttu-id="f72eb-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f72eb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f72eb-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f72eb-119">-Force</span></span>
<span data-ttu-id="f72eb-120">Supply -Force, чтобы пропустить подтверждение этой команды.</span><span class="sxs-lookup"><span data-stu-id="f72eb-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="f72eb-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f72eb-121">-InputObject</span></span>
<span data-ttu-id="f72eb-122">Объект ввода SyncGroup</span><span class="sxs-lookup"><span data-stu-id="f72eb-122">SyncGroup Input Object</span></span>

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

### <span data-ttu-id="f72eb-123">-Name</span><span class="sxs-lookup"><span data-stu-id="f72eb-123">-Name</span></span>
<span data-ttu-id="f72eb-124">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="f72eb-124">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="f72eb-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f72eb-125">-PassThru</span></span>
<span data-ttu-id="f72eb-126">В обычном выполнении этот cmdlet не возвращает никакого значения для успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="f72eb-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="f72eb-127">Если задан параметр PassThru, то после успешного выполнения cmdlet напишет значение в конвейер.</span><span class="sxs-lookup"><span data-stu-id="f72eb-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="f72eb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f72eb-128">-ResourceGroupName</span></span>
<span data-ttu-id="f72eb-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f72eb-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="f72eb-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f72eb-130">-ResourceId</span></span>
<span data-ttu-id="f72eb-131">ИД ресурса SyncGroup</span><span class="sxs-lookup"><span data-stu-id="f72eb-131">SyncGroup Resource Id</span></span>

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

### <span data-ttu-id="f72eb-132">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="f72eb-132">-StorageSyncServiceName</span></span>
<span data-ttu-id="f72eb-133">Имя службы StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="f72eb-133">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="f72eb-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f72eb-134">-Confirm</span></span>
<span data-ttu-id="f72eb-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f72eb-135">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f72eb-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f72eb-136">-WhatIf</span></span>
<span data-ttu-id="f72eb-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f72eb-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f72eb-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f72eb-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f72eb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f72eb-139">CommonParameters</span></span>
<span data-ttu-id="f72eb-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f72eb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f72eb-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f72eb-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f72eb-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f72eb-142">INPUTS</span></span>

### <span data-ttu-id="f72eb-143">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="f72eb-143">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="f72eb-144">System.String</span><span class="sxs-lookup"><span data-stu-id="f72eb-144">System.String</span></span>

### <span data-ttu-id="f72eb-145">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f72eb-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f72eb-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f72eb-146">OUTPUTS</span></span>

### <span data-ttu-id="f72eb-147">System.Object</span><span class="sxs-lookup"><span data-stu-id="f72eb-147">System.Object</span></span>
## <span data-ttu-id="f72eb-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f72eb-148">NOTES</span></span>

## <span data-ttu-id="f72eb-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f72eb-149">RELATED LINKS</span></span>
