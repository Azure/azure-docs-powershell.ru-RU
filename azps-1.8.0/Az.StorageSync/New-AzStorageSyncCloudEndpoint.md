---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 7a8c11bc4b24415e1baf826824596bc06e1fe99a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728494"
---
# <span data-ttu-id="11d96-101">New-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="11d96-101">New-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="11d96-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="11d96-102">SYNOPSIS</span></span>
<span data-ttu-id="11d96-103">Эта команда создает облачную конечную точку синхронизации файлов Azure в группе синхронизации.</span><span class="sxs-lookup"><span data-stu-id="11d96-103">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

## <span data-ttu-id="11d96-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="11d96-104">SYNTAX</span></span>

### <span data-ttu-id="11d96-105">ObjectParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="11d96-105">ObjectParameterSet (Default)</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11d96-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="11d96-106">StringParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -StorageAccountResourceId <String> -AzureFileShareName <String>
 [-StorageAccountTenantId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11d96-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="11d96-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11d96-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="11d96-108">DESCRIPTION</span></span>
<span data-ttu-id="11d96-109">Эта команда создает облачную конечную точку синхронизации файлов Azure.</span><span class="sxs-lookup"><span data-stu-id="11d96-109">This command creates an Azure File Sync cloud endpoint.</span></span> <span data-ttu-id="11d96-110">Конечная точка облака — это ссылка на существующую общую файловую службу Azure.</span><span class="sxs-lookup"><span data-stu-id="11d96-110">A cloud endpoint is a reference to an existing Azure file share.</span></span> <span data-ttu-id="11d96-111">Она представляет общую файловую точку и определяет участие в синхронизации всех файлов в группе синхронизации, в которой была создана облачная конечная точка.</span><span class="sxs-lookup"><span data-stu-id="11d96-111">It represents the file share and defines it participation in syncing all the files part of the sync group the cloud endpoint has been created in.</span></span>

## <span data-ttu-id="11d96-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="11d96-112">EXAMPLES</span></span>

### <span data-ttu-id="11d96-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="11d96-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName" -StorageAccountResourceId $storageAccountResourceId -AzureFileShareName "myAzureFileShareName" -StorageAccountTenantId "myStorageAccountTenantId"
```

<span data-ttu-id="11d96-114">Облачная конечная точка является неотъемлемой частью группы синхронизации, это пример создания одной из существующих групп синхронизации с именем "mySyncGroupName".</span><span class="sxs-lookup"><span data-stu-id="11d96-114">A cloud endpoint is an integral member of a sync group, this is an example of creating one inside of an existing sync group called "mySyncGroupName".</span></span>

## <span data-ttu-id="11d96-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="11d96-115">PARAMETERS</span></span>

### <span data-ttu-id="11d96-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11d96-116">-AsJob</span></span>
<span data-ttu-id="11d96-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="11d96-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="11d96-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11d96-118">-DefaultProfile</span></span>
<span data-ttu-id="11d96-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="11d96-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11d96-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="11d96-120">-Name</span></span>
<span data-ttu-id="11d96-121">Имя конечной точки облака.</span><span class="sxs-lookup"><span data-stu-id="11d96-121">Name of the cloud endpoint.</span></span> <span data-ttu-id="11d96-122">При создании на портале Azure имя задается именем файла Azure, на который ссылается служба общего доступа.</span><span class="sxs-lookup"><span data-stu-id="11d96-122">When created through the Azure portal, Name is set to the name of the Azure file share it references.</span></span>

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

### <span data-ttu-id="11d96-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="11d96-123">-ParentObject</span></span>
<span data-ttu-id="11d96-124">Объект SyncGroup, обычно передаваемый через параметр.</span><span class="sxs-lookup"><span data-stu-id="11d96-124">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="11d96-125">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="11d96-125">-ParentResourceId</span></span>
<span data-ttu-id="11d96-126">Идентификатор родительского ресурса SyncGroup</span><span class="sxs-lookup"><span data-stu-id="11d96-126">SyncGroup Parent Resource Id</span></span>

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

### <span data-ttu-id="11d96-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11d96-127">-ResourceGroupName</span></span>
<span data-ttu-id="11d96-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="11d96-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="11d96-129">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="11d96-129">-StorageAccountResourceId</span></span>
<span data-ttu-id="11d96-130">Идентификатор ресурса учетной записи хранилища</span><span class="sxs-lookup"><span data-stu-id="11d96-130">Storage Account Resource Id</span></span>

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

### <span data-ttu-id="11d96-131">-AzureFileShareName</span><span class="sxs-lookup"><span data-stu-id="11d96-131">-AzureFileShareName</span></span>
<span data-ttu-id="11d96-132">Имя общего доступа к учетной записи хранения (имя общего файлового файла Azure)</span><span class="sxs-lookup"><span data-stu-id="11d96-132">Storage Account Share Name (Azure file share name)</span></span>

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

### <span data-ttu-id="11d96-133">-StorageAccountTenantId</span><span class="sxs-lookup"><span data-stu-id="11d96-133">-StorageAccountTenantId</span></span>
<span data-ttu-id="11d96-134">Идентификатор клиента учетной записи хранилища (код каталога организации)</span><span class="sxs-lookup"><span data-stu-id="11d96-134">Storage Account Tenant Id (Company Directory Id)</span></span>

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

### <span data-ttu-id="11d96-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="11d96-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="11d96-136">Имя StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="11d96-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="11d96-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="11d96-137">-SyncGroupName</span></span>
<span data-ttu-id="11d96-138">Имя SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="11d96-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="11d96-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11d96-139">-Confirm</span></span>
<span data-ttu-id="11d96-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="11d96-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11d96-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11d96-141">-WhatIf</span></span>
<span data-ttu-id="11d96-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="11d96-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="11d96-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="11d96-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11d96-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11d96-144">CommonParameters</span></span>
<span data-ttu-id="11d96-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="11d96-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11d96-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11d96-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11d96-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="11d96-147">INPUTS</span></span>

### <span data-ttu-id="11d96-148">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="11d96-148">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="11d96-149">System. String</span><span class="sxs-lookup"><span data-stu-id="11d96-149">System.String</span></span>

## <span data-ttu-id="11d96-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="11d96-150">OUTPUTS</span></span>

### <span data-ttu-id="11d96-151">Microsoft. Azure. Commands. StorageSync. Models. PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="11d96-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="11d96-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="11d96-152">NOTES</span></span>

## <span data-ttu-id="11d96-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="11d96-153">RELATED LINKS</span></span>
