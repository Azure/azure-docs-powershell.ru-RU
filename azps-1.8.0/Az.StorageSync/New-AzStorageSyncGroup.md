---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
ms.openlocfilehash: 34f4dc1933e755167333d12d4566838ea47c26b1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728488"
---
# <span data-ttu-id="5d314-101">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="5d314-101">New-AzStorageSyncGroup</span></span>

## <span data-ttu-id="5d314-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5d314-102">SYNOPSIS</span></span>
<span data-ttu-id="5d314-103">Эта команда создает новую группу синхронизации в указанной службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="5d314-103">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="5d314-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5d314-104">SYNTAX</span></span>

### <span data-ttu-id="5d314-105">ObjectParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5d314-105">ObjectParameterSet (Default)</span></span>
```
New-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d314-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d314-106">StringParameterSet</span></span>
```
New-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d314-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d314-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5d314-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d314-108">DESCRIPTION</span></span>
<span data-ttu-id="5d314-109">Эта команда создает новую группу синхронизации в указанной службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="5d314-109">This command creates a new sync group within a specified storage sync service.</span></span> <span data-ttu-id="5d314-110">Группа синхронизации используется для описания топологии местоположений, называемой конечными точками, которые будут синхронизировать все файлы, хранящиеся в одной из конечных точек.</span><span class="sxs-lookup"><span data-stu-id="5d314-110">A sync group is used to describe a topology of locations, referred to as endpoints, that will sync any files stored within any one of the endpoints.</span></span> <span data-ttu-id="5d314-111">Группа синхронизации включает облачные конечные точки, которые ссылаются на общие папки Azure и также содержат конечные точки сервера, которые ссылаются на определенный локальный путь на зарегистрированном сервере.</span><span class="sxs-lookup"><span data-stu-id="5d314-111">A sync group contains cloud endpoints, which reference Azure file shares, and it also contains server endpoints which reference a specific local path on a registered server.</span></span>

## <span data-ttu-id="5d314-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5d314-112">EXAMPLES</span></span>

### <span data-ttu-id="5d314-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5d314-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncGroup -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="5d314-114">Эта команда создает новую группу синхронизации в указанной службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="5d314-114">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="5d314-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5d314-115">PARAMETERS</span></span>

### <span data-ttu-id="5d314-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d314-116">-DefaultProfile</span></span>
<span data-ttu-id="5d314-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5d314-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d314-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5d314-118">-Name</span></span>
<span data-ttu-id="5d314-119">Имя SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="5d314-119">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="5d314-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5d314-120">-ParentObject</span></span>
<span data-ttu-id="5d314-121">Объект StorageSyncService, обычно передаваемый через параметр.</span><span class="sxs-lookup"><span data-stu-id="5d314-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="5d314-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5d314-122">-ParentResourceId</span></span>
<span data-ttu-id="5d314-123">Идентификатор родительского ресурса StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="5d314-123">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="5d314-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d314-124">-ResourceGroupName</span></span>
<span data-ttu-id="5d314-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5d314-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="5d314-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="5d314-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="5d314-127">Имя StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="5d314-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="5d314-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d314-128">CommonParameters</span></span>
<span data-ttu-id="5d314-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5d314-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d314-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d314-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d314-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5d314-131">INPUTS</span></span>

### <span data-ttu-id="5d314-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5d314-132">System.String</span></span>

### <span data-ttu-id="5d314-133">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="5d314-133">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="5d314-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d314-134">OUTPUTS</span></span>

### <span data-ttu-id="5d314-135">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="5d314-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="5d314-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="5d314-136">NOTES</span></span>

## <span data-ttu-id="5d314-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5d314-137">RELATED LINKS</span></span>
