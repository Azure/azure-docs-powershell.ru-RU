---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/invoke-Azstoragesyncfilerecall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
ms.openlocfilehash: 06eb3942a5320ff7c5c8bb3d089ecad2da912edb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907497"
---
# <span data-ttu-id="cb110-101">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="cb110-101">Invoke-AzStorageSyncFileRecall</span></span>

## <span data-ttu-id="cb110-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cb110-102">SYNOPSIS</span></span>
<span data-ttu-id="cb110-103">Эта команда повторно вызывает все многоуровневые файлы на локальный диск.</span><span class="sxs-lookup"><span data-stu-id="cb110-103">This command recalls all tiered files back to local disk.</span></span>

## <span data-ttu-id="cb110-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cb110-104">SYNTAX</span></span>

### <span data-ttu-id="cb110-105">StringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cb110-105">StringParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb110-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb110-106">ResourceIdParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceId] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb110-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb110-107">ObjectParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-InputObject] <PSServerEndpoint> [-Pattern <String>] [-RecallPath <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb110-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb110-108">DESCRIPTION</span></span>
<span data-ttu-id="cb110-109">При включении уровня облака в конечной точке сервера (определенном месте на зарегистрированном сервере) можно использовать эту команду для отзыва всех многоуровневых файлов на локальном диске.</span><span class="sxs-lookup"><span data-stu-id="cb110-109">When cloud tiering is enabled on a server endpoint (a specific location on a registered server) then this command can be used to recall all tiered files to local disk.</span></span> <span data-ttu-id="cb110-110">Перед началом отзыва настоятельно рекомендуется отключить уровень облака в этой конечной точке сервера.</span><span class="sxs-lookup"><span data-stu-id="cb110-110">It is highly recommended to disable cloud tiering on this server endpoint before starting recall.</span></span> <span data-ttu-id="cb110-111">Если уровень по-прежнему включен, отзыв может привести к другим файлам с повышенными разрешениями, чтобы получить необходимую цель всего содержимого на локальном диске.</span><span class="sxs-lookup"><span data-stu-id="cb110-111">If tiering is still on, recall might lead to other files getting tiered which misses to achieve the desired goal of all content residing on local disk.</span></span>

## <span data-ttu-id="cb110-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cb110-112">EXAMPLES</span></span>

### <span data-ttu-id="cb110-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cb110-113">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncFileRecall -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -ServerEndpointName "myServerEndpointName"
```

<span data-ttu-id="cb110-114">Эта команда рекурсивно отзывает все многоуровневые файлы, расположенные в корневом пути указанной конечной точки сервера.</span><span class="sxs-lookup"><span data-stu-id="cb110-114">This command recursively recalls all tiered files located under the root path of the specified server endpoint.</span></span>

## <span data-ttu-id="cb110-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cb110-115">PARAMETERS</span></span>

### <span data-ttu-id="cb110-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb110-116">-AsJob</span></span>
<span data-ttu-id="cb110-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="cb110-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cb110-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb110-118">-DefaultProfile</span></span>
<span data-ttu-id="cb110-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cb110-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb110-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb110-120">-InputObject</span></span>
<span data-ttu-id="cb110-121">Объект SyncGroup, обычно передаваемый через параметр.</span><span class="sxs-lookup"><span data-stu-id="cb110-121">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="cb110-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cb110-122">-Name</span></span>
<span data-ttu-id="cb110-123">Имя ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="cb110-123">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="cb110-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb110-124">-PassThru</span></span>
<span data-ttu-id="cb110-125">При нормальном выполнении этот командлет не возвращает значение в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="cb110-125">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="cb110-126">Если вы предоставляете параметр PassThru, командлет запишет значение в конвейер после успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="cb110-126">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="cb110-127">-Pattern</span><span class="sxs-lookup"><span data-stu-id="cb110-127">-Pattern</span></span>
<span data-ttu-id="cb110-128">Шаблон имени файла</span><span class="sxs-lookup"><span data-stu-id="cb110-128">Pattern of the file name</span></span>

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

### <span data-ttu-id="cb110-129">-RecallPath</span><span class="sxs-lookup"><span data-stu-id="cb110-129">-RecallPath</span></span>
<span data-ttu-id="cb110-130">Отзыв пути, который нужно отозвать.</span><span class="sxs-lookup"><span data-stu-id="cb110-130">Recall path which need to be recalled.</span></span>

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

### <span data-ttu-id="cb110-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb110-131">-ResourceGroupName</span></span>
<span data-ttu-id="cb110-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cb110-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="cb110-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb110-133">-ResourceId</span></span>
<span data-ttu-id="cb110-134">Идентификатор ресурса ServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="cb110-134">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="cb110-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="cb110-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="cb110-136">Имя StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="cb110-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="cb110-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="cb110-137">-SyncGroupName</span></span>
<span data-ttu-id="cb110-138">Имя SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="cb110-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="cb110-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb110-139">-Confirm</span></span>
<span data-ttu-id="cb110-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cb110-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb110-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb110-141">-WhatIf</span></span>
<span data-ttu-id="cb110-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cb110-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cb110-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cb110-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb110-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb110-144">CommonParameters</span></span>
<span data-ttu-id="cb110-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cb110-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb110-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb110-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb110-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cb110-147">INPUTS</span></span>

### <span data-ttu-id="cb110-148">System. String</span><span class="sxs-lookup"><span data-stu-id="cb110-148">System.String</span></span>

### <span data-ttu-id="cb110-149">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="cb110-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="cb110-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb110-150">OUTPUTS</span></span>

### <span data-ttu-id="cb110-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cb110-151">System.Boolean</span></span>

## <span data-ttu-id="cb110-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="cb110-152">NOTES</span></span>

## <span data-ttu-id="cb110-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cb110-153">RELATED LINKS</span></span>
