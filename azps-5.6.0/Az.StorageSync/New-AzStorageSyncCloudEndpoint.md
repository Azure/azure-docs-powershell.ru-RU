---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/new-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: c55b49052ae34eba9dfff960c85e9ade7617d2a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011416"
---
# <span data-ttu-id="d24ce-101">New-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="d24ce-101">New-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="d24ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d24ce-102">SYNOPSIS</span></span>
<span data-ttu-id="d24ce-103">Эта команда создает облачную конечную точку синхронизации файлов Azure в группе синхронизации.</span><span class="sxs-lookup"><span data-stu-id="d24ce-103">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

## <span data-ttu-id="d24ce-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d24ce-104">SYNTAX</span></span>

### <span data-ttu-id="d24ce-105">StringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d24ce-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -StorageAccountResourceId <String> -AzureFileShareName <String>
 [-StorageAccountTenantId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d24ce-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d24ce-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d24ce-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="d24ce-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d24ce-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d24ce-108">DESCRIPTION</span></span>
<span data-ttu-id="d24ce-109">Эта команда создает облачную конечную точку синхронизации файлов Azure.</span><span class="sxs-lookup"><span data-stu-id="d24ce-109">This command creates an Azure File Sync cloud endpoint.</span></span> <span data-ttu-id="d24ce-110">Облачная конечная точка — это ссылка на существующую файловую папку Azure.</span><span class="sxs-lookup"><span data-stu-id="d24ce-110">A cloud endpoint is a reference to an existing Azure file share.</span></span> <span data-ttu-id="d24ce-111">Он представляет файловую папку и определяет участие в синхронизации всех файлов в группе синхронизации, в ней была создана конечная точка в облаке.</span><span class="sxs-lookup"><span data-stu-id="d24ce-111">It represents the file share and defines it participation in syncing all the files part of the sync group the cloud endpoint has been created in.</span></span>

## <span data-ttu-id="d24ce-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d24ce-112">EXAMPLES</span></span>

### <span data-ttu-id="d24ce-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d24ce-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName" -StorageAccountResourceId $storageAccountResourceId -AzureFileShareName "myAzureFileShareName" -StorageAccountTenantId "myStorageAccountTenantId"
```

<span data-ttu-id="d24ce-114">Облачная конечная точка интегрирована в группу синхронизации. Это пример создания группы синхронизации mySyncGroupName.</span><span class="sxs-lookup"><span data-stu-id="d24ce-114">A cloud endpoint is an integral member of a sync group, this is an example of creating one inside of an existing sync group called "mySyncGroupName".</span></span>

## <span data-ttu-id="d24ce-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d24ce-115">PARAMETERS</span></span>

### <span data-ttu-id="d24ce-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d24ce-116">-AsJob</span></span>
<span data-ttu-id="d24ce-117">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d24ce-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d24ce-118">-AzureFileShareName</span><span class="sxs-lookup"><span data-stu-id="d24ce-118">-AzureFileShareName</span></span>
<span data-ttu-id="d24ce-119">Имя "Поделиться" учетной записи хранения (имя файла в Azure)</span><span class="sxs-lookup"><span data-stu-id="d24ce-119">Storage Account Share Name (Azure file share name)</span></span>

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

### <span data-ttu-id="d24ce-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d24ce-120">-DefaultProfile</span></span>
<span data-ttu-id="d24ce-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d24ce-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d24ce-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d24ce-122">-Name</span></span>
<span data-ttu-id="d24ce-123">Имя облачной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="d24ce-123">Name of the cloud endpoint.</span></span> <span data-ttu-id="d24ce-124">При его создания на портале Azure для имени создается имя файла, на который он ссылается.</span><span class="sxs-lookup"><span data-stu-id="d24ce-124">When created through the Azure portal, Name is set to the name of the Azure file share it references.</span></span>

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

### <span data-ttu-id="d24ce-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d24ce-125">-ParentObject</span></span>
<span data-ttu-id="d24ce-126">Объект SyncGroup, обычно переданный через параметр.</span><span class="sxs-lookup"><span data-stu-id="d24ce-126">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="d24ce-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d24ce-127">-ParentResourceId</span></span>
<span data-ttu-id="d24ce-128">ИД родительского ресурса SyncGroup</span><span class="sxs-lookup"><span data-stu-id="d24ce-128">SyncGroup Parent Resource Id</span></span>

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

### <span data-ttu-id="d24ce-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d24ce-129">-ResourceGroupName</span></span>
<span data-ttu-id="d24ce-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d24ce-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="d24ce-131">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="d24ce-131">-StorageAccountResourceId</span></span>
<span data-ttu-id="d24ce-132">ИД ресурса учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="d24ce-132">Storage Account Resource Id</span></span>

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

### <span data-ttu-id="d24ce-133">-StorageAccountTenantId</span><span class="sxs-lookup"><span data-stu-id="d24ce-133">-StorageAccountTenantId</span></span>
<span data-ttu-id="d24ce-134">ИД клиента учетной записи хранения (ИД каталога организации)</span><span class="sxs-lookup"><span data-stu-id="d24ce-134">Storage Account Tenant Id (Company Directory Id)</span></span>

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

### <span data-ttu-id="d24ce-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="d24ce-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="d24ce-136">Имя службы StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="d24ce-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="d24ce-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="d24ce-137">-SyncGroupName</span></span>
<span data-ttu-id="d24ce-138">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="d24ce-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="d24ce-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d24ce-139">-Confirm</span></span>
<span data-ttu-id="d24ce-140">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d24ce-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d24ce-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d24ce-141">-WhatIf</span></span>
<span data-ttu-id="d24ce-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d24ce-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d24ce-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d24ce-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d24ce-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d24ce-144">CommonParameters</span></span>
<span data-ttu-id="d24ce-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d24ce-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d24ce-146">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d24ce-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d24ce-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d24ce-147">INPUTS</span></span>

### <span data-ttu-id="d24ce-148">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="d24ce-148">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="d24ce-149">System.String</span><span class="sxs-lookup"><span data-stu-id="d24ce-149">System.String</span></span>

## <span data-ttu-id="d24ce-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d24ce-150">OUTPUTS</span></span>

### <span data-ttu-id="d24ce-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="d24ce-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="d24ce-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d24ce-152">NOTES</span></span>

## <span data-ttu-id="d24ce-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d24ce-153">RELATED LINKS</span></span>
