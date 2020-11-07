---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 328fd4c798380202b355974cc8d9150e1d138da5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728483"
---
# <span data-ttu-id="457f1-101">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="457f1-101">Remove-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="457f1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="457f1-102">SYNOPSIS</span></span>
<span data-ttu-id="457f1-103">Эта команда удалит указанную конечную точку сервера.</span><span class="sxs-lookup"><span data-stu-id="457f1-103">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="457f1-104">Синхронизация с этим расположением будет немедленно остановлена.</span><span class="sxs-lookup"><span data-stu-id="457f1-104">Sync to this location will stop immediately.</span></span>

## <span data-ttu-id="457f1-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="457f1-105">SYNTAX</span></span>

### <span data-ttu-id="457f1-106">StringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="457f1-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="457f1-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="457f1-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="457f1-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="457f1-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="457f1-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="457f1-109">DESCRIPTION</span></span>
<span data-ttu-id="457f1-110">Удаление конечной точки сервера является разрушительной операцией.</span><span class="sxs-lookup"><span data-stu-id="457f1-110">Removing a server endpoint is a destructive operation.</span></span> <span data-ttu-id="457f1-111">Это расположение на сервере прекратит синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="457f1-111">This server location will stop syncing.</span></span> <span data-ttu-id="457f1-112">Эта операция не должна выполняться для решения проблем с синхронизацией.</span><span class="sxs-lookup"><span data-stu-id="457f1-112">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="457f1-113">Если расположение на сервере (включая файлы, к которому они подключены) снова добавляется к той же группе синхронизации, что и конечная точка сервера, это может привести к конфликтным файлам и другим нежелательным последствиям.</span><span class="sxs-lookup"><span data-stu-id="457f1-113">If this server location (incl. it's files) is added again to the same sync group as a server endpoint, it can lead to conflict files and other unintended consequences.</span></span> <span data-ttu-id="457f1-114">Эта команда предназначена только для списания.</span><span class="sxs-lookup"><span data-stu-id="457f1-114">This command is intended for decommissioning only.</span></span>

## <span data-ttu-id="457f1-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="457f1-115">EXAMPLES</span></span>

### <span data-ttu-id="457f1-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="457f1-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncServerEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"
```

<span data-ttu-id="457f1-117">Эта команда удалит конечную точку сервера.</span><span class="sxs-lookup"><span data-stu-id="457f1-117">This command will remove the server endpoint.</span></span>

## <span data-ttu-id="457f1-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="457f1-118">PARAMETERS</span></span>

### <span data-ttu-id="457f1-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="457f1-119">-AsJob</span></span>
<span data-ttu-id="457f1-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="457f1-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="457f1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="457f1-121">-DefaultProfile</span></span>
<span data-ttu-id="457f1-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="457f1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="457f1-123">-Force</span><span class="sxs-lookup"><span data-stu-id="457f1-123">-Force</span></span>
<span data-ttu-id="457f1-124">Укажите, чтобы пропустить подтверждение этой команды.</span><span class="sxs-lookup"><span data-stu-id="457f1-124">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="457f1-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="457f1-125">-InputObject</span></span>
<span data-ttu-id="457f1-126">Входной объект ServerEndpoint, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="457f1-126">ServerEndpoint Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="457f1-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="457f1-127">-Name</span></span>
<span data-ttu-id="457f1-128">Имя ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="457f1-128">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="457f1-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="457f1-129">-PassThru</span></span>
<span data-ttu-id="457f1-130">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="457f1-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="457f1-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="457f1-131">-ResourceGroupName</span></span>
<span data-ttu-id="457f1-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="457f1-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="457f1-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="457f1-133">-ResourceId</span></span>
<span data-ttu-id="457f1-134">Идентификатор ресурса ServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="457f1-134">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="457f1-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="457f1-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="457f1-136">Имя StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="457f1-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="457f1-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="457f1-137">-SyncGroupName</span></span>
<span data-ttu-id="457f1-138">Имя SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="457f1-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="457f1-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="457f1-139">-Confirm</span></span>
<span data-ttu-id="457f1-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="457f1-140">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="457f1-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="457f1-141">-WhatIf</span></span>
<span data-ttu-id="457f1-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="457f1-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="457f1-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="457f1-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="457f1-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="457f1-144">CommonParameters</span></span>
<span data-ttu-id="457f1-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="457f1-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="457f1-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="457f1-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="457f1-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="457f1-147">INPUTS</span></span>

### <span data-ttu-id="457f1-148">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="457f1-148">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

### <span data-ttu-id="457f1-149">System. String</span><span class="sxs-lookup"><span data-stu-id="457f1-149">System.String</span></span>

## <span data-ttu-id="457f1-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="457f1-150">OUTPUTS</span></span>

### <span data-ttu-id="457f1-151">System. Object</span><span class="sxs-lookup"><span data-stu-id="457f1-151">System.Object</span></span>
## <span data-ttu-id="457f1-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="457f1-152">NOTES</span></span>

## <span data-ttu-id="457f1-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="457f1-153">RELATED LINKS</span></span>
