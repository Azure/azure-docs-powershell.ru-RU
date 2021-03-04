---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/register-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
ms.openlocfilehash: 62dcefcf48e1d4c685b2a4f4855af41da7d8db75
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011320"
---
# <span data-ttu-id="b7110-101">Register-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="b7110-101">Register-AzStorageSyncServer</span></span>

## <span data-ttu-id="b7110-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7110-102">SYNOPSIS</span></span>
<span data-ttu-id="b7110-103">Эта команда регистрирует сервер в службе синхронизации хранилища, что создает отношение доверия.</span><span class="sxs-lookup"><span data-stu-id="b7110-103">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="b7110-104">Затем для настройки синхронизации на этом сервере можно использовать PowerShell или портал Azure.</span><span class="sxs-lookup"><span data-stu-id="b7110-104">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

## <span data-ttu-id="b7110-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b7110-105">SYNTAX</span></span>

### <span data-ttu-id="b7110-106">StringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b7110-106">StringParameterSet (Default)</span></span>
```
Register-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7110-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7110-107">ObjectParameterSet</span></span>
```
Register-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7110-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7110-108">ParentStringParameterSet</span></span>
```
Register-AzStorageSyncServer [-ParentResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7110-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7110-109">DESCRIPTION</span></span>
<span data-ttu-id="b7110-110">Эта команда регистрирует сервер в службу синхронизации хранилища — ресурс верхнего уровня для Azure File Sync. Создается доверительные отношения между сервером и службой синхронизации хранилища, обеспечивая безопасную передачу данных и каналы управления.</span><span class="sxs-lookup"><span data-stu-id="b7110-110">This command registers a server to a storage sync service, the top-level resource for Azure File Sync. A trust relationship between server and storage sync service is created that ensures secure data transfer and management channels.</span></span> <span data-ttu-id="b7110-111">Затем powerShell или портал Azure можно использовать для настройки синхронизации на этом сервере.</span><span class="sxs-lookup"><span data-stu-id="b7110-111">PowerShell or the Azure portal can then be used to configure what syncs on this server.</span></span> <span data-ttu-id="b7110-112">Сервер можно зарегистрировать только в одной службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="b7110-112">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="b7110-113">Если серверы когда-нибудь потребуется синхронизировать один и тот же набор файлов, зарегистрируйте их в той же службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="b7110-113">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>
<span data-ttu-id="b7110-114">Команду необходимо выполнить локально на сервере, который нужно зарегистрировать, — непосредственно или в удаленном сеансе PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b7110-114">The command must be run locally on the server that is to be registered - either executed directly or via a remote PowerShell session.</span></span> <span data-ttu-id="b7110-115">Нельзя принять объект удаленного компьютера.</span><span class="sxs-lookup"><span data-stu-id="b7110-115">A remote computer object cannot be accepted.</span></span>

## <span data-ttu-id="b7110-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b7110-116">EXAMPLES</span></span>

### <span data-ttu-id="b7110-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b7110-117">Example 1</span></span>
```powershell
PS C:\> Register-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="b7110-118">Эта команда зарегистрирует локальный сервер, на который она будет выполнить.</span><span class="sxs-lookup"><span data-stu-id="b7110-118">This command will register the local server this command is run on.</span></span>

## <span data-ttu-id="b7110-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7110-119">PARAMETERS</span></span>

### <span data-ttu-id="b7110-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7110-120">-AsJob</span></span>
<span data-ttu-id="b7110-121">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b7110-121">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7110-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7110-122">-DefaultProfile</span></span>
<span data-ttu-id="b7110-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b7110-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7110-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b7110-124">-ParentObject</span></span>
<span data-ttu-id="b7110-125">Объект StorageSyncService, обычно переданный через параметр.</span><span class="sxs-lookup"><span data-stu-id="b7110-125">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="b7110-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b7110-126">-ParentResourceId</span></span>
<span data-ttu-id="b7110-127">ИД родительского ресурса StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="b7110-127">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="b7110-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7110-128">-ResourceGroupName</span></span>
<span data-ttu-id="b7110-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b7110-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="b7110-130">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="b7110-130">-StorageSyncServiceName</span></span>
<span data-ttu-id="b7110-131">Имя службы StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="b7110-131">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="b7110-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7110-132">-Confirm</span></span>
<span data-ttu-id="b7110-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7110-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7110-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7110-134">-WhatIf</span></span>
<span data-ttu-id="b7110-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7110-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b7110-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b7110-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7110-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7110-137">CommonParameters</span></span>
<span data-ttu-id="b7110-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7110-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7110-139">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7110-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7110-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b7110-140">INPUTS</span></span>

### <span data-ttu-id="b7110-141">System.String</span><span class="sxs-lookup"><span data-stu-id="b7110-141">System.String</span></span>

### <span data-ttu-id="b7110-142">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="b7110-142">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="b7110-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b7110-143">OUTPUTS</span></span>

### <span data-ttu-id="b7110-144">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="b7110-144">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="b7110-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b7110-145">NOTES</span></span>

## <span data-ttu-id="b7110-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b7110-146">RELATED LINKS</span></span>
