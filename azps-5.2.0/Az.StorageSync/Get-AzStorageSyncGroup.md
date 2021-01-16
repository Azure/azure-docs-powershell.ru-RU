---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
ms.openlocfilehash: b59d5dd1ca094d4b4d5eed276957f07b7d34f1f2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392255"
---
# <span data-ttu-id="6cbc8-101">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="6cbc8-101">Get-AzStorageSyncGroup</span></span>

## <span data-ttu-id="6cbc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cbc8-102">SYNOPSIS</span></span>
<span data-ttu-id="6cbc8-103">Эта команда содержит список всех групп синхронизации в заданной службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="6cbc8-103">This command lists all sync groups within a given storage sync service.</span></span>

## <span data-ttu-id="6cbc8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6cbc8-104">SYNTAX</span></span>

### <span data-ttu-id="6cbc8-105">StringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6cbc8-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6cbc8-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cbc8-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6cbc8-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cbc8-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6cbc8-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6cbc8-108">DESCRIPTION</span></span>
<span data-ttu-id="6cbc8-109">Эта команда содержит список всех групп синхронизации в заданной службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="6cbc8-109">This command lists all sync groups within a given storage sync service.</span></span> <span data-ttu-id="6cbc8-110">Его также можно использовать для списка атрибутов каждой группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="6cbc8-110">It can be used to also list the attributes of each sync group.</span></span>

## <span data-ttu-id="6cbc8-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6cbc8-111">EXAMPLES</span></span>

### <span data-ttu-id="6cbc8-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6cbc8-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncGroup New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="6cbc8-113">Эта команда возвращает все группы синхронизации, содержащиеся в указанной службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="6cbc8-113">This command gets all sync groups contained within the specified storage sync service.</span></span> <span data-ttu-id="6cbc8-114">Укажите -Имя, чтобы вернуть определенное имя.</span><span class="sxs-lookup"><span data-stu-id="6cbc8-114">Specify -Name to return a specific one.</span></span>

## <span data-ttu-id="6cbc8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6cbc8-115">PARAMETERS</span></span>

### <span data-ttu-id="6cbc8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cbc8-116">-DefaultProfile</span></span>
<span data-ttu-id="6cbc8-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6cbc8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cbc8-118">-Name</span><span class="sxs-lookup"><span data-stu-id="6cbc8-118">-Name</span></span>
<span data-ttu-id="6cbc8-119">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="6cbc8-119">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cbc8-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6cbc8-120">-ParentObject</span></span>
<span data-ttu-id="6cbc8-121">Объект StorageSyncService, обычно переданный через параметр.</span><span class="sxs-lookup"><span data-stu-id="6cbc8-121">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: ObjectParameterSet
Aliases: StorageSyncService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6cbc8-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6cbc8-122">-ParentResourceId</span></span>
<span data-ttu-id="6cbc8-123">Объект StorageSyncService, обычно переданный через параметр.</span><span class="sxs-lookup"><span data-stu-id="6cbc8-123">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: StorageSyncServiceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cbc8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cbc8-124">-ResourceGroupName</span></span>
<span data-ttu-id="6cbc8-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6cbc8-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="6cbc8-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="6cbc8-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="6cbc8-127">Имя службы StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="6cbc8-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="6cbc8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cbc8-128">CommonParameters</span></span>
<span data-ttu-id="6cbc8-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cbc8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cbc8-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cbc8-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cbc8-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6cbc8-131">INPUTS</span></span>

### <span data-ttu-id="6cbc8-132">System.String</span><span class="sxs-lookup"><span data-stu-id="6cbc8-132">System.String</span></span>

### <span data-ttu-id="6cbc8-133">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="6cbc8-133">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="6cbc8-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6cbc8-134">OUTPUTS</span></span>

### <span data-ttu-id="6cbc8-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="6cbc8-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="6cbc8-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6cbc8-136">NOTES</span></span>

## <span data-ttu-id="6cbc8-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6cbc8-137">RELATED LINKS</span></span>
