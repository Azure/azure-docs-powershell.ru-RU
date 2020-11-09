---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/set-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: b8adfd7c069c4215ec8f26d259ed9d1bc39be2d9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249318"
---
# <span data-ttu-id="817ac-101">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="817ac-101">Set-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="817ac-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="817ac-102">SYNOPSIS</span></span>
<span data-ttu-id="817ac-103">Эта команда позволяет вносить изменения в регулируемых параметрах конечной точки сервера.</span><span class="sxs-lookup"><span data-stu-id="817ac-103">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

## <span data-ttu-id="817ac-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="817ac-104">SYNTAX</span></span>

### <span data-ttu-id="817ac-105">StringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="817ac-105">StringParameterSet (Default)</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="817ac-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="817ac-106">ResourceIdParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceId] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="817ac-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="817ac-107">ObjectParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="817ac-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="817ac-108">DESCRIPTION</span></span>
<span data-ttu-id="817ac-109">Эта команда позволяет вносить изменения в регулируемых параметрах конечной точки сервера.</span><span class="sxs-lookup"><span data-stu-id="817ac-109">This command allows for changes on the adjustable parameters of a server endpoint.</span></span> <span data-ttu-id="817ac-110">В любое время можно изменить уровень облака и политики уровней в облаке.</span><span class="sxs-lookup"><span data-stu-id="817ac-110">For instance cloud tiering and cloud tiering policies can be changed at any time.</span></span> <span data-ttu-id="817ac-111">Некоторые аспекты конечной точки сервера, например локальный путь, невозможно изменить после создания конечной точки сервера.</span><span class="sxs-lookup"><span data-stu-id="817ac-111">Several aspects of a server endpoint, such as the local path, cannot be changed after the server endpoint had been created.</span></span>

## <span data-ttu-id="817ac-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="817ac-112">EXAMPLES</span></span>

### <span data-ttu-id="817ac-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="817ac-113">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"  -TierFilesOlderThanDays 30 -OfflineDataTransfer -OfflineDataTransfer $false
```

<span data-ttu-id="817ac-114">В этом примере выполняются два действия: она задает новую политику уровня облака в указанной конечной точке сервера, которая направляет сервер на уровень всех файлов, к которым не обращались в течение последних 30 дней, а также отключает режим автономной передачи данных, который изначально был включен в этой конечной точке сервера при ее создании.</span><span class="sxs-lookup"><span data-stu-id="817ac-114">This example performs two actions, it sets a new cloud tiering policy on the specified server endpoint, which directs the server to tier all files that have not been accessed in the past 30 days and it also disables the offline data transfer mode, which was initially enabled on this server endpoint during it's creation.</span></span> <span data-ttu-id="817ac-115">Автономная передача данных используется как часть взаимодействия со службами массовой миграции, например полем данных Azure.</span><span class="sxs-lookup"><span data-stu-id="817ac-115">Offline data transfer is used as part of interoperability with bulk migration services, such as Azure Data Box.</span></span>

## <span data-ttu-id="817ac-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="817ac-116">PARAMETERS</span></span>

### <span data-ttu-id="817ac-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="817ac-117">-AsJob</span></span>
<span data-ttu-id="817ac-118">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="817ac-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="817ac-119">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="817ac-119">-CloudTiering</span></span>
<span data-ttu-id="817ac-120">Параметр уровня облака</span><span class="sxs-lookup"><span data-stu-id="817ac-120">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="817ac-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="817ac-121">-DefaultProfile</span></span>
<span data-ttu-id="817ac-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="817ac-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="817ac-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="817ac-123">-InputObject</span></span>
<span data-ttu-id="817ac-124">Объект SyncGroup, обычно передаваемый через параметр.</span><span class="sxs-lookup"><span data-stu-id="817ac-124">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="817ac-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="817ac-125">-Name</span></span>
<span data-ttu-id="817ac-126">Имя ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="817ac-126">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="817ac-127">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="817ac-127">-OfflineDataTransfer</span></span>
<span data-ttu-id="817ac-128">Параметр данных, заполненный облаком</span><span class="sxs-lookup"><span data-stu-id="817ac-128">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="817ac-129">-localCacheMode</span><span class="sxs-lookup"><span data-stu-id="817ac-129">-localCacheMode</span></span>
<span data-ttu-id="817ac-130">Параметр режима локального кэша</span><span class="sxs-lookup"><span data-stu-id="817ac-130">Local cache mode Parameter</span></span>

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

### <span data-ttu-id="817ac-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="817ac-131">-ResourceGroupName</span></span>
<span data-ttu-id="817ac-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="817ac-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="817ac-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="817ac-133">-ResourceId</span></span>
<span data-ttu-id="817ac-134">Идентификатор ресурса ServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="817ac-134">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="817ac-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="817ac-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="817ac-136">Имя StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="817ac-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="817ac-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="817ac-137">-SyncGroupName</span></span>
<span data-ttu-id="817ac-138">Имя SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="817ac-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="817ac-139">-TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="817ac-139">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="817ac-140">Уровни файлов, предшествующих дню, с параметрами</span><span class="sxs-lookup"><span data-stu-id="817ac-140">Tier Files Older Than Days Parameter</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="817ac-141">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="817ac-141">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="817ac-142">Параметр процента свободного места в томе</span><span class="sxs-lookup"><span data-stu-id="817ac-142">Volume Free Space Percent Parameter</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="817ac-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="817ac-143">-Confirm</span></span>
<span data-ttu-id="817ac-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="817ac-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="817ac-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="817ac-145">-WhatIf</span></span>
<span data-ttu-id="817ac-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="817ac-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="817ac-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="817ac-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="817ac-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="817ac-148">CommonParameters</span></span>
<span data-ttu-id="817ac-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="817ac-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="817ac-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="817ac-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="817ac-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="817ac-151">INPUTS</span></span>

### <span data-ttu-id="817ac-152">System. String</span><span class="sxs-lookup"><span data-stu-id="817ac-152">System.String</span></span>

### <span data-ttu-id="817ac-153">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="817ac-153">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="817ac-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="817ac-154">OUTPUTS</span></span>

### <span data-ttu-id="817ac-155">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="817ac-155">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="817ac-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="817ac-156">NOTES</span></span>

## <span data-ttu-id="817ac-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="817ac-157">RELATED LINKS</span></span>