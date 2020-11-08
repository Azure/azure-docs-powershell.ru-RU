---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/register-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
ms.openlocfilehash: bb1ce6f9ff7e846c2f485665cafad700fa4c825b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248459"
---
# <span data-ttu-id="e5cd0-101">Register-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="e5cd0-101">Register-AzStorageSyncServer</span></span>

## <span data-ttu-id="e5cd0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e5cd0-102">SYNOPSIS</span></span>
<span data-ttu-id="e5cd0-103">Эта команда регистрирует сервер для службы синхронизации хранилища, который создает отношение доверия.</span><span class="sxs-lookup"><span data-stu-id="e5cd0-103">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="e5cd0-104">Вы можете использовать PowerShell или портал Azure для настройки синхронизации на этом сервере.</span><span class="sxs-lookup"><span data-stu-id="e5cd0-104">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

## <span data-ttu-id="e5cd0-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e5cd0-105">SYNTAX</span></span>

### <span data-ttu-id="e5cd0-106">StringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e5cd0-106">StringParameterSet (Default)</span></span>
```
Register-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5cd0-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5cd0-107">ObjectParameterSet</span></span>
```
Register-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5cd0-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5cd0-108">ParentStringParameterSet</span></span>
```
Register-AzStorageSyncServer [-ParentResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5cd0-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5cd0-109">DESCRIPTION</span></span>
<span data-ttu-id="e5cd0-110">Эта команда регистрирует сервер для службы синхронизации хранилища, ресурс верхнего уровня для синхронизации файлов Azure. Создается отношение доверия между сервером и службой синхронизации хранилища, которое обеспечивает безопасность каналов передачи данных и управления ими.</span><span class="sxs-lookup"><span data-stu-id="e5cd0-110">This command registers a server to a storage sync service, the top-level resource for Azure File Sync. A trust relationship between server and storage sync service is created that ensures secure data transfer and management channels.</span></span> <span data-ttu-id="e5cd0-111">Вы можете использовать PowerShell или портал Azure для настройки синхронизации на этом сервере.</span><span class="sxs-lookup"><span data-stu-id="e5cd0-111">PowerShell or the Azure portal can then be used to configure what syncs on this server.</span></span> <span data-ttu-id="e5cd0-112">Сервер может быть зарегистрирован только в одной службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="e5cd0-112">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="e5cd0-113">Если нужно, чтобы серверы использовали один и тот же набор файлов, зарегистрируйте их в одной и той же службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="e5cd0-113">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>
<span data-ttu-id="e5cd0-114">Команда должна выполняться локально на сервере, который должен быть зарегистрирован, либо выполняться прямо, либо с помощью удаленного сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e5cd0-114">The command must be run locally on the server that is to be registered - either executed directly or via a remote PowerShell session.</span></span> <span data-ttu-id="e5cd0-115">Удаленный объект компьютера не может быть принят.</span><span class="sxs-lookup"><span data-stu-id="e5cd0-115">A remote computer object cannot be accepted.</span></span>

## <span data-ttu-id="e5cd0-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e5cd0-116">EXAMPLES</span></span>

### <span data-ttu-id="e5cd0-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e5cd0-117">Example 1</span></span>
```powershell
PS C:\> Register-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="e5cd0-118">Эта команда зарегистрирует локальный сервер, на котором она выполняется.</span><span class="sxs-lookup"><span data-stu-id="e5cd0-118">This command will register the local server this command is run on.</span></span>

## <span data-ttu-id="e5cd0-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e5cd0-119">PARAMETERS</span></span>

### <span data-ttu-id="e5cd0-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e5cd0-120">-AsJob</span></span>
<span data-ttu-id="e5cd0-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e5cd0-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e5cd0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5cd0-122">-DefaultProfile</span></span>
<span data-ttu-id="e5cd0-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e5cd0-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5cd0-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e5cd0-124">-ParentObject</span></span>
<span data-ttu-id="e5cd0-125">Объект StorageSyncService, обычно передаваемый через параметр.</span><span class="sxs-lookup"><span data-stu-id="e5cd0-125">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="e5cd0-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e5cd0-126">-ParentResourceId</span></span>
<span data-ttu-id="e5cd0-127">Идентификатор родительского ресурса StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="e5cd0-127">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="e5cd0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5cd0-128">-ResourceGroupName</span></span>
<span data-ttu-id="e5cd0-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e5cd0-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="e5cd0-130">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="e5cd0-130">-StorageSyncServiceName</span></span>
<span data-ttu-id="e5cd0-131">Имя StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="e5cd0-131">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="e5cd0-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5cd0-132">-Confirm</span></span>
<span data-ttu-id="e5cd0-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e5cd0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5cd0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5cd0-134">-WhatIf</span></span>
<span data-ttu-id="e5cd0-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e5cd0-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e5cd0-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e5cd0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5cd0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5cd0-137">CommonParameters</span></span>
<span data-ttu-id="e5cd0-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e5cd0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5cd0-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5cd0-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5cd0-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e5cd0-140">INPUTS</span></span>

### <span data-ttu-id="e5cd0-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e5cd0-141">System.String</span></span>

### <span data-ttu-id="e5cd0-142">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="e5cd0-142">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="e5cd0-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5cd0-143">OUTPUTS</span></span>

### <span data-ttu-id="e5cd0-144">Microsoft. Azure. Commands. StorageSync. Models. PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="e5cd0-144">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="e5cd0-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="e5cd0-145">NOTES</span></span>

## <span data-ttu-id="e5cd0-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5cd0-146">RELATED LINKS</span></span>
