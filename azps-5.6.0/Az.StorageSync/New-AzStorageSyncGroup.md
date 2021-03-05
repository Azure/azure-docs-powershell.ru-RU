---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/new-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
ms.openlocfilehash: e96b4360247937ace5a0e2894f3bfac19fc1da0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011411"
---
# <span data-ttu-id="eda49-101">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="eda49-101">New-AzStorageSyncGroup</span></span>

## <span data-ttu-id="eda49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eda49-102">SYNOPSIS</span></span>
<span data-ttu-id="eda49-103">Эта команда создает новую группу синхронизации в указанной службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="eda49-103">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="eda49-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="eda49-104">SYNTAX</span></span>

### <span data-ttu-id="eda49-105">StringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="eda49-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eda49-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eda49-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eda49-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="eda49-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eda49-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eda49-108">DESCRIPTION</span></span>
<span data-ttu-id="eda49-109">Эта команда создает новую группу синхронизации в указанной службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="eda49-109">This command creates a new sync group within a specified storage sync service.</span></span> <span data-ttu-id="eda49-110">Группа синхронизации используется для описания топологии местоположений, которые называются конечными точками, и синхронизируются все файлы, хранимые в одной из конечных точек.</span><span class="sxs-lookup"><span data-stu-id="eda49-110">A sync group is used to describe a topology of locations, referred to as endpoints, that will sync any files stored within any one of the endpoints.</span></span> <span data-ttu-id="eda49-111">Группа синхронизации содержит облачные конечные точки, ссылаясь на файловые папки Azure, а также конечные точки сервера, которые ссылаются на определенный локальный путь на зарегистрированном сервере.</span><span class="sxs-lookup"><span data-stu-id="eda49-111">A sync group contains cloud endpoints, which reference Azure file shares, and it also contains server endpoints which reference a specific local path on a registered server.</span></span>

## <span data-ttu-id="eda49-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="eda49-112">EXAMPLES</span></span>

### <span data-ttu-id="eda49-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="eda49-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncGroup -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="eda49-114">Эта команда создает новую группу синхронизации в указанной службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="eda49-114">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="eda49-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eda49-115">PARAMETERS</span></span>

### <span data-ttu-id="eda49-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eda49-116">-DefaultProfile</span></span>
<span data-ttu-id="eda49-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eda49-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eda49-118">-Name</span><span class="sxs-lookup"><span data-stu-id="eda49-118">-Name</span></span>
<span data-ttu-id="eda49-119">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="eda49-119">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="eda49-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="eda49-120">-ParentObject</span></span>
<span data-ttu-id="eda49-121">Объект StorageSyncService, обычно переданный через параметр.</span><span class="sxs-lookup"><span data-stu-id="eda49-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="eda49-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="eda49-122">-ParentResourceId</span></span>
<span data-ttu-id="eda49-123">ИД родительского ресурса StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="eda49-123">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="eda49-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eda49-124">-ResourceGroupName</span></span>
<span data-ttu-id="eda49-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eda49-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="eda49-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="eda49-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="eda49-127">Имя службы StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="eda49-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="eda49-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eda49-128">-Confirm</span></span>
<span data-ttu-id="eda49-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eda49-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eda49-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eda49-130">-WhatIf</span></span>
<span data-ttu-id="eda49-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eda49-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eda49-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="eda49-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eda49-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eda49-133">CommonParameters</span></span>
<span data-ttu-id="eda49-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eda49-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eda49-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eda49-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eda49-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eda49-136">INPUTS</span></span>

### <span data-ttu-id="eda49-137">System.String</span><span class="sxs-lookup"><span data-stu-id="eda49-137">System.String</span></span>

### <span data-ttu-id="eda49-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="eda49-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="eda49-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="eda49-139">OUTPUTS</span></span>

### <span data-ttu-id="eda49-140">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="eda49-140">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="eda49-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="eda49-141">NOTES</span></span>

## <span data-ttu-id="eda49-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eda49-142">RELATED LINKS</span></span>
