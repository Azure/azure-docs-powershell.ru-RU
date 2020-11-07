---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/remove-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 4c78e636788ea1c91f4ff71b8439f84097503d82
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907521"
---
# <span data-ttu-id="fca57-101">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="fca57-101">Remove-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="fca57-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fca57-102">SYNOPSIS</span></span>
<span data-ttu-id="fca57-103">Эта команда удалит указанную облачную конечную точку из группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="fca57-103">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="fca57-104">Без хотя бы одной конечной точки облака нельзя синхронизировать другие конечные точки сервера в этой группе синхронизации.</span><span class="sxs-lookup"><span data-stu-id="fca57-104">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

## <span data-ttu-id="fca57-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fca57-105">SYNTAX</span></span>

### <span data-ttu-id="fca57-106">StringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fca57-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fca57-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fca57-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-InputObject] <PSCloudEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fca57-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fca57-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fca57-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fca57-109">DESCRIPTION</span></span>
<span data-ttu-id="fca57-110">Эта команда удалит указанную облачную конечную точку из группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="fca57-110">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="fca57-111">Файл Azure, на который ссылается облачная конечная точка, не поддерживает этот процесс.</span><span class="sxs-lookup"><span data-stu-id="fca57-111">The Azure file share the cloud endpoint references remains untouched by this process.</span></span> <span data-ttu-id="fca57-112">Эта команда предназначена только для списания.</span><span class="sxs-lookup"><span data-stu-id="fca57-112">This command is only intended for decommissioning.</span></span> <span data-ttu-id="fca57-113">Удаление облачной конечной точки является разрушительной операцией.</span><span class="sxs-lookup"><span data-stu-id="fca57-113">Removing a cloud endpoint is a destructive operation.</span></span> <span data-ttu-id="fca57-114">Конечные точки сервера не могут синхронизироваться, если присутствует хотя бы одна конечная точка облака.</span><span class="sxs-lookup"><span data-stu-id="fca57-114">Server endpoints cannot sync without at least one cloud endpoint present.</span></span> <span data-ttu-id="fca57-115">Эта операция не должна выполняться для решения проблем с синхронизацией.</span><span class="sxs-lookup"><span data-stu-id="fca57-115">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="fca57-116">Если эта файловая служба Azure будет добавлена в ту же группу синхронизации, как облачную конечную точку, это может привести к конфликтным файлам и другим нежелательным последствиям.</span><span class="sxs-lookup"><span data-stu-id="fca57-116">If this Azure file share is added again to the same sync group, as a cloud endpoint, it can lead to conflict files and other unintended consequences.</span></span>

## <span data-ttu-id="fca57-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fca57-117">EXAMPLES</span></span>

### <span data-ttu-id="fca57-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fca57-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncCloudEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName"
```

<span data-ttu-id="fca57-119">Эта команда удалит конечную точку облака.</span><span class="sxs-lookup"><span data-stu-id="fca57-119">This command will remove the cloud endpoint.</span></span>

## <span data-ttu-id="fca57-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fca57-120">PARAMETERS</span></span>

### <span data-ttu-id="fca57-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fca57-121">-AsJob</span></span>
<span data-ttu-id="fca57-122">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="fca57-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fca57-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fca57-123">-DefaultProfile</span></span>
<span data-ttu-id="fca57-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fca57-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fca57-125">-Force</span><span class="sxs-lookup"><span data-stu-id="fca57-125">-Force</span></span>
<span data-ttu-id="fca57-126">Укажите, чтобы пропустить подтверждение этой команды.</span><span class="sxs-lookup"><span data-stu-id="fca57-126">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="fca57-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fca57-127">-InputObject</span></span>
<span data-ttu-id="fca57-128">Входной объект CloudEndpoint, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="fca57-128">CloudEndpoint Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="fca57-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fca57-129">-Name</span></span>
<span data-ttu-id="fca57-130">Имя CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="fca57-130">Name of the CloudEndpoint.</span></span>

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

### <span data-ttu-id="fca57-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fca57-131">-PassThru</span></span>
<span data-ttu-id="fca57-132">При нормальном выполнении этот командлет не возвращает значение в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="fca57-132">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="fca57-133">Если вы предоставляете параметр PassThru, командлет запишет значение в конвейер после успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="fca57-133">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="fca57-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fca57-134">-ResourceGroupName</span></span>
<span data-ttu-id="fca57-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fca57-135">Resource Group Name.</span></span>

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

### <span data-ttu-id="fca57-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fca57-136">-ResourceId</span></span>
<span data-ttu-id="fca57-137">Идентификатор ресурса CloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="fca57-137">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="fca57-138">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="fca57-138">-StorageSyncServiceName</span></span>
<span data-ttu-id="fca57-139">Имя StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="fca57-139">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="fca57-140">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="fca57-140">-SyncGroupName</span></span>
<span data-ttu-id="fca57-141">Имя SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="fca57-141">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="fca57-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fca57-142">-Confirm</span></span>
<span data-ttu-id="fca57-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fca57-143">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fca57-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fca57-144">-WhatIf</span></span>
<span data-ttu-id="fca57-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fca57-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fca57-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fca57-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fca57-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fca57-147">CommonParameters</span></span>
<span data-ttu-id="fca57-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fca57-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fca57-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fca57-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fca57-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fca57-150">INPUTS</span></span>

### <span data-ttu-id="fca57-151">Microsoft. Azure. Commands. StorageSync. Models. PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="fca57-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

### <span data-ttu-id="fca57-152">System. String</span><span class="sxs-lookup"><span data-stu-id="fca57-152">System.String</span></span>

## <span data-ttu-id="fca57-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fca57-153">OUTPUTS</span></span>

### <span data-ttu-id="fca57-154">System. Object</span><span class="sxs-lookup"><span data-stu-id="fca57-154">System.Object</span></span>
## <span data-ttu-id="fca57-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="fca57-155">NOTES</span></span>

## <span data-ttu-id="fca57-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fca57-156">RELATED LINKS</span></span>
