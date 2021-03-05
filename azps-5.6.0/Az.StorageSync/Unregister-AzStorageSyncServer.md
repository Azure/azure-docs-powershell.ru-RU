---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/unregister-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
ms.openlocfilehash: 5ebcdee62997ed678b9696264a40076a40c36342
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973976"
---
# <span data-ttu-id="6f648-101">Unregister-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="6f648-101">Unregister-AzStorageSyncServer</span></span>

## <span data-ttu-id="6f648-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f648-102">SYNOPSIS</span></span>
<span data-ttu-id="6f648-103">Предупреждение. Если отопустить сервер, будет каскадно удалено все конечные точки сервера.</span><span class="sxs-lookup"><span data-stu-id="6f648-103">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="6f648-104">Эта команда отстранит регистрацию сервера из его службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="6f648-104">This command will unregister a server from it's storage sync service.</span></span>

## <span data-ttu-id="6f648-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6f648-105">SYNTAX</span></span>

### <span data-ttu-id="6f648-106">StringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6f648-106">StringParameterSet (Default)</span></span>
```
Unregister-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-ServerId] <Guid> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f648-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f648-107">InputObjectParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-InputObject] <PSRegisteredServer> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f648-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f648-108">ResourceIdParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f648-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f648-109">DESCRIPTION</span></span>
<span data-ttu-id="6f648-110">Эта команда отстраномит сервер от службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="6f648-110">This command will unregister a server from the storage sync service.</span></span> <span data-ttu-id="6f648-111">Предупреждение. Если отрегистрить сервер, это приведет к каскадным удалениям всех конечных точек сервера на этом сервере.</span><span class="sxs-lookup"><span data-stu-id="6f648-111">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="6f648-112">Он следует использовать только тогда, когда вы уверены, что больше не нужно синхронизировать путь к этому серверу.</span><span class="sxs-lookup"><span data-stu-id="6f648-112">It should only be called when you are certain that no path on this server is to be synced anymore.</span></span>

## <span data-ttu-id="6f648-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6f648-113">EXAMPLES</span></span>

### <span data-ttu-id="6f648-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6f648-114">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> Unregister-AzStorageSyncServer -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -ServerId $RegisteredServer.ServerId
```

<span data-ttu-id="6f648-115">Эта команда откатит регистрацию сервера, что приводит к каскадным удалениям всех конечных точек сервера на этом сервере.</span><span class="sxs-lookup"><span data-stu-id="6f648-115">This command will unregister the server, causing cascading deletes of all server endpoints on this server.</span></span>

## <span data-ttu-id="6f648-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f648-116">PARAMETERS</span></span>

### <span data-ttu-id="6f648-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f648-117">-AsJob</span></span>
<span data-ttu-id="6f648-118">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6f648-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6f648-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f648-119">-DefaultProfile</span></span>
<span data-ttu-id="6f648-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6f648-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f648-121">-Force</span><span class="sxs-lookup"><span data-stu-id="6f648-121">-Force</span></span>
<span data-ttu-id="6f648-122">Supply -Force, чтобы пропустить подтверждение этой команды.</span><span class="sxs-lookup"><span data-stu-id="6f648-122">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="6f648-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f648-123">-InputObject</span></span>
<span data-ttu-id="6f648-124">Объект ввода RegisteredServer, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="6f648-124">RegisteredServer Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="6f648-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f648-125">-PassThru</span></span>
<span data-ttu-id="6f648-126">В обычном выполнении этот cmdlet не возвращает никакого значения для успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="6f648-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="6f648-127">Если для параметра PassThru задан параметр PassThru, то после успешного выполнения он будет записывать значение в конвейер.</span><span class="sxs-lookup"><span data-stu-id="6f648-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="6f648-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f648-128">-ResourceGroupName</span></span>
<span data-ttu-id="6f648-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6f648-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="6f648-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f648-130">-ResourceId</span></span>
<span data-ttu-id="6f648-131">RegisteredServer Resource Id</span><span class="sxs-lookup"><span data-stu-id="6f648-131">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="6f648-132">-ServerId</span><span class="sxs-lookup"><span data-stu-id="6f648-132">-ServerId</span></span>
<span data-ttu-id="6f648-133">Имя зарегистрированногоerver.</span><span class="sxs-lookup"><span data-stu-id="6f648-133">Name of the RegisteredServer.</span></span>

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

### <span data-ttu-id="6f648-134">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="6f648-134">-StorageSyncServiceName</span></span>
<span data-ttu-id="6f648-135">Имя службы StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="6f648-135">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="6f648-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6f648-136">-Confirm</span></span>
<span data-ttu-id="6f648-137">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f648-137">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f648-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f648-138">-WhatIf</span></span>
<span data-ttu-id="6f648-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f648-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6f648-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6f648-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f648-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f648-141">CommonParameters</span></span>
<span data-ttu-id="6f648-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f648-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f648-143">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f648-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f648-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6f648-144">INPUTS</span></span>

### <span data-ttu-id="6f648-145">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="6f648-145">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

### <span data-ttu-id="6f648-146">System.String</span><span class="sxs-lookup"><span data-stu-id="6f648-146">System.String</span></span>

### <span data-ttu-id="6f648-147">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6f648-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6f648-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6f648-148">OUTPUTS</span></span>

### <span data-ttu-id="6f648-149">System.Object</span><span class="sxs-lookup"><span data-stu-id="6f648-149">System.Object</span></span>
## <span data-ttu-id="6f648-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6f648-150">NOTES</span></span>

## <span data-ttu-id="6f648-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f648-151">RELATED LINKS</span></span>
