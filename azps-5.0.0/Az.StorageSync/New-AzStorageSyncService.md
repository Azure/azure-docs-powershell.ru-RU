---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncService.md
ms.openlocfilehash: 0476a881ec1ee479b97dad4ab8dcf95121dd5302
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318209"
---
# <span data-ttu-id="928b6-101">New-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="928b6-101">New-AzStorageSyncService</span></span>

## <span data-ttu-id="928b6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="928b6-102">SYNOPSIS</span></span>
<span data-ttu-id="928b6-103">Эта команда создает новую службу синхронизации хранилища в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="928b6-103">This command creates a new storage sync service in a resource group.</span></span>

## <span data-ttu-id="928b6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="928b6-104">SYNTAX</span></span>

```
New-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-IncomingTrafficPolicy] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="928b6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="928b6-105">DESCRIPTION</span></span>
<span data-ttu-id="928b6-106">Служба синхронизации хранилища — это ресурс верхнего уровня для синхронизации файлов Azure. Эта команда создает новую службу синхронизации хранилища в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="928b6-106">A storage sync service is the top level resource for Azure File Sync. This command creates a new storage sync service in a resource group.</span></span> <span data-ttu-id="928b6-107">Для различения отдельных групп серверов в организации рекомендуется создать как можно меньше служб синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="928b6-107">We recommend to create as few storage sync services as absolutely necessary to differentiate distinct groups of servers in your organization.</span></span> <span data-ttu-id="928b6-108">Служба синхронизации хранилища включает группы синхронизации, а также работает как целевой объект для регистрации серверов.</span><span class="sxs-lookup"><span data-stu-id="928b6-108">A storage sync service contains sync groups and also works as a target to register your servers to.</span></span> <span data-ttu-id="928b6-109">Сервер может быть зарегистрирован только в одной службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="928b6-109">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="928b6-110">Если нужно, чтобы серверы использовали один и тот же набор файлов, зарегистрируйте их в одной и той же службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="928b6-110">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>

## <span data-ttu-id="928b6-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="928b6-111">EXAMPLES</span></span>

### <span data-ttu-id="928b6-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="928b6-112">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncService -ResourceGroupName "myResourceGroup" -Location "myLocation" -StorageSyncServiceName "myStorageSyncServiceName" -IncomingTrafficPolicy "AllowAllTraffic"
```

<span data-ttu-id="928b6-113">Эта команда создаст службу синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="928b6-113">This command will create a storage sync service.</span></span>

## <span data-ttu-id="928b6-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="928b6-114">PARAMETERS</span></span>

### <span data-ttu-id="928b6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="928b6-115">-DefaultProfile</span></span>
<span data-ttu-id="928b6-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="928b6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="928b6-117">-Location</span><span class="sxs-lookup"><span data-stu-id="928b6-117">-Location</span></span>
<span data-ttu-id="928b6-118">Расположение службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="928b6-118">Storage Sync Service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="928b6-119">-IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="928b6-119">-IncomingTrafficPolicy</span></span>
<span data-ttu-id="928b6-120">Служба синхронизации хранилища IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="928b6-120">Storage Sync Service IncomingTrafficPolicy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="928b6-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="928b6-121">-Name</span></span>
<span data-ttu-id="928b6-122">Имя службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="928b6-122">Name of the storage sync service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageSyncServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="928b6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="928b6-123">-ResourceGroupName</span></span>
<span data-ttu-id="928b6-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="928b6-124">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="928b6-125">-Тег</span><span class="sxs-lookup"><span data-stu-id="928b6-125">-Tag</span></span>
<span data-ttu-id="928b6-126">Теги службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="928b6-126">Storage Sync Service Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="928b6-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="928b6-127">-Confirm</span></span>
<span data-ttu-id="928b6-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="928b6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="928b6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="928b6-129">-WhatIf</span></span>
<span data-ttu-id="928b6-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="928b6-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="928b6-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="928b6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="928b6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="928b6-132">CommonParameters</span></span>
<span data-ttu-id="928b6-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="928b6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="928b6-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="928b6-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="928b6-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="928b6-135">INPUTS</span></span>

### <span data-ttu-id="928b6-136">System. String</span><span class="sxs-lookup"><span data-stu-id="928b6-136">System.String</span></span>

## <span data-ttu-id="928b6-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="928b6-137">OUTPUTS</span></span>

### <span data-ttu-id="928b6-138">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="928b6-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="928b6-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="928b6-139">NOTES</span></span>

## <span data-ttu-id="928b6-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="928b6-140">RELATED LINKS</span></span>
