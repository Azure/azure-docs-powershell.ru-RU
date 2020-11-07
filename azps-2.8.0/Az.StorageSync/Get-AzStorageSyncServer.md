---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
ms.openlocfilehash: bd1665ee82dfad0bb6028252ad100e5c651d0c2d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906973"
---
# <span data-ttu-id="d3e45-101">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="d3e45-101">Get-AzStorageSyncServer</span></span>

## <span data-ttu-id="d3e45-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d3e45-102">SYNOPSIS</span></span>
<span data-ttu-id="d3e45-103">Эта команда перечисляет все серверы, зарегистрированные для указанной службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="d3e45-103">This command lists all servers registered to a given storage sync service.</span></span>

## <span data-ttu-id="d3e45-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d3e45-104">SYNTAX</span></span>

### <span data-ttu-id="d3e45-105">StringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d3e45-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3e45-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3e45-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3e45-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3e45-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServer [-ParentResourceId] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3e45-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3e45-108">DESCRIPTION</span></span>
<span data-ttu-id="d3e45-109">Эта команда перечисляет все серверы, зарегистрированные для указанной службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="d3e45-109">This command lists all servers registered to a given storage sync service.</span></span> <span data-ttu-id="d3e45-110">Также можно использовать для перечисления атрибутов каждого зарегистрированного сервера.</span><span class="sxs-lookup"><span data-stu-id="d3e45-110">It can be used to also list the attributes of each registered server.</span></span>

## <span data-ttu-id="d3e45-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d3e45-111">EXAMPLES</span></span>

### <span data-ttu-id="d3e45-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d3e45-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="d3e45-113">Эта команда возвращает все серверы, зарегистрированные в определенной службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="d3e45-113">This command gets all servers registered to a specific storage sync service.</span></span>

## <span data-ttu-id="d3e45-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d3e45-114">PARAMETERS</span></span>

### <span data-ttu-id="d3e45-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3e45-115">-DefaultProfile</span></span>
<span data-ttu-id="d3e45-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d3e45-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3e45-117">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d3e45-117">-ParentObject</span></span>
<span data-ttu-id="d3e45-118">Объект StorageSyncService, обычно передаваемый через параметр.</span><span class="sxs-lookup"><span data-stu-id="d3e45-118">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="d3e45-119">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d3e45-119">-ParentResourceId</span></span>
<span data-ttu-id="d3e45-120">Объект StorageSyncService, обычно передаваемый через параметр.</span><span class="sxs-lookup"><span data-stu-id="d3e45-120">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="d3e45-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3e45-121">-ResourceGroupName</span></span>
<span data-ttu-id="d3e45-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d3e45-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="d3e45-123">-ServerId</span><span class="sxs-lookup"><span data-stu-id="d3e45-123">-ServerId</span></span>
<span data-ttu-id="d3e45-124">Имя RegisteredServer.</span><span class="sxs-lookup"><span data-stu-id="d3e45-124">Name of the RegisteredServer.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: RegisteredServerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3e45-125">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="d3e45-125">-StorageSyncServiceName</span></span>
<span data-ttu-id="d3e45-126">Имя StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="d3e45-126">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="d3e45-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3e45-127">CommonParameters</span></span>
<span data-ttu-id="d3e45-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d3e45-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3e45-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3e45-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3e45-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d3e45-130">INPUTS</span></span>

### <span data-ttu-id="d3e45-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d3e45-131">System.String</span></span>

### <span data-ttu-id="d3e45-132">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="d3e45-132">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="d3e45-133">System. GUID</span><span class="sxs-lookup"><span data-stu-id="d3e45-133">System.Guid</span></span>

## <span data-ttu-id="d3e45-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3e45-134">OUTPUTS</span></span>

### <span data-ttu-id="d3e45-135">Microsoft. Azure. Commands. StorageSync. Models. PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="d3e45-135">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="d3e45-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="d3e45-136">NOTES</span></span>

## <span data-ttu-id="d3e45-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3e45-137">RELATED LINKS</span></span>
