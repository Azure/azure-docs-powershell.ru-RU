---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
ms.openlocfilehash: fb199887edcc3a9895095101870856d15f86ac08
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243782"
---
# <span data-ttu-id="5fef9-101">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="5fef9-101">New-AzStorageSyncGroup</span></span>

## <span data-ttu-id="5fef9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5fef9-102">SYNOPSIS</span></span>
<span data-ttu-id="5fef9-103">Эта команда создает новую группу синхронизации в указанной службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="5fef9-103">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="5fef9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5fef9-104">SYNTAX</span></span>

### <span data-ttu-id="5fef9-105">StringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5fef9-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fef9-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5fef9-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fef9-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="5fef9-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fef9-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5fef9-108">DESCRIPTION</span></span>
<span data-ttu-id="5fef9-109">Эта команда создает новую группу синхронизации в указанной службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="5fef9-109">This command creates a new sync group within a specified storage sync service.</span></span> <span data-ttu-id="5fef9-110">Группа синхронизации используется для описания топологии местоположений, называемой конечными точками, которые будут синхронизировать все файлы, хранящиеся в одной из конечных точек.</span><span class="sxs-lookup"><span data-stu-id="5fef9-110">A sync group is used to describe a topology of locations, referred to as endpoints, that will sync any files stored within any one of the endpoints.</span></span> <span data-ttu-id="5fef9-111">Группа синхронизации включает облачные конечные точки, которые ссылаются на общие папки Azure и также содержат конечные точки сервера, которые ссылаются на определенный локальный путь на зарегистрированном сервере.</span><span class="sxs-lookup"><span data-stu-id="5fef9-111">A sync group contains cloud endpoints, which reference Azure file shares, and it also contains server endpoints which reference a specific local path on a registered server.</span></span>

## <span data-ttu-id="5fef9-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5fef9-112">EXAMPLES</span></span>

### <span data-ttu-id="5fef9-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5fef9-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncGroup -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="5fef9-114">Эта команда создает новую группу синхронизации в указанной службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="5fef9-114">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="5fef9-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5fef9-115">PARAMETERS</span></span>

### <span data-ttu-id="5fef9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fef9-116">-DefaultProfile</span></span>
<span data-ttu-id="5fef9-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5fef9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fef9-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5fef9-118">-Name</span></span>
<span data-ttu-id="5fef9-119">Имя SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="5fef9-119">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="5fef9-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5fef9-120">-ParentObject</span></span>
<span data-ttu-id="5fef9-121">Объект StorageSyncService, обычно передаваемый через параметр.</span><span class="sxs-lookup"><span data-stu-id="5fef9-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="5fef9-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5fef9-122">-ParentResourceId</span></span>
<span data-ttu-id="5fef9-123">Идентификатор родительского ресурса StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="5fef9-123">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="5fef9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fef9-124">-ResourceGroupName</span></span>
<span data-ttu-id="5fef9-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5fef9-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="5fef9-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="5fef9-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="5fef9-127">Имя StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="5fef9-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="5fef9-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5fef9-128">-Confirm</span></span>
<span data-ttu-id="5fef9-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5fef9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fef9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fef9-130">-WhatIf</span></span>
<span data-ttu-id="5fef9-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5fef9-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5fef9-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5fef9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fef9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fef9-133">CommonParameters</span></span>
<span data-ttu-id="5fef9-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5fef9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fef9-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fef9-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fef9-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5fef9-136">INPUTS</span></span>

### <span data-ttu-id="5fef9-137">System. String</span><span class="sxs-lookup"><span data-stu-id="5fef9-137">System.String</span></span>

### <span data-ttu-id="5fef9-138">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="5fef9-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="5fef9-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5fef9-139">OUTPUTS</span></span>

### <span data-ttu-id="5fef9-140">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="5fef9-140">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="5fef9-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="5fef9-141">NOTES</span></span>

## <span data-ttu-id="5fef9-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5fef9-142">RELATED LINKS</span></span>
