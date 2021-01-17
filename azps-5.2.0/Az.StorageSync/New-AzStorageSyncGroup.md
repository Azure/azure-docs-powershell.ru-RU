---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
ms.openlocfilehash: fb199887edcc3a9895095101870856d15f86ac08
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414583"
---
# <span data-ttu-id="626fb-101">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="626fb-101">New-AzStorageSyncGroup</span></span>

## <span data-ttu-id="626fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="626fb-102">SYNOPSIS</span></span>
<span data-ttu-id="626fb-103">Эта команда создает новую группу синхронизации в указанной службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="626fb-103">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="626fb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="626fb-104">SYNTAX</span></span>

### <span data-ttu-id="626fb-105">StringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="626fb-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="626fb-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="626fb-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="626fb-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="626fb-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="626fb-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="626fb-108">DESCRIPTION</span></span>
<span data-ttu-id="626fb-109">Эта команда создает новую группу синхронизации в указанной службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="626fb-109">This command creates a new sync group within a specified storage sync service.</span></span> <span data-ttu-id="626fb-110">Группа синхронизации используется для описания топологии местоположений, которые называются конечными точками, и синхронизируются все файлы, хранимые в одной из конечных точек.</span><span class="sxs-lookup"><span data-stu-id="626fb-110">A sync group is used to describe a topology of locations, referred to as endpoints, that will sync any files stored within any one of the endpoints.</span></span> <span data-ttu-id="626fb-111">Группа синхронизации содержит облачные конечные точки, ссылаясь на файловые папки Azure, а также конечные точки сервера, которые ссылаются на определенный локальный путь на зарегистрированном сервере.</span><span class="sxs-lookup"><span data-stu-id="626fb-111">A sync group contains cloud endpoints, which reference Azure file shares, and it also contains server endpoints which reference a specific local path on a registered server.</span></span>

## <span data-ttu-id="626fb-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="626fb-112">EXAMPLES</span></span>

### <span data-ttu-id="626fb-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="626fb-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncGroup -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="626fb-114">Эта команда создает новую группу синхронизации в указанной службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="626fb-114">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="626fb-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="626fb-115">PARAMETERS</span></span>

### <span data-ttu-id="626fb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="626fb-116">-DefaultProfile</span></span>
<span data-ttu-id="626fb-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="626fb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="626fb-118">-Name</span><span class="sxs-lookup"><span data-stu-id="626fb-118">-Name</span></span>
<span data-ttu-id="626fb-119">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="626fb-119">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="626fb-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="626fb-120">-ParentObject</span></span>
<span data-ttu-id="626fb-121">Объект StorageSyncService, обычно переданный через параметр.</span><span class="sxs-lookup"><span data-stu-id="626fb-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="626fb-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="626fb-122">-ParentResourceId</span></span>
<span data-ttu-id="626fb-123">ИД родительского ресурса StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="626fb-123">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="626fb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="626fb-124">-ResourceGroupName</span></span>
<span data-ttu-id="626fb-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="626fb-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="626fb-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="626fb-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="626fb-127">Имя службы StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="626fb-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="626fb-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="626fb-128">-Confirm</span></span>
<span data-ttu-id="626fb-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="626fb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="626fb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="626fb-130">-WhatIf</span></span>
<span data-ttu-id="626fb-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="626fb-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="626fb-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="626fb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="626fb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="626fb-133">CommonParameters</span></span>
<span data-ttu-id="626fb-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="626fb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="626fb-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="626fb-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="626fb-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="626fb-136">INPUTS</span></span>

### <span data-ttu-id="626fb-137">System.String</span><span class="sxs-lookup"><span data-stu-id="626fb-137">System.String</span></span>

### <span data-ttu-id="626fb-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="626fb-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="626fb-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="626fb-139">OUTPUTS</span></span>

### <span data-ttu-id="626fb-140">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="626fb-140">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="626fb-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="626fb-141">NOTES</span></span>

## <span data-ttu-id="626fb-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="626fb-142">RELATED LINKS</span></span>
