---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncService.md
ms.openlocfilehash: 0476a881ec1ee479b97dad4ab8dcf95121dd5302
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505614"
---
# <span data-ttu-id="30db8-101">New-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="30db8-101">New-AzStorageSyncService</span></span>

## <span data-ttu-id="30db8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30db8-102">SYNOPSIS</span></span>
<span data-ttu-id="30db8-103">Эта команда создает новую службу синхронизации хранилища в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="30db8-103">This command creates a new storage sync service in a resource group.</span></span>

## <span data-ttu-id="30db8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="30db8-104">SYNTAX</span></span>

```
New-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-IncomingTrafficPolicy] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30db8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="30db8-105">DESCRIPTION</span></span>
<span data-ttu-id="30db8-106">Служба синхронизации хранилища — это ресурс верхнего уровня для Azure File Sync. Эта команда создает новую службу синхронизации хранилища в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="30db8-106">A storage sync service is the top level resource for Azure File Sync. This command creates a new storage sync service in a resource group.</span></span> <span data-ttu-id="30db8-107">Мы рекомендуем создавать как можно меньше служб синхронизации хранилища, чтобы отличать отдельные группы серверов в организации.</span><span class="sxs-lookup"><span data-stu-id="30db8-107">We recommend to create as few storage sync services as absolutely necessary to differentiate distinct groups of servers in your organization.</span></span> <span data-ttu-id="30db8-108">Служба синхронизации хранилища содержит группы синхронизации, а также служит целевым объектом для регистрации серверов.</span><span class="sxs-lookup"><span data-stu-id="30db8-108">A storage sync service contains sync groups and also works as a target to register your servers to.</span></span> <span data-ttu-id="30db8-109">Сервер можно зарегистрировать только в одной службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="30db8-109">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="30db8-110">Если серверы когда-нибудь потребуется синхронизировать один и тот же набор файлов, зарегистрируйте их в той же службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="30db8-110">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>

## <span data-ttu-id="30db8-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="30db8-111">EXAMPLES</span></span>

### <span data-ttu-id="30db8-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="30db8-112">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncService -ResourceGroupName "myResourceGroup" -Location "myLocation" -StorageSyncServiceName "myStorageSyncServiceName" -IncomingTrafficPolicy "AllowAllTraffic"
```

<span data-ttu-id="30db8-113">Эта команда создает службу синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="30db8-113">This command will create a storage sync service.</span></span>

## <span data-ttu-id="30db8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30db8-114">PARAMETERS</span></span>

### <span data-ttu-id="30db8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30db8-115">-DefaultProfile</span></span>
<span data-ttu-id="30db8-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="30db8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30db8-117">-Location</span><span class="sxs-lookup"><span data-stu-id="30db8-117">-Location</span></span>
<span data-ttu-id="30db8-118">Расположение службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="30db8-118">Storage Sync Service location.</span></span>

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

### <span data-ttu-id="30db8-119">-IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="30db8-119">-IncomingTrafficPolicy</span></span>
<span data-ttu-id="30db8-120">Служба синхронизации хранилища IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="30db8-120">Storage Sync Service IncomingTrafficPolicy</span></span>

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

### <span data-ttu-id="30db8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="30db8-121">-Name</span></span>
<span data-ttu-id="30db8-122">Имя службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="30db8-122">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="30db8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30db8-123">-ResourceGroupName</span></span>
<span data-ttu-id="30db8-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="30db8-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="30db8-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="30db8-125">-Tag</span></span>
<span data-ttu-id="30db8-126">Теги службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="30db8-126">Storage Sync Service Tags.</span></span>

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

### <span data-ttu-id="30db8-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="30db8-127">-Confirm</span></span>
<span data-ttu-id="30db8-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30db8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30db8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30db8-129">-WhatIf</span></span>
<span data-ttu-id="30db8-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30db8-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="30db8-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="30db8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30db8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30db8-132">CommonParameters</span></span>
<span data-ttu-id="30db8-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30db8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30db8-134">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30db8-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30db8-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="30db8-135">INPUTS</span></span>

### <span data-ttu-id="30db8-136">System.String</span><span class="sxs-lookup"><span data-stu-id="30db8-136">System.String</span></span>

## <span data-ttu-id="30db8-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="30db8-137">OUTPUTS</span></span>

### <span data-ttu-id="30db8-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="30db8-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="30db8-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="30db8-139">NOTES</span></span>

## <span data-ttu-id="30db8-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="30db8-140">RELATED LINKS</span></span>
