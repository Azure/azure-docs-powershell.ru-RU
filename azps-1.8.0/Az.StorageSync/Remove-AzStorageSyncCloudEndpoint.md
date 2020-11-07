---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/remove-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 2d9ad2417041f39ea43f48813310869f1ea7f353
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728482"
---
# <span data-ttu-id="4e887-101">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="4e887-101">Remove-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="4e887-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e887-102">SYNOPSIS</span></span>
<span data-ttu-id="4e887-103">Эта команда удалит указанную облачную конечную точку из группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="4e887-103">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="4e887-104">Без хотя бы одной конечной точки облака нельзя синхронизировать другие конечные точки сервера в этой группе синхронизации.</span><span class="sxs-lookup"><span data-stu-id="4e887-104">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

## <span data-ttu-id="4e887-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e887-105">SYNTAX</span></span>

### <span data-ttu-id="4e887-106">StringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4e887-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e887-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e887-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-InputObject] <PSCloudEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e887-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e887-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e887-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e887-109">DESCRIPTION</span></span>
<span data-ttu-id="4e887-110">Эта команда удалит указанную облачную конечную точку из группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="4e887-110">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="4e887-111">Файл Azure, на который ссылается облачная конечная точка, не поддерживает этот процесс.</span><span class="sxs-lookup"><span data-stu-id="4e887-111">The Azure file share the cloud endpoint references remains untouched by this process.</span></span> <span data-ttu-id="4e887-112">Эта команда предназначена только для списания.</span><span class="sxs-lookup"><span data-stu-id="4e887-112">This command is only intended for decommissioning.</span></span> <span data-ttu-id="4e887-113">Удаление облачной конечной точки является разрушительной операцией.</span><span class="sxs-lookup"><span data-stu-id="4e887-113">Removing a cloud endpoint is a destructive operation.</span></span> <span data-ttu-id="4e887-114">Конечные точки сервера не могут синхронизироваться, если присутствует хотя бы одна конечная точка облака.</span><span class="sxs-lookup"><span data-stu-id="4e887-114">Server endpoints cannot sync without at least one cloud endpoint present.</span></span> <span data-ttu-id="4e887-115">Эта операция не должна выполняться для решения проблем с синхронизацией.</span><span class="sxs-lookup"><span data-stu-id="4e887-115">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="4e887-116">Если эта файловая служба Azure будет добавлена в ту же группу синхронизации, как облачную конечную точку, это может привести к конфликтным файлам и другим нежелательным последствиям.</span><span class="sxs-lookup"><span data-stu-id="4e887-116">If this Azure file share is added again to the same sync group, as a cloud endpoint, it can lead to conflict files and other unintended consequences.</span></span>

## <span data-ttu-id="4e887-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e887-117">EXAMPLES</span></span>

### <span data-ttu-id="4e887-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4e887-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncCloudEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName"
```

<span data-ttu-id="4e887-119">Эта команда удалит конечную точку облака.</span><span class="sxs-lookup"><span data-stu-id="4e887-119">This command will remove the cloud endpoint.</span></span>

## <span data-ttu-id="4e887-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e887-120">PARAMETERS</span></span>

### <span data-ttu-id="4e887-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e887-121">-AsJob</span></span>
<span data-ttu-id="4e887-122">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="4e887-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4e887-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e887-123">-DefaultProfile</span></span>
<span data-ttu-id="4e887-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e887-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e887-125">-Force</span><span class="sxs-lookup"><span data-stu-id="4e887-125">-Force</span></span>
<span data-ttu-id="4e887-126">Укажите, чтобы пропустить подтверждение этой команды.</span><span class="sxs-lookup"><span data-stu-id="4e887-126">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="4e887-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e887-127">-InputObject</span></span>
<span data-ttu-id="4e887-128">Входной объект CloudEndpoint, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="4e887-128">CloudEndpoint Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="4e887-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4e887-129">-Name</span></span>
<span data-ttu-id="4e887-130">Имя CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="4e887-130">Name of the CloudEndpoint.</span></span>

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

### <span data-ttu-id="4e887-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e887-131">-PassThru</span></span>
<span data-ttu-id="4e887-132">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="4e887-132">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="4e887-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e887-133">-ResourceGroupName</span></span>
<span data-ttu-id="4e887-134">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4e887-134">Resource Group Name.</span></span>

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

### <span data-ttu-id="4e887-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e887-135">-ResourceId</span></span>
<span data-ttu-id="4e887-136">Идентификатор ресурса CloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="4e887-136">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="4e887-137">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="4e887-137">-StorageSyncServiceName</span></span>
<span data-ttu-id="4e887-138">Имя StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="4e887-138">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="4e887-139">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="4e887-139">-SyncGroupName</span></span>
<span data-ttu-id="4e887-140">Имя SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="4e887-140">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="4e887-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e887-141">-Confirm</span></span>
<span data-ttu-id="4e887-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4e887-142">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e887-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e887-143">-WhatIf</span></span>
<span data-ttu-id="4e887-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4e887-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4e887-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4e887-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e887-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e887-146">CommonParameters</span></span>
<span data-ttu-id="4e887-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e887-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e887-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e887-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e887-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e887-149">INPUTS</span></span>

### <span data-ttu-id="4e887-150">Microsoft. Azure. Commands. StorageSync. Models. PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="4e887-150">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

### <span data-ttu-id="4e887-151">System. String</span><span class="sxs-lookup"><span data-stu-id="4e887-151">System.String</span></span>

## <span data-ttu-id="4e887-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e887-152">OUTPUTS</span></span>

### <span data-ttu-id="4e887-153">System. Object</span><span class="sxs-lookup"><span data-stu-id="4e887-153">System.Object</span></span>
## <span data-ttu-id="4e887-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e887-154">NOTES</span></span>

## <span data-ttu-id="4e887-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e887-155">RELATED LINKS</span></span>
