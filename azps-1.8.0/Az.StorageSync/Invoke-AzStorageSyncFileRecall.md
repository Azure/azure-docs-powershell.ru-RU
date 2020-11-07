---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/invoke-Azstoragesyncfilerecall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
ms.openlocfilehash: 5463c20274f60c2d6fb6c4807bf2c4d27da76808
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728493"
---
# <span data-ttu-id="534e2-101">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="534e2-101">Invoke-AzStorageSyncFileRecall</span></span>

## <span data-ttu-id="534e2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="534e2-102">SYNOPSIS</span></span>
<span data-ttu-id="534e2-103">Эта команда повторно вызывает все многоуровневые файлы на локальный диск.</span><span class="sxs-lookup"><span data-stu-id="534e2-103">This command recalls all tiered files back to local disk.</span></span>

## <span data-ttu-id="534e2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="534e2-104">SYNTAX</span></span>

### <span data-ttu-id="534e2-105">ObjectParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="534e2-105">ObjectParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncFileRecall [-InputObject] <PSServerEndpoint> [-Pattern <String>] [-RecallPath <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="534e2-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="534e2-106">StringParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="534e2-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="534e2-107">ResourceIdParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceId] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="534e2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="534e2-108">DESCRIPTION</span></span>
<span data-ttu-id="534e2-109">При включении уровня облака в конечной точке сервера (определенном месте на зарегистрированном сервере) можно использовать эту команду для отзыва всех многоуровневых файлов на локальном диске.</span><span class="sxs-lookup"><span data-stu-id="534e2-109">When cloud tiering is enabled on a server endpoint (a specific location on a registered server) then this command can be used to recall all tiered files to local disk.</span></span> <span data-ttu-id="534e2-110">Перед началом отзыва настоятельно рекомендуется отключить уровень облака в этой конечной точке сервера.</span><span class="sxs-lookup"><span data-stu-id="534e2-110">It is highly recommended to disable cloud tiering on this server endpoint before starting recall.</span></span> <span data-ttu-id="534e2-111">Если уровень по-прежнему включен, отзыв может привести к другим файлам с повышенными разрешениями, чтобы получить необходимую цель всего содержимого на локальном диске.</span><span class="sxs-lookup"><span data-stu-id="534e2-111">If tiering is still on, recall might lead to other files getting tiered which misses to achieve the desired goal of all content residing on local disk.</span></span>

## <span data-ttu-id="534e2-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="534e2-112">EXAMPLES</span></span>

### <span data-ttu-id="534e2-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="534e2-113">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncFileRecall -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -ServerEndpointName "myServerEndpointName"
```

<span data-ttu-id="534e2-114">Эта команда рекурсивно отзывает все многоуровневые файлы, расположенные в корневом пути указанной конечной точки сервера.</span><span class="sxs-lookup"><span data-stu-id="534e2-114">This command recursively recalls all tiered files located under the root path of the specified server endpoint.</span></span>

## <span data-ttu-id="534e2-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="534e2-115">PARAMETERS</span></span>

### <span data-ttu-id="534e2-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="534e2-116">-AsJob</span></span>
<span data-ttu-id="534e2-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="534e2-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="534e2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="534e2-118">-DefaultProfile</span></span>
<span data-ttu-id="534e2-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="534e2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="534e2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="534e2-120">-InputObject</span></span>
<span data-ttu-id="534e2-121">Объект SyncGroup, обычно передаваемый через параметр.</span><span class="sxs-lookup"><span data-stu-id="534e2-121">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: ObjectParameterSet
Aliases: RegisteredServer

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="534e2-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="534e2-122">-Name</span></span>
<span data-ttu-id="534e2-123">Имя ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="534e2-123">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="534e2-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="534e2-124">-PassThru</span></span>
<span data-ttu-id="534e2-125">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="534e2-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="534e2-126">-Pattern</span><span class="sxs-lookup"><span data-stu-id="534e2-126">-Pattern</span></span>
<span data-ttu-id="534e2-127">Шаблон имени файла</span><span class="sxs-lookup"><span data-stu-id="534e2-127">Pattern of the file name</span></span>

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

### <span data-ttu-id="534e2-128">-RecallPath</span><span class="sxs-lookup"><span data-stu-id="534e2-128">-RecallPath</span></span>
<span data-ttu-id="534e2-129">Отзыв пути, который нужно отозвать.</span><span class="sxs-lookup"><span data-stu-id="534e2-129">Recall path which need to be recalled.</span></span>

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

### <span data-ttu-id="534e2-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="534e2-130">-ResourceGroupName</span></span>
<span data-ttu-id="534e2-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="534e2-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="534e2-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="534e2-132">-ResourceId</span></span>
<span data-ttu-id="534e2-133">Идентификатор ресурса ServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="534e2-133">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="534e2-134">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="534e2-134">-StorageSyncServiceName</span></span>
<span data-ttu-id="534e2-135">Имя StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="534e2-135">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="534e2-136">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="534e2-136">-SyncGroupName</span></span>
<span data-ttu-id="534e2-137">Имя SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="534e2-137">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="534e2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="534e2-138">CommonParameters</span></span>
<span data-ttu-id="534e2-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="534e2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="534e2-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="534e2-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="534e2-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="534e2-141">INPUTS</span></span>

### <span data-ttu-id="534e2-142">System. String</span><span class="sxs-lookup"><span data-stu-id="534e2-142">System.String</span></span>

### <span data-ttu-id="534e2-143">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="534e2-143">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="534e2-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="534e2-144">OUTPUTS</span></span>

### <span data-ttu-id="534e2-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="534e2-145">System.Boolean</span></span>

## <span data-ttu-id="534e2-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="534e2-146">NOTES</span></span>

## <span data-ttu-id="534e2-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="534e2-147">RELATED LINKS</span></span>
