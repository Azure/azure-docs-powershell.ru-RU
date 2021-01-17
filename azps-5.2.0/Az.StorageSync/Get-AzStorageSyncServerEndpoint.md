---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 35a3e8c3eecfe8e710addde0eb2080aa20333f0b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414628"
---
# <span data-ttu-id="095ba-101">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="095ba-101">Get-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="095ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="095ba-102">SYNOPSIS</span></span>
<span data-ttu-id="095ba-103">Эта команда содержит список всех конечных точек сервера в заданной группе синхронизации.</span><span class="sxs-lookup"><span data-stu-id="095ba-103">This command lists all server endpoints within a given sync group.</span></span>

## <span data-ttu-id="095ba-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="095ba-104">SYNTAX</span></span>

### <span data-ttu-id="095ba-105">StringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="095ba-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="095ba-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="095ba-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="095ba-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="095ba-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="095ba-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="095ba-108">DESCRIPTION</span></span>
<span data-ttu-id="095ba-109">Эта команда содержит список всех конечных точек сервера в заданной группе синхронизации.</span><span class="sxs-lookup"><span data-stu-id="095ba-109">This command lists all server endpoints within a given sync group.</span></span> <span data-ttu-id="095ba-110">Его также можно использовать для списка атрибутов каждой конечной точки сервера.</span><span class="sxs-lookup"><span data-stu-id="095ba-110">It can be used to also list the attributes of each server endpoint.</span></span>

## <span data-ttu-id="095ba-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="095ba-111">EXAMPLES</span></span>

### <span data-ttu-id="095ba-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="095ba-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="095ba-113">Эта команда возвращает все конечные точки сервера, содержащиеся в указанной группе синхронизации.</span><span class="sxs-lookup"><span data-stu-id="095ba-113">This command gets all server endpoints contained within the specified sync group.</span></span> <span data-ttu-id="095ba-114">Укажите -ServerEndpointName, чтобы вернуть определенное имя.</span><span class="sxs-lookup"><span data-stu-id="095ba-114">Specify -ServerEndpointName to return a specific one.</span></span>

## <span data-ttu-id="095ba-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="095ba-115">PARAMETERS</span></span>

### <span data-ttu-id="095ba-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="095ba-116">-DefaultProfile</span></span>
<span data-ttu-id="095ba-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="095ba-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="095ba-118">-Name</span><span class="sxs-lookup"><span data-stu-id="095ba-118">-Name</span></span>
<span data-ttu-id="095ba-119">Имя конечной точки сервера.</span><span class="sxs-lookup"><span data-stu-id="095ba-119">Name of the server endpoint.</span></span>

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

### <span data-ttu-id="095ba-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="095ba-120">-ParentObject</span></span>
<span data-ttu-id="095ba-121">Объект StorageSyncService, обычно переданный через параметр.</span><span class="sxs-lookup"><span data-stu-id="095ba-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="095ba-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="095ba-122">-ParentResourceId</span></span>
<span data-ttu-id="095ba-123">Объект StorageSyncService, обычно переданный через параметр.</span><span class="sxs-lookup"><span data-stu-id="095ba-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="095ba-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="095ba-124">-ResourceGroupName</span></span>
<span data-ttu-id="095ba-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="095ba-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="095ba-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="095ba-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="095ba-127">Имя службы StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="095ba-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="095ba-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="095ba-128">-SyncGroupName</span></span>
<span data-ttu-id="095ba-129">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="095ba-129">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="095ba-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="095ba-130">CommonParameters</span></span>
<span data-ttu-id="095ba-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="095ba-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="095ba-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="095ba-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="095ba-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="095ba-133">INPUTS</span></span>

### <span data-ttu-id="095ba-134">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="095ba-134">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="095ba-135">System.String</span><span class="sxs-lookup"><span data-stu-id="095ba-135">System.String</span></span>

## <span data-ttu-id="095ba-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="095ba-136">OUTPUTS</span></span>

### <span data-ttu-id="095ba-137">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="095ba-137">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="095ba-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="095ba-138">NOTES</span></span>

## <span data-ttu-id="095ba-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="095ba-139">RELATED LINKS</span></span>
