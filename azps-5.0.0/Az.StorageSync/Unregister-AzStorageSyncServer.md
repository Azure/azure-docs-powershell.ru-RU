---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/unregister-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
ms.openlocfilehash: f6de2bf731bc11a4b0ec8b6c894e6d77569ec9ce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245997"
---
# <span data-ttu-id="de129-101">Unregister-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="de129-101">Unregister-AzStorageSyncServer</span></span>

## <span data-ttu-id="de129-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="de129-102">SYNOPSIS</span></span>
<span data-ttu-id="de129-103">Предупреждение: Отмена регистрации сервера приводит к каскадному удалению всех конечных точек сервера на этом сервере.</span><span class="sxs-lookup"><span data-stu-id="de129-103">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="de129-104">Эта команда отменит регистрацию сервера в службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="de129-104">This command will unregister a server from it's storage sync service.</span></span>

## <span data-ttu-id="de129-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="de129-105">SYNTAX</span></span>

### <span data-ttu-id="de129-106">StringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="de129-106">StringParameterSet (Default)</span></span>
```
Unregister-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-ServerId] <Guid> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de129-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="de129-107">InputObjectParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-InputObject] <PSRegisteredServer> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de129-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="de129-108">ResourceIdParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de129-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="de129-109">DESCRIPTION</span></span>
<span data-ttu-id="de129-110">Эта команда отменит регистрацию сервера в службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="de129-110">This command will unregister a server from the storage sync service.</span></span> <span data-ttu-id="de129-111">Предупреждение: Отмена регистрации сервера приводит к каскадному удалению всех конечных точек сервера на этом сервере.</span><span class="sxs-lookup"><span data-stu-id="de129-111">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="de129-112">Его следует вызывать только в том случае, если вы уверены, что путь на этом сервере больше не нужно синхронизировать.</span><span class="sxs-lookup"><span data-stu-id="de129-112">It should only be called when you are certain that no path on this server is to be synced anymore.</span></span>

## <span data-ttu-id="de129-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="de129-113">EXAMPLES</span></span>

### <span data-ttu-id="de129-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="de129-114">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> Unregister-AzStorageSyncServer -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -ServerId $RegisteredServer.ServerId
```

<span data-ttu-id="de129-115">Эта команда отменит регистрацию сервера, вынуждая каскадное удаление всех конечных точек сервера на этом сервере.</span><span class="sxs-lookup"><span data-stu-id="de129-115">This command will unregister the server, causing cascading deletes of all server endpoints on this server.</span></span>

## <span data-ttu-id="de129-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="de129-116">PARAMETERS</span></span>

### <span data-ttu-id="de129-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de129-117">-AsJob</span></span>
<span data-ttu-id="de129-118">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="de129-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="de129-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de129-119">-DefaultProfile</span></span>
<span data-ttu-id="de129-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="de129-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de129-121">-Force</span><span class="sxs-lookup"><span data-stu-id="de129-121">-Force</span></span>
<span data-ttu-id="de129-122">Укажите, чтобы пропустить подтверждение этой команды.</span><span class="sxs-lookup"><span data-stu-id="de129-122">Supply -Force to skip confirmation of this command.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de129-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de129-123">-InputObject</span></span>
<span data-ttu-id="de129-124">Входной объект RegisteredServer, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="de129-124">RegisteredServer Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de129-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="de129-125">-PassThru</span></span>
<span data-ttu-id="de129-126">При нормальном выполнении этот командлет не возвращает значение в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="de129-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="de129-127">Если вы предоставляете параметр PassThru, командлет запишет значение в конвейер после успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="de129-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="de129-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de129-128">-ResourceGroupName</span></span>
<span data-ttu-id="de129-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="de129-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de129-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de129-130">-ResourceId</span></span>
<span data-ttu-id="de129-131">Идентификатор ресурса RegisteredServer</span><span class="sxs-lookup"><span data-stu-id="de129-131">RegisteredServer Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de129-132">-ServerId</span><span class="sxs-lookup"><span data-stu-id="de129-132">-ServerId</span></span>
<span data-ttu-id="de129-133">Имя RegisteredServer.</span><span class="sxs-lookup"><span data-stu-id="de129-133">Name of the RegisteredServer.</span></span>

```yaml
Type: System.Guid
Parameter Sets: StringParameterSet
Aliases: RegisteredServerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de129-134">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="de129-134">-StorageSyncServiceName</span></span>
<span data-ttu-id="de129-135">Имя StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="de129-135">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de129-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="de129-136">-Confirm</span></span>
<span data-ttu-id="de129-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="de129-137">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de129-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de129-138">-WhatIf</span></span>
<span data-ttu-id="de129-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="de129-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="de129-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="de129-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de129-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de129-141">CommonParameters</span></span>
<span data-ttu-id="de129-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="de129-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de129-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de129-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de129-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="de129-144">INPUTS</span></span>

### <span data-ttu-id="de129-145">Microsoft. Azure. Commands. StorageSync. Models. PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="de129-145">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

### <span data-ttu-id="de129-146">System. String</span><span class="sxs-lookup"><span data-stu-id="de129-146">System.String</span></span>

### <span data-ttu-id="de129-147">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="de129-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="de129-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="de129-148">OUTPUTS</span></span>

### <span data-ttu-id="de129-149">System. Object</span><span class="sxs-lookup"><span data-stu-id="de129-149">System.Object</span></span>
## <span data-ttu-id="de129-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="de129-150">NOTES</span></span>

## <span data-ttu-id="de129-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="de129-151">RELATED LINKS</span></span>
