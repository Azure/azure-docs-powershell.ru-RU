---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
ms.openlocfilehash: 9d378139fb4783922973b5982039271461447c9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906974"
---
# <span data-ttu-id="1a1ec-101">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="1a1ec-101">Get-AzStorageSyncGroup</span></span>

## <span data-ttu-id="1a1ec-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1a1ec-102">SYNOPSIS</span></span>
<span data-ttu-id="1a1ec-103">Эта команда выводит список всех групп синхронизации в заданной службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="1a1ec-103">This command lists all sync groups within a given storage sync service.</span></span>

## <span data-ttu-id="1a1ec-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1a1ec-104">SYNTAX</span></span>

### <span data-ttu-id="1a1ec-105">StringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1a1ec-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a1ec-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a1ec-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a1ec-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a1ec-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1a1ec-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a1ec-108">DESCRIPTION</span></span>
<span data-ttu-id="1a1ec-109">Эта команда выводит список всех групп синхронизации в заданной службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="1a1ec-109">This command lists all sync groups within a given storage sync service.</span></span> <span data-ttu-id="1a1ec-110">Также можно использовать для перечисления атрибутов каждой из групп синхронизации.</span><span class="sxs-lookup"><span data-stu-id="1a1ec-110">It can be used to also list the attributes of each sync group.</span></span>

## <span data-ttu-id="1a1ec-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1a1ec-111">EXAMPLES</span></span>

### <span data-ttu-id="1a1ec-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1a1ec-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncGroup New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="1a1ec-113">Эта команда получает все группы синхронизации, содержащиеся в указанной службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="1a1ec-113">This command gets all sync groups contained within the specified storage sync service.</span></span> <span data-ttu-id="1a1ec-114">Укажите имя, чтобы вернуть определенную единицу.</span><span class="sxs-lookup"><span data-stu-id="1a1ec-114">Specify -Name to return a specific one.</span></span>

## <span data-ttu-id="1a1ec-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1a1ec-115">PARAMETERS</span></span>

### <span data-ttu-id="1a1ec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a1ec-116">-DefaultProfile</span></span>
<span data-ttu-id="1a1ec-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1a1ec-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a1ec-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1a1ec-118">-Name</span></span>
<span data-ttu-id="1a1ec-119">Имя SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="1a1ec-119">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="1a1ec-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1a1ec-120">-ParentObject</span></span>
<span data-ttu-id="1a1ec-121">Объект StorageSyncService, обычно передаваемый через параметр.</span><span class="sxs-lookup"><span data-stu-id="1a1ec-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="1a1ec-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="1a1ec-122">-ParentResourceId</span></span>
<span data-ttu-id="1a1ec-123">Объект StorageSyncService, обычно передаваемый через параметр.</span><span class="sxs-lookup"><span data-stu-id="1a1ec-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="1a1ec-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a1ec-124">-ResourceGroupName</span></span>
<span data-ttu-id="1a1ec-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1a1ec-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="1a1ec-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="1a1ec-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="1a1ec-127">Имя StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="1a1ec-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="1a1ec-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a1ec-128">CommonParameters</span></span>
<span data-ttu-id="1a1ec-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1a1ec-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a1ec-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a1ec-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a1ec-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1a1ec-131">INPUTS</span></span>

### <span data-ttu-id="1a1ec-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1a1ec-132">System.String</span></span>

### <span data-ttu-id="1a1ec-133">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="1a1ec-133">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="1a1ec-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a1ec-134">OUTPUTS</span></span>

### <span data-ttu-id="1a1ec-135">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="1a1ec-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="1a1ec-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="1a1ec-136">NOTES</span></span>

## <span data-ttu-id="1a1ec-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1a1ec-137">RELATED LINKS</span></span>
