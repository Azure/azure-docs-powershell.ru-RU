---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
ms.openlocfilehash: b59d5dd1ca094d4b4d5eed276957f07b7d34f1f2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235215"
---
# <span data-ttu-id="bfc49-101">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="bfc49-101">Get-AzStorageSyncGroup</span></span>

## <span data-ttu-id="bfc49-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bfc49-102">SYNOPSIS</span></span>
<span data-ttu-id="bfc49-103">Эта команда выводит список всех групп синхронизации в заданной службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="bfc49-103">This command lists all sync groups within a given storage sync service.</span></span>

## <span data-ttu-id="bfc49-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bfc49-104">SYNTAX</span></span>

### <span data-ttu-id="bfc49-105">StringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bfc49-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfc49-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfc49-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfc49-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfc49-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bfc49-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bfc49-108">DESCRIPTION</span></span>
<span data-ttu-id="bfc49-109">Эта команда выводит список всех групп синхронизации в заданной службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="bfc49-109">This command lists all sync groups within a given storage sync service.</span></span> <span data-ttu-id="bfc49-110">Также можно использовать для перечисления атрибутов каждой из групп синхронизации.</span><span class="sxs-lookup"><span data-stu-id="bfc49-110">It can be used to also list the attributes of each sync group.</span></span>

## <span data-ttu-id="bfc49-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bfc49-111">EXAMPLES</span></span>

### <span data-ttu-id="bfc49-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bfc49-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncGroup New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="bfc49-113">Эта команда получает все группы синхронизации, содержащиеся в указанной службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="bfc49-113">This command gets all sync groups contained within the specified storage sync service.</span></span> <span data-ttu-id="bfc49-114">Укажите имя, чтобы вернуть определенную единицу.</span><span class="sxs-lookup"><span data-stu-id="bfc49-114">Specify -Name to return a specific one.</span></span>

## <span data-ttu-id="bfc49-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bfc49-115">PARAMETERS</span></span>

### <span data-ttu-id="bfc49-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfc49-116">-DefaultProfile</span></span>
<span data-ttu-id="bfc49-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bfc49-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfc49-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bfc49-118">-Name</span></span>
<span data-ttu-id="bfc49-119">Имя SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="bfc49-119">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="bfc49-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="bfc49-120">-ParentObject</span></span>
<span data-ttu-id="bfc49-121">Объект StorageSyncService, обычно передаваемый через параметр.</span><span class="sxs-lookup"><span data-stu-id="bfc49-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="bfc49-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="bfc49-122">-ParentResourceId</span></span>
<span data-ttu-id="bfc49-123">Объект StorageSyncService, обычно передаваемый через параметр.</span><span class="sxs-lookup"><span data-stu-id="bfc49-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="bfc49-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfc49-124">-ResourceGroupName</span></span>
<span data-ttu-id="bfc49-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bfc49-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="bfc49-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="bfc49-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="bfc49-127">Имя StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="bfc49-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="bfc49-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfc49-128">CommonParameters</span></span>
<span data-ttu-id="bfc49-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bfc49-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfc49-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfc49-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfc49-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bfc49-131">INPUTS</span></span>

### <span data-ttu-id="bfc49-132">System. String</span><span class="sxs-lookup"><span data-stu-id="bfc49-132">System.String</span></span>

### <span data-ttu-id="bfc49-133">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="bfc49-133">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="bfc49-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bfc49-134">OUTPUTS</span></span>

### <span data-ttu-id="bfc49-135">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="bfc49-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="bfc49-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="bfc49-136">NOTES</span></span>

## <span data-ttu-id="bfc49-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bfc49-137">RELATED LINKS</span></span>
