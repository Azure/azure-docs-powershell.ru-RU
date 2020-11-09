---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 95b30bda3d824fccc5bb40e442697b81b6396d56
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318245"
---
# <span data-ttu-id="8d5bf-101">New-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="8d5bf-101">New-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="8d5bf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8d5bf-102">SYNOPSIS</span></span>
<span data-ttu-id="8d5bf-103">Эта команда создает облачную конечную точку синхронизации файлов Azure в группе синхронизации.</span><span class="sxs-lookup"><span data-stu-id="8d5bf-103">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

## <span data-ttu-id="8d5bf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8d5bf-104">SYNTAX</span></span>

### <span data-ttu-id="8d5bf-105">StringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8d5bf-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -StorageAccountResourceId <String> -AzureFileShareName <String>
 [-StorageAccountTenantId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8d5bf-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d5bf-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d5bf-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d5bf-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d5bf-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d5bf-108">DESCRIPTION</span></span>
<span data-ttu-id="8d5bf-109">Эта команда создает облачную конечную точку синхронизации файлов Azure.</span><span class="sxs-lookup"><span data-stu-id="8d5bf-109">This command creates an Azure File Sync cloud endpoint.</span></span> <span data-ttu-id="8d5bf-110">Конечная точка облака — это ссылка на существующую общую файловую службу Azure.</span><span class="sxs-lookup"><span data-stu-id="8d5bf-110">A cloud endpoint is a reference to an existing Azure file share.</span></span> <span data-ttu-id="8d5bf-111">Она представляет общую файловую точку и определяет участие в синхронизации всех файлов в группе синхронизации, в которой была создана облачная конечная точка.</span><span class="sxs-lookup"><span data-stu-id="8d5bf-111">It represents the file share and defines it participation in syncing all the files part of the sync group the cloud endpoint has been created in.</span></span>

## <span data-ttu-id="8d5bf-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8d5bf-112">EXAMPLES</span></span>

### <span data-ttu-id="8d5bf-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8d5bf-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName" -StorageAccountResourceId $storageAccountResourceId -AzureFileShareName "myAzureFileShareName" -StorageAccountTenantId "myStorageAccountTenantId"
```

<span data-ttu-id="8d5bf-114">Облачная конечная точка является неотъемлемой частью группы синхронизации, это пример создания одной из существующих групп синхронизации с именем "mySyncGroupName".</span><span class="sxs-lookup"><span data-stu-id="8d5bf-114">A cloud endpoint is an integral member of a sync group, this is an example of creating one inside of an existing sync group called "mySyncGroupName".</span></span>

## <span data-ttu-id="8d5bf-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8d5bf-115">PARAMETERS</span></span>

### <span data-ttu-id="8d5bf-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8d5bf-116">-AsJob</span></span>
<span data-ttu-id="8d5bf-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8d5bf-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8d5bf-118">-AzureFileShareName</span><span class="sxs-lookup"><span data-stu-id="8d5bf-118">-AzureFileShareName</span></span>
<span data-ttu-id="8d5bf-119">Имя общего доступа к учетной записи хранения (имя общего файлового файла Azure)</span><span class="sxs-lookup"><span data-stu-id="8d5bf-119">Storage Account Share Name (Azure file share name)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d5bf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d5bf-120">-DefaultProfile</span></span>
<span data-ttu-id="8d5bf-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8d5bf-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d5bf-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8d5bf-122">-Name</span></span>
<span data-ttu-id="8d5bf-123">Имя конечной точки облака.</span><span class="sxs-lookup"><span data-stu-id="8d5bf-123">Name of the cloud endpoint.</span></span> <span data-ttu-id="8d5bf-124">При создании на портале Azure имя задается именем файла Azure, на который ссылается служба общего доступа.</span><span class="sxs-lookup"><span data-stu-id="8d5bf-124">When created through the Azure portal, Name is set to the name of the Azure file share it references.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CloudEndpointName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d5bf-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8d5bf-125">-ParentObject</span></span>
<span data-ttu-id="8d5bf-126">Объект SyncGroup, обычно передаваемый через параметр.</span><span class="sxs-lookup"><span data-stu-id="8d5bf-126">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: ObjectParameterSet
Aliases: SyncGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d5bf-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8d5bf-127">-ParentResourceId</span></span>
<span data-ttu-id="8d5bf-128">Идентификатор родительского ресурса SyncGroup</span><span class="sxs-lookup"><span data-stu-id="8d5bf-128">SyncGroup Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: SyncGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d5bf-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d5bf-129">-ResourceGroupName</span></span>
<span data-ttu-id="8d5bf-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8d5bf-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="8d5bf-131">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="8d5bf-131">-StorageAccountResourceId</span></span>
<span data-ttu-id="8d5bf-132">Идентификатор ресурса учетной записи хранилища</span><span class="sxs-lookup"><span data-stu-id="8d5bf-132">Storage Account Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d5bf-133">-StorageAccountTenantId</span><span class="sxs-lookup"><span data-stu-id="8d5bf-133">-StorageAccountTenantId</span></span>
<span data-ttu-id="8d5bf-134">Идентификатор клиента учетной записи хранилища (код каталога организации)</span><span class="sxs-lookup"><span data-stu-id="8d5bf-134">Storage Account Tenant Id (Company Directory Id)</span></span>

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

### <span data-ttu-id="8d5bf-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="8d5bf-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="8d5bf-136">Имя StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="8d5bf-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="8d5bf-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="8d5bf-137">-SyncGroupName</span></span>
<span data-ttu-id="8d5bf-138">Имя SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="8d5bf-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="8d5bf-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d5bf-139">-Confirm</span></span>
<span data-ttu-id="8d5bf-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8d5bf-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d5bf-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d5bf-141">-WhatIf</span></span>
<span data-ttu-id="8d5bf-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8d5bf-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8d5bf-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8d5bf-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d5bf-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d5bf-144">CommonParameters</span></span>
<span data-ttu-id="8d5bf-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8d5bf-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d5bf-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d5bf-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d5bf-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8d5bf-147">INPUTS</span></span>

### <span data-ttu-id="8d5bf-148">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="8d5bf-148">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="8d5bf-149">System. String</span><span class="sxs-lookup"><span data-stu-id="8d5bf-149">System.String</span></span>

## <span data-ttu-id="8d5bf-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d5bf-150">OUTPUTS</span></span>

### <span data-ttu-id="8d5bf-151">Microsoft. Azure. Commands. StorageSync. Models. PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="8d5bf-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="8d5bf-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="8d5bf-152">NOTES</span></span>

## <span data-ttu-id="8d5bf-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8d5bf-153">RELATED LINKS</span></span>
