---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 076a1393365e93a8008f15137d078a49491d81f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217188"
---
# <span data-ttu-id="1fd04-101">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="1fd04-101">Get-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="1fd04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fd04-102">SYNOPSIS</span></span>
<span data-ttu-id="1fd04-103">Эта команда содержит список всех облачных конечных точек в заданной группе синхронизации.</span><span class="sxs-lookup"><span data-stu-id="1fd04-103">This command lists all cloud endpoints within a given sync group.</span></span>

## <span data-ttu-id="1fd04-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1fd04-104">SYNTAX</span></span>

### <span data-ttu-id="1fd04-105">StringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1fd04-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1fd04-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fd04-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1fd04-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fd04-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1fd04-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fd04-108">DESCRIPTION</span></span>
<span data-ttu-id="1fd04-109">Эта команда содержит список всех облачных конечных точек в заданной группе синхронизации.</span><span class="sxs-lookup"><span data-stu-id="1fd04-109">This command lists all cloud endpoints within a given sync group.</span></span> <span data-ttu-id="1fd04-110">Его также можно использовать для списка атрибутов каждой конечной точки облака.</span><span class="sxs-lookup"><span data-stu-id="1fd04-110">It can be used to also list the attributes of each cloud endpoint.</span></span>

## <span data-ttu-id="1fd04-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1fd04-111">EXAMPLES</span></span>

### <span data-ttu-id="1fd04-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1fd04-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="1fd04-113">Эта команда возвращает все облачные конечные точки, содержащиеся в указанной группе синхронизации.</span><span class="sxs-lookup"><span data-stu-id="1fd04-113">This command gets all cloud endpoints contained within the specified sync group.</span></span> <span data-ttu-id="1fd04-114">Укажите -CloudEndpointName, чтобы вернуть определенное имя.</span><span class="sxs-lookup"><span data-stu-id="1fd04-114">Specify -CloudEndpointName to return a specific one.</span></span>

## <span data-ttu-id="1fd04-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1fd04-115">PARAMETERS</span></span>

### <span data-ttu-id="1fd04-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fd04-116">-DefaultProfile</span></span>
<span data-ttu-id="1fd04-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1fd04-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fd04-118">-Name</span><span class="sxs-lookup"><span data-stu-id="1fd04-118">-Name</span></span>
<span data-ttu-id="1fd04-119">Имя CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="1fd04-119">Name of the CloudEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CloudEndpointName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fd04-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1fd04-120">-ParentObject</span></span>
<span data-ttu-id="1fd04-121">Объект StorageSyncService, обычно переданный через параметр.</span><span class="sxs-lookup"><span data-stu-id="1fd04-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="1fd04-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="1fd04-122">-ParentResourceId</span></span>
<span data-ttu-id="1fd04-123">Объект StorageSyncService, обычно переданный через параметр.</span><span class="sxs-lookup"><span data-stu-id="1fd04-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="1fd04-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fd04-124">-ResourceGroupName</span></span>
<span data-ttu-id="1fd04-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1fd04-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fd04-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="1fd04-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="1fd04-127">Имя службы StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="1fd04-127">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fd04-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="1fd04-128">-SyncGroupName</span></span>
<span data-ttu-id="1fd04-129">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="1fd04-129">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fd04-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fd04-130">CommonParameters</span></span>
<span data-ttu-id="1fd04-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fd04-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fd04-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fd04-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fd04-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1fd04-133">INPUTS</span></span>

### <span data-ttu-id="1fd04-134">System.String</span><span class="sxs-lookup"><span data-stu-id="1fd04-134">System.String</span></span>

### <span data-ttu-id="1fd04-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="1fd04-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="1fd04-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1fd04-136">OUTPUTS</span></span>

### <span data-ttu-id="1fd04-137">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="1fd04-137">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="1fd04-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1fd04-138">NOTES</span></span>

## <span data-ttu-id="1fd04-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1fd04-139">RELATED LINKS</span></span>
