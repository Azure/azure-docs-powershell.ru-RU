---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 1f6692067c48cc093e7d74d75c678374aba30f24
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906970"
---
# <span data-ttu-id="07a55-101">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="07a55-101">Get-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="07a55-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="07a55-102">SYNOPSIS</span></span>
<span data-ttu-id="07a55-103">Эта команда перечисляет все конечные точки сервера в заданной группе синхронизации.</span><span class="sxs-lookup"><span data-stu-id="07a55-103">This command lists all server endpoints within a given sync group.</span></span>

## <span data-ttu-id="07a55-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="07a55-104">SYNTAX</span></span>

### <span data-ttu-id="07a55-105">StringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="07a55-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07a55-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="07a55-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07a55-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="07a55-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07a55-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="07a55-108">DESCRIPTION</span></span>
<span data-ttu-id="07a55-109">Эта команда перечисляет все конечные точки сервера в заданной группе синхронизации.</span><span class="sxs-lookup"><span data-stu-id="07a55-109">This command lists all server endpoints within a given sync group.</span></span> <span data-ttu-id="07a55-110">Также можно использовать для перечисления атрибутов каждой конечной точки сервера.</span><span class="sxs-lookup"><span data-stu-id="07a55-110">It can be used to also list the attributes of each server endpoint.</span></span>

## <span data-ttu-id="07a55-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="07a55-111">EXAMPLES</span></span>

### <span data-ttu-id="07a55-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="07a55-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="07a55-113">Эта команда получает все конечные точки сервера, содержащиеся в указанной группе синхронизации.</span><span class="sxs-lookup"><span data-stu-id="07a55-113">This command gets all server endpoints contained within the specified sync group.</span></span> <span data-ttu-id="07a55-114">Укажите-ServerEndpointName, чтобы вернуть определенную единицу.</span><span class="sxs-lookup"><span data-stu-id="07a55-114">Specify -ServerEndpointName to return a specific one.</span></span>

## <span data-ttu-id="07a55-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="07a55-115">PARAMETERS</span></span>

### <span data-ttu-id="07a55-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07a55-116">-DefaultProfile</span></span>
<span data-ttu-id="07a55-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="07a55-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07a55-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="07a55-118">-Name</span></span>
<span data-ttu-id="07a55-119">Имя конечной точки сервера.</span><span class="sxs-lookup"><span data-stu-id="07a55-119">Name of the server endpoint.</span></span>

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

### <span data-ttu-id="07a55-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="07a55-120">-ParentObject</span></span>
<span data-ttu-id="07a55-121">Объект StorageSyncService, обычно передаваемый через параметр.</span><span class="sxs-lookup"><span data-stu-id="07a55-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="07a55-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="07a55-122">-ParentResourceId</span></span>
<span data-ttu-id="07a55-123">Объект StorageSyncService, обычно передаваемый через параметр.</span><span class="sxs-lookup"><span data-stu-id="07a55-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="07a55-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07a55-124">-ResourceGroupName</span></span>
<span data-ttu-id="07a55-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="07a55-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="07a55-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="07a55-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="07a55-127">Имя StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="07a55-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="07a55-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="07a55-128">-SyncGroupName</span></span>
<span data-ttu-id="07a55-129">Имя SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="07a55-129">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="07a55-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07a55-130">CommonParameters</span></span>
<span data-ttu-id="07a55-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="07a55-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07a55-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07a55-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07a55-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="07a55-133">INPUTS</span></span>

### <span data-ttu-id="07a55-134">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="07a55-134">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="07a55-135">System. String</span><span class="sxs-lookup"><span data-stu-id="07a55-135">System.String</span></span>

## <span data-ttu-id="07a55-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="07a55-136">OUTPUTS</span></span>

### <span data-ttu-id="07a55-137">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="07a55-137">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="07a55-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="07a55-138">NOTES</span></span>

## <span data-ttu-id="07a55-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="07a55-139">RELATED LINKS</span></span>
