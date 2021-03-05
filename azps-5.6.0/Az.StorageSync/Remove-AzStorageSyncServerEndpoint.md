---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/az.storagesync/remove-azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: ed0f21c7a3ad2105073cb81a8dff174d201f96ac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974024"
---
# <span data-ttu-id="aa2b2-101">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="aa2b2-101">Remove-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="aa2b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa2b2-102">SYNOPSIS</span></span>
<span data-ttu-id="aa2b2-103">Эта команда удалит указанную конечную точку сервера.</span><span class="sxs-lookup"><span data-stu-id="aa2b2-103">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="aa2b2-104">Синхронизация с этой расположением остановится немедленно.</span><span class="sxs-lookup"><span data-stu-id="aa2b2-104">Sync to this location will stop immediately.</span></span>

## <span data-ttu-id="aa2b2-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="aa2b2-105">SYNTAX</span></span>

### <span data-ttu-id="aa2b2-106">StringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aa2b2-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa2b2-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa2b2-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa2b2-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa2b2-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa2b2-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa2b2-109">DESCRIPTION</span></span>
<span data-ttu-id="aa2b2-110">Удаление конечной точки сервера является невероятельным действием.</span><span class="sxs-lookup"><span data-stu-id="aa2b2-110">Removing a server endpoint is a destructive operation.</span></span> <span data-ttu-id="aa2b2-111">Это расположение сервера перестанет синхронизироваться.</span><span class="sxs-lookup"><span data-stu-id="aa2b2-111">This server location will stop syncing.</span></span> <span data-ttu-id="aa2b2-112">Эту операцию не следует выполнять для решения проблем с синхронизацией.</span><span class="sxs-lookup"><span data-stu-id="aa2b2-112">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="aa2b2-113">Если это расположение на сервере (incl. it's files) снова добавлено в ту же группу синхронизации, что и конечная точка сервера, это может привести к конфликтам файлов и другим непредвиденным последствиям.</span><span class="sxs-lookup"><span data-stu-id="aa2b2-113">If this server location (incl. it's files) is added again to the same sync group as a server endpoint, it can lead to conflict files and other unintended consequences.</span></span> <span data-ttu-id="aa2b2-114">Эта команда предназначена только для вывода из эксплуатации.</span><span class="sxs-lookup"><span data-stu-id="aa2b2-114">This command is intended for decommissioning only.</span></span>

## <span data-ttu-id="aa2b2-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="aa2b2-115">EXAMPLES</span></span>

### <span data-ttu-id="aa2b2-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="aa2b2-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncServerEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"
```

<span data-ttu-id="aa2b2-117">Эта команда удалит конечную точку сервера.</span><span class="sxs-lookup"><span data-stu-id="aa2b2-117">This command will remove the server endpoint.</span></span>

## <span data-ttu-id="aa2b2-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa2b2-118">PARAMETERS</span></span>

### <span data-ttu-id="aa2b2-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa2b2-119">-AsJob</span></span>
<span data-ttu-id="aa2b2-120">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="aa2b2-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aa2b2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa2b2-121">-DefaultProfile</span></span>
<span data-ttu-id="aa2b2-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aa2b2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa2b2-123">-Force</span><span class="sxs-lookup"><span data-stu-id="aa2b2-123">-Force</span></span>
<span data-ttu-id="aa2b2-124">Необходимо пропустить подтверждение этой команды.</span><span class="sxs-lookup"><span data-stu-id="aa2b2-124">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="aa2b2-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa2b2-125">-InputObject</span></span>
<span data-ttu-id="aa2b2-126">Объект ввода ServerEndpoint, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="aa2b2-126">ServerEndpoint Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="aa2b2-127">-Name</span><span class="sxs-lookup"><span data-stu-id="aa2b2-127">-Name</span></span>
<span data-ttu-id="aa2b2-128">Имя сервераEndpoint.</span><span class="sxs-lookup"><span data-stu-id="aa2b2-128">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="aa2b2-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa2b2-129">-PassThru</span></span>
<span data-ttu-id="aa2b2-130">В обычном выполнении этот cmdlet не возвращает никакого значения для успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="aa2b2-130">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="aa2b2-131">Если задан параметр PassThru, то после успешного выполнения cmdlet напишет значение в конвейер.</span><span class="sxs-lookup"><span data-stu-id="aa2b2-131">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="aa2b2-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa2b2-132">-ResourceGroupName</span></span>
<span data-ttu-id="aa2b2-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aa2b2-133">Resource Group Name.</span></span>

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

### <span data-ttu-id="aa2b2-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa2b2-134">-ResourceId</span></span>
<span data-ttu-id="aa2b2-135">ИД ресурса ServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="aa2b2-135">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="aa2b2-136">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="aa2b2-136">-StorageSyncServiceName</span></span>
<span data-ttu-id="aa2b2-137">Имя службы StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="aa2b2-137">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="aa2b2-138">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="aa2b2-138">-SyncGroupName</span></span>
<span data-ttu-id="aa2b2-139">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="aa2b2-139">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="aa2b2-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa2b2-140">-Confirm</span></span>
<span data-ttu-id="aa2b2-141">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa2b2-141">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa2b2-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa2b2-142">-WhatIf</span></span>
<span data-ttu-id="aa2b2-143">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa2b2-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aa2b2-144">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="aa2b2-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa2b2-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa2b2-145">CommonParameters</span></span>
<span data-ttu-id="aa2b2-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa2b2-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa2b2-147">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa2b2-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa2b2-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aa2b2-148">INPUTS</span></span>

### <span data-ttu-id="aa2b2-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="aa2b2-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

### <span data-ttu-id="aa2b2-150">System.String</span><span class="sxs-lookup"><span data-stu-id="aa2b2-150">System.String</span></span>

## <span data-ttu-id="aa2b2-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="aa2b2-151">OUTPUTS</span></span>

### <span data-ttu-id="aa2b2-152">System.Object</span><span class="sxs-lookup"><span data-stu-id="aa2b2-152">System.Object</span></span>
## <span data-ttu-id="aa2b2-153">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="aa2b2-153">NOTES</span></span>

## <span data-ttu-id="aa2b2-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aa2b2-154">RELATED LINKS</span></span>
