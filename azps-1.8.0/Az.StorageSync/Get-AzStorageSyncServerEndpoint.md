---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: b71da416d7609f05d4716090dc8f09bf0ec0b084
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728500"
---
# <span data-ttu-id="ead0c-101">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ead0c-101">Get-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="ead0c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ead0c-102">SYNOPSIS</span></span>
<span data-ttu-id="ead0c-103">Эта команда перечисляет все конечные точки сервера в заданной группе синхронизации.</span><span class="sxs-lookup"><span data-stu-id="ead0c-103">This command lists all server endpoints within a given sync group.</span></span>

## <span data-ttu-id="ead0c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ead0c-104">SYNTAX</span></span>

### <span data-ttu-id="ead0c-105">ObjectParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ead0c-105">ObjectParameterSet (Default)</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ead0c-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="ead0c-106">StringParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ead0c-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="ead0c-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ead0c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ead0c-108">DESCRIPTION</span></span>
<span data-ttu-id="ead0c-109">Эта команда перечисляет все конечные точки сервера в заданной группе синхронизации.</span><span class="sxs-lookup"><span data-stu-id="ead0c-109">This command lists all server endpoints within a given sync group.</span></span> <span data-ttu-id="ead0c-110">Также можно использовать для перечисления атрибутов каждой конечной точки сервера.</span><span class="sxs-lookup"><span data-stu-id="ead0c-110">It can be used to also list the attributes of each server endpoint.</span></span>

## <span data-ttu-id="ead0c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ead0c-111">EXAMPLES</span></span>

### <span data-ttu-id="ead0c-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ead0c-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="ead0c-113">Эта команда получает все конечные точки сервера, содержащиеся в указанной группе синхронизации.</span><span class="sxs-lookup"><span data-stu-id="ead0c-113">This command gets all server endpoints contained within the specified sync group.</span></span> <span data-ttu-id="ead0c-114">Укажите-ServerEndpointName, чтобы вернуть определенную единицу.</span><span class="sxs-lookup"><span data-stu-id="ead0c-114">Specify -ServerEndpointName to return a specific one.</span></span>

## <span data-ttu-id="ead0c-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ead0c-115">PARAMETERS</span></span>

### <span data-ttu-id="ead0c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ead0c-116">-DefaultProfile</span></span>
<span data-ttu-id="ead0c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ead0c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ead0c-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ead0c-118">-Name</span></span>
<span data-ttu-id="ead0c-119">Имя конечной точки сервера.</span><span class="sxs-lookup"><span data-stu-id="ead0c-119">Name of the server endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerEndpointName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ead0c-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ead0c-120">-ParentObject</span></span>
<span data-ttu-id="ead0c-121">Объект StorageSyncService, обычно передаваемый через параметр.</span><span class="sxs-lookup"><span data-stu-id="ead0c-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="ead0c-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ead0c-122">-ParentResourceId</span></span>
<span data-ttu-id="ead0c-123">Объект StorageSyncService, обычно передаваемый через параметр.</span><span class="sxs-lookup"><span data-stu-id="ead0c-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="ead0c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ead0c-124">-ResourceGroupName</span></span>
<span data-ttu-id="ead0c-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ead0c-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="ead0c-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="ead0c-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="ead0c-127">Имя StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="ead0c-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="ead0c-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="ead0c-128">-SyncGroupName</span></span>
<span data-ttu-id="ead0c-129">Имя SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="ead0c-129">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="ead0c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ead0c-130">CommonParameters</span></span>
<span data-ttu-id="ead0c-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ead0c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ead0c-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ead0c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ead0c-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ead0c-133">INPUTS</span></span>

### <span data-ttu-id="ead0c-134">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="ead0c-134">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="ead0c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="ead0c-135">System.String</span></span>

## <span data-ttu-id="ead0c-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ead0c-136">OUTPUTS</span></span>

### <span data-ttu-id="ead0c-137">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ead0c-137">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="ead0c-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="ead0c-138">NOTES</span></span>

## <span data-ttu-id="ead0c-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ead0c-139">RELATED LINKS</span></span>
