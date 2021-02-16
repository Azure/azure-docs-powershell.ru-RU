---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/invoke-Azstoragesyncfilerecall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
ms.openlocfilehash: fb053da61aabd9328f4ff3d848243ff9b84d6d09
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229737"
---
# <span data-ttu-id="e05b8-101">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="e05b8-101">Invoke-AzStorageSyncFileRecall</span></span>

## <span data-ttu-id="e05b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e05b8-102">SYNOPSIS</span></span>
<span data-ttu-id="e05b8-103">Эта команда отзывит все многоуровневые файлы на локальный диск.</span><span class="sxs-lookup"><span data-stu-id="e05b8-103">This command recalls all tiered files back to local disk.</span></span>

## <span data-ttu-id="e05b8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e05b8-104">SYNTAX</span></span>

### <span data-ttu-id="e05b8-105">StringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e05b8-105">StringParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e05b8-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e05b8-106">ResourceIdParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceId] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e05b8-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e05b8-107">ObjectParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-InputObject] <PSServerEndpoint> [-Pattern <String>] [-RecallPath <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e05b8-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e05b8-108">DESCRIPTION</span></span>
<span data-ttu-id="e05b8-109">Если на сервере (определенном расположении на зарегистрированном сервере) включено облачное многоуровневое размещение, эту команду можно использовать для отзыва всех многоуровневых файлов на локальный диск.</span><span class="sxs-lookup"><span data-stu-id="e05b8-109">When cloud tiering is enabled on a server endpoint (a specific location on a registered server) then this command can be used to recall all tiered files to local disk.</span></span> <span data-ttu-id="e05b8-110">Перед отзывом настоятельно рекомендуется отключить многоуровневый уровень облака на этой конечной точке сервера.</span><span class="sxs-lookup"><span data-stu-id="e05b8-110">It is highly recommended to disable cloud tiering on this server endpoint before starting recall.</span></span> <span data-ttu-id="e05b8-111">Если это не по-прежнему происходит, отзыв может привести к переупополнение других файлов, из-за чего не получается достичь нужной цели для всего содержимого, которое находится на локальном диске.</span><span class="sxs-lookup"><span data-stu-id="e05b8-111">If tiering is still on, recall might lead to other files getting tiered which misses to achieve the desired goal of all content residing on local disk.</span></span>

## <span data-ttu-id="e05b8-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e05b8-112">EXAMPLES</span></span>

### <span data-ttu-id="e05b8-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e05b8-113">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncFileRecall -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -ServerEndpointName "myServerEndpointName"
```

<span data-ttu-id="e05b8-114">Эта команда рекурсивно отзывает все многоуровневые файлы, расположенные в корневом пути к указанной конечной точке сервера.</span><span class="sxs-lookup"><span data-stu-id="e05b8-114">This command recursively recalls all tiered files located under the root path of the specified server endpoint.</span></span>

## <span data-ttu-id="e05b8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e05b8-115">PARAMETERS</span></span>

### <span data-ttu-id="e05b8-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e05b8-116">-AsJob</span></span>
<span data-ttu-id="e05b8-117">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e05b8-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e05b8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e05b8-118">-DefaultProfile</span></span>
<span data-ttu-id="e05b8-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e05b8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e05b8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e05b8-120">-InputObject</span></span>
<span data-ttu-id="e05b8-121">Объект SyncGroup, обычно переданный через параметр.</span><span class="sxs-lookup"><span data-stu-id="e05b8-121">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: ObjectParameterSet
Aliases: RegisteredServer, ServerEndpoint

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e05b8-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e05b8-122">-Name</span></span>
<span data-ttu-id="e05b8-123">Имя сервераEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e05b8-123">Name of the ServerEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ServerEndpointName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e05b8-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e05b8-124">-PassThru</span></span>
<span data-ttu-id="e05b8-125">В обычном выполнении этот cmdlet не возвращает никакого значения для успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="e05b8-125">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="e05b8-126">Если для параметра PassThru задан параметр PassThru, после успешного выполнения он будет записывать значение в конвейер.</span><span class="sxs-lookup"><span data-stu-id="e05b8-126">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="e05b8-127">-Pattern</span><span class="sxs-lookup"><span data-stu-id="e05b8-127">-Pattern</span></span>
<span data-ttu-id="e05b8-128">Шаблон имени файла</span><span class="sxs-lookup"><span data-stu-id="e05b8-128">Pattern of the file name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e05b8-129">-RecallPath</span><span class="sxs-lookup"><span data-stu-id="e05b8-129">-RecallPath</span></span>
<span data-ttu-id="e05b8-130">Путь отзыва, который необходимо отозвать.</span><span class="sxs-lookup"><span data-stu-id="e05b8-130">Recall path which need to be recalled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e05b8-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e05b8-131">-ResourceGroupName</span></span>
<span data-ttu-id="e05b8-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e05b8-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="e05b8-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e05b8-133">-ResourceId</span></span>
<span data-ttu-id="e05b8-134">ИД ресурса ServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e05b8-134">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="e05b8-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="e05b8-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="e05b8-136">Имя службы StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="e05b8-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="e05b8-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="e05b8-137">-SyncGroupName</span></span>
<span data-ttu-id="e05b8-138">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="e05b8-138">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e05b8-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e05b8-139">-Confirm</span></span>
<span data-ttu-id="e05b8-140">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e05b8-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e05b8-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e05b8-141">-WhatIf</span></span>
<span data-ttu-id="e05b8-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e05b8-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e05b8-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e05b8-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e05b8-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e05b8-144">CommonParameters</span></span>
<span data-ttu-id="e05b8-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e05b8-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e05b8-146">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e05b8-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e05b8-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e05b8-147">INPUTS</span></span>

### <span data-ttu-id="e05b8-148">System.String</span><span class="sxs-lookup"><span data-stu-id="e05b8-148">System.String</span></span>

### <span data-ttu-id="e05b8-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e05b8-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="e05b8-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e05b8-150">OUTPUTS</span></span>

### <span data-ttu-id="e05b8-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e05b8-151">System.Boolean</span></span>

## <span data-ttu-id="e05b8-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e05b8-152">NOTES</span></span>

## <span data-ttu-id="e05b8-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e05b8-153">RELATED LINKS</span></span>
