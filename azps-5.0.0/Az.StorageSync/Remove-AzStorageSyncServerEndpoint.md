---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 9afb334e7c26b49bddcabdbcd1ac4036fc3a77c6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246329"
---
# <span data-ttu-id="b6447-101">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b6447-101">Remove-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="b6447-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b6447-102">SYNOPSIS</span></span>
<span data-ttu-id="b6447-103">Эта команда удалит указанную конечную точку сервера.</span><span class="sxs-lookup"><span data-stu-id="b6447-103">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="b6447-104">Синхронизация с этим расположением будет немедленно остановлена.</span><span class="sxs-lookup"><span data-stu-id="b6447-104">Sync to this location will stop immediately.</span></span>

## <span data-ttu-id="b6447-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b6447-105">SYNTAX</span></span>

### <span data-ttu-id="b6447-106">StringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b6447-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6447-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6447-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6447-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6447-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6447-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6447-109">DESCRIPTION</span></span>
<span data-ttu-id="b6447-110">Удаление конечной точки сервера является разрушительной операцией.</span><span class="sxs-lookup"><span data-stu-id="b6447-110">Removing a server endpoint is a destructive operation.</span></span> <span data-ttu-id="b6447-111">Это расположение на сервере прекратит синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="b6447-111">This server location will stop syncing.</span></span> <span data-ttu-id="b6447-112">Эта операция не должна выполняться для решения проблем с синхронизацией.</span><span class="sxs-lookup"><span data-stu-id="b6447-112">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="b6447-113">Если расположение на сервере (включая файлы, к которому они подключены) снова добавляется к той же группе синхронизации, что и конечная точка сервера, это может привести к конфликтным файлам и другим нежелательным последствиям.</span><span class="sxs-lookup"><span data-stu-id="b6447-113">If this server location (incl. it's files) is added again to the same sync group as a server endpoint, it can lead to conflict files and other unintended consequences.</span></span> <span data-ttu-id="b6447-114">Эта команда предназначена только для списания.</span><span class="sxs-lookup"><span data-stu-id="b6447-114">This command is intended for decommissioning only.</span></span>

## <span data-ttu-id="b6447-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b6447-115">EXAMPLES</span></span>

### <span data-ttu-id="b6447-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b6447-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncServerEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"
```

<span data-ttu-id="b6447-117">Эта команда удалит конечную точку сервера.</span><span class="sxs-lookup"><span data-stu-id="b6447-117">This command will remove the server endpoint.</span></span>

## <span data-ttu-id="b6447-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b6447-118">PARAMETERS</span></span>

### <span data-ttu-id="b6447-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6447-119">-AsJob</span></span>
<span data-ttu-id="b6447-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b6447-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b6447-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6447-121">-DefaultProfile</span></span>
<span data-ttu-id="b6447-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b6447-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6447-123">-Force</span><span class="sxs-lookup"><span data-stu-id="b6447-123">-Force</span></span>
<span data-ttu-id="b6447-124">Укажите, чтобы пропустить подтверждение этой команды.</span><span class="sxs-lookup"><span data-stu-id="b6447-124">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="b6447-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6447-125">-InputObject</span></span>
<span data-ttu-id="b6447-126">Входной объект ServerEndpoint, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="b6447-126">ServerEndpoint Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6447-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b6447-127">-Name</span></span>
<span data-ttu-id="b6447-128">Имя ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="b6447-128">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="b6447-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6447-129">-PassThru</span></span>
<span data-ttu-id="b6447-130">При нормальном выполнении этот командлет не возвращает значение в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="b6447-130">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="b6447-131">Если вы предоставляете параметр PassThru, командлет запишет значение в конвейер после успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="b6447-131">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="b6447-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6447-132">-ResourceGroupName</span></span>
<span data-ttu-id="b6447-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b6447-133">Resource Group Name.</span></span>

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

### <span data-ttu-id="b6447-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6447-134">-ResourceId</span></span>
<span data-ttu-id="b6447-135">Идентификатор ресурса ServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b6447-135">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="b6447-136">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="b6447-136">-StorageSyncServiceName</span></span>
<span data-ttu-id="b6447-137">Имя StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="b6447-137">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="b6447-138">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="b6447-138">-SyncGroupName</span></span>
<span data-ttu-id="b6447-139">Имя SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="b6447-139">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="b6447-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6447-140">-Confirm</span></span>
<span data-ttu-id="b6447-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b6447-141">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6447-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6447-142">-WhatIf</span></span>
<span data-ttu-id="b6447-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b6447-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b6447-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b6447-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6447-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6447-145">CommonParameters</span></span>
<span data-ttu-id="b6447-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b6447-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6447-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6447-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6447-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b6447-148">INPUTS</span></span>

### <span data-ttu-id="b6447-149">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b6447-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

### <span data-ttu-id="b6447-150">System. String</span><span class="sxs-lookup"><span data-stu-id="b6447-150">System.String</span></span>

## <span data-ttu-id="b6447-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6447-151">OUTPUTS</span></span>

### <span data-ttu-id="b6447-152">System. Object</span><span class="sxs-lookup"><span data-stu-id="b6447-152">System.Object</span></span>
## <span data-ttu-id="b6447-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="b6447-153">NOTES</span></span>

## <span data-ttu-id="b6447-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b6447-154">RELATED LINKS</span></span>