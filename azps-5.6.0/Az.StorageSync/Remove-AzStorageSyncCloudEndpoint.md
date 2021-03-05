---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/remove-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 451df6b0608ece9888b1525388784dcee1aac334
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974072"
---
# <span data-ttu-id="97302-101">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="97302-101">Remove-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="97302-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97302-102">SYNOPSIS</span></span>
<span data-ttu-id="97302-103">Эта команда удаляет указанную конечную точку облака из группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="97302-103">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="97302-104">Без хотя бы одной облачной конечной точки другие конечные точки сервера в этой группе синхронизации не будут синхронизироваться.</span><span class="sxs-lookup"><span data-stu-id="97302-104">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

## <span data-ttu-id="97302-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="97302-105">SYNTAX</span></span>

### <span data-ttu-id="97302-106">StringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="97302-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97302-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="97302-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-InputObject] <PSCloudEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97302-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="97302-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97302-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="97302-109">DESCRIPTION</span></span>
<span data-ttu-id="97302-110">Эта команда удаляет указанную конечную точку облака из группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="97302-110">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="97302-111">Этот процесс не затрагивает ссылки на облачные конечные точки в файле Azure.</span><span class="sxs-lookup"><span data-stu-id="97302-111">The Azure file share the cloud endpoint references remains untouched by this process.</span></span> <span data-ttu-id="97302-112">Эта команда предназначена только для списки.</span><span class="sxs-lookup"><span data-stu-id="97302-112">This command is only intended for decommissioning.</span></span> <span data-ttu-id="97302-113">Удаление облачной конечной точки — это необлагоразумная операция.</span><span class="sxs-lookup"><span data-stu-id="97302-113">Removing a cloud endpoint is a destructive operation.</span></span> <span data-ttu-id="97302-114">Конечные точки сервера не могут синхронизироваться, пока не будет хотя бы одна облачная конечная точка.</span><span class="sxs-lookup"><span data-stu-id="97302-114">Server endpoints cannot sync without at least one cloud endpoint present.</span></span> <span data-ttu-id="97302-115">Эту операцию не следует выполнять для решения проблем с синхронизацией.</span><span class="sxs-lookup"><span data-stu-id="97302-115">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="97302-116">Если эта файловая папка Azure снова добавлена в ту же группу синхронизации, как облачная конечная точка, это может привести к конфликтам файлов и другим непредвиденным последствиям.</span><span class="sxs-lookup"><span data-stu-id="97302-116">If this Azure file share is added again to the same sync group, as a cloud endpoint, it can lead to conflict files and other unintended consequences.</span></span>

## <span data-ttu-id="97302-117">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="97302-117">EXAMPLES</span></span>

### <span data-ttu-id="97302-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="97302-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncCloudEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName"
```

<span data-ttu-id="97302-119">Эта команда удалит конечную точку облака.</span><span class="sxs-lookup"><span data-stu-id="97302-119">This command will remove the cloud endpoint.</span></span>

## <span data-ttu-id="97302-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97302-120">PARAMETERS</span></span>

### <span data-ttu-id="97302-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97302-121">-AsJob</span></span>
<span data-ttu-id="97302-122">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="97302-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="97302-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97302-123">-DefaultProfile</span></span>
<span data-ttu-id="97302-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="97302-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97302-125">-Force</span><span class="sxs-lookup"><span data-stu-id="97302-125">-Force</span></span>
<span data-ttu-id="97302-126">Supply -Force, чтобы пропустить подтверждение этой команды.</span><span class="sxs-lookup"><span data-stu-id="97302-126">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="97302-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97302-127">-InputObject</span></span>
<span data-ttu-id="97302-128">Объект ввода CloudEndpoint, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="97302-128">CloudEndpoint Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97302-129">-Name</span><span class="sxs-lookup"><span data-stu-id="97302-129">-Name</span></span>
<span data-ttu-id="97302-130">Имя CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="97302-130">Name of the CloudEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97302-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="97302-131">-PassThru</span></span>
<span data-ttu-id="97302-132">В обычном выполнении этот cmdlet не возвращает никакого значения для успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="97302-132">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="97302-133">Если для параметра PassThru задан параметр PassThru, то после успешного выполнения он будет записывать значение в конвейер.</span><span class="sxs-lookup"><span data-stu-id="97302-133">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="97302-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97302-134">-ResourceGroupName</span></span>
<span data-ttu-id="97302-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="97302-135">Resource Group Name.</span></span>

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

### <span data-ttu-id="97302-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97302-136">-ResourceId</span></span>
<span data-ttu-id="97302-137">CloudEndpoint Resource Id</span><span class="sxs-lookup"><span data-stu-id="97302-137">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="97302-138">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="97302-138">-StorageSyncServiceName</span></span>
<span data-ttu-id="97302-139">Имя службы StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="97302-139">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97302-140">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="97302-140">-SyncGroupName</span></span>
<span data-ttu-id="97302-141">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="97302-141">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97302-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="97302-142">-Confirm</span></span>
<span data-ttu-id="97302-143">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97302-143">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97302-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97302-144">-WhatIf</span></span>
<span data-ttu-id="97302-145">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97302-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="97302-146">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="97302-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97302-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97302-147">CommonParameters</span></span>
<span data-ttu-id="97302-148">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97302-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97302-149">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97302-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97302-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="97302-150">INPUTS</span></span>

### <span data-ttu-id="97302-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="97302-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

### <span data-ttu-id="97302-152">System.String</span><span class="sxs-lookup"><span data-stu-id="97302-152">System.String</span></span>

## <span data-ttu-id="97302-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="97302-153">OUTPUTS</span></span>

### <span data-ttu-id="97302-154">System.Object</span><span class="sxs-lookup"><span data-stu-id="97302-154">System.Object</span></span>
## <span data-ttu-id="97302-155">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="97302-155">NOTES</span></span>

## <span data-ttu-id="97302-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="97302-156">RELATED LINKS</span></span>
