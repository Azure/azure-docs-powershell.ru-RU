---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/unregister-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
ms.openlocfilehash: f6de2bf731bc11a4b0ec8b6c894e6d77569ec9ce
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414495"
---
# <span data-ttu-id="41335-101">Unregister-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="41335-101">Unregister-AzStorageSyncServer</span></span>

## <span data-ttu-id="41335-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41335-102">SYNOPSIS</span></span>
<span data-ttu-id="41335-103">Предупреждение. Если отрегистрить сервер, это приведет к каскадным удалениям всех конечных точек сервера на этом сервере.</span><span class="sxs-lookup"><span data-stu-id="41335-103">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="41335-104">Эта команда отстранит регистрацию сервера из его службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="41335-104">This command will unregister a server from it's storage sync service.</span></span>

## <span data-ttu-id="41335-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="41335-105">SYNTAX</span></span>

### <span data-ttu-id="41335-106">StringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="41335-106">StringParameterSet (Default)</span></span>
```
Unregister-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-ServerId] <Guid> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41335-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="41335-107">InputObjectParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-InputObject] <PSRegisteredServer> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41335-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="41335-108">ResourceIdParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41335-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="41335-109">DESCRIPTION</span></span>
<span data-ttu-id="41335-110">Эта команда отстранит сервер из службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="41335-110">This command will unregister a server from the storage sync service.</span></span> <span data-ttu-id="41335-111">Предупреждение. Если отрегистрить сервер, это приведет к каскадным удалениям всех конечных точек сервера на этом сервере.</span><span class="sxs-lookup"><span data-stu-id="41335-111">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="41335-112">Он следует использовать только тогда, когда вы уверены, что больше не нужно синхронизировать путь к этому серверу.</span><span class="sxs-lookup"><span data-stu-id="41335-112">It should only be called when you are certain that no path on this server is to be synced anymore.</span></span>

## <span data-ttu-id="41335-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="41335-113">EXAMPLES</span></span>

### <span data-ttu-id="41335-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="41335-114">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> Unregister-AzStorageSyncServer -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -ServerId $RegisteredServer.ServerId
```

<span data-ttu-id="41335-115">Эта команда откатит регистрацию сервера, что приводит к каскадным удалениям всех конечных точек сервера на этом сервере.</span><span class="sxs-lookup"><span data-stu-id="41335-115">This command will unregister the server, causing cascading deletes of all server endpoints on this server.</span></span>

## <span data-ttu-id="41335-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41335-116">PARAMETERS</span></span>

### <span data-ttu-id="41335-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41335-117">-AsJob</span></span>
<span data-ttu-id="41335-118">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="41335-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="41335-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41335-119">-DefaultProfile</span></span>
<span data-ttu-id="41335-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="41335-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41335-121">-Force</span><span class="sxs-lookup"><span data-stu-id="41335-121">-Force</span></span>
<span data-ttu-id="41335-122">Supply -Force, чтобы пропустить подтверждение этой команды.</span><span class="sxs-lookup"><span data-stu-id="41335-122">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="41335-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41335-123">-InputObject</span></span>
<span data-ttu-id="41335-124">Объект ввода RegisteredServer, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="41335-124">RegisteredServer Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="41335-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41335-125">-PassThru</span></span>
<span data-ttu-id="41335-126">В обычном выполнении этот cmdlet не возвращает никакого значения для успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="41335-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="41335-127">Если для параметра PassThru задан параметр PassThru, после успешного выполнения он будет записывать значение в конвейер.</span><span class="sxs-lookup"><span data-stu-id="41335-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="41335-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41335-128">-ResourceGroupName</span></span>
<span data-ttu-id="41335-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="41335-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="41335-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41335-130">-ResourceId</span></span>
<span data-ttu-id="41335-131">RegisteredServer Resource Id</span><span class="sxs-lookup"><span data-stu-id="41335-131">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="41335-132">-ServerId</span><span class="sxs-lookup"><span data-stu-id="41335-132">-ServerId</span></span>
<span data-ttu-id="41335-133">Имя зарегистрированногоServer.</span><span class="sxs-lookup"><span data-stu-id="41335-133">Name of the RegisteredServer.</span></span>

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

### <span data-ttu-id="41335-134">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="41335-134">-StorageSyncServiceName</span></span>
<span data-ttu-id="41335-135">Имя службы StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="41335-135">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="41335-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="41335-136">-Confirm</span></span>
<span data-ttu-id="41335-137">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41335-137">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41335-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41335-138">-WhatIf</span></span>
<span data-ttu-id="41335-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41335-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="41335-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="41335-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41335-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41335-141">CommonParameters</span></span>
<span data-ttu-id="41335-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41335-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41335-143">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41335-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41335-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="41335-144">INPUTS</span></span>

### <span data-ttu-id="41335-145">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="41335-145">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

### <span data-ttu-id="41335-146">System.String</span><span class="sxs-lookup"><span data-stu-id="41335-146">System.String</span></span>

### <span data-ttu-id="41335-147">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="41335-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="41335-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="41335-148">OUTPUTS</span></span>

### <span data-ttu-id="41335-149">System.Object</span><span class="sxs-lookup"><span data-stu-id="41335-149">System.Object</span></span>
## <span data-ttu-id="41335-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="41335-150">NOTES</span></span>

## <span data-ttu-id="41335-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="41335-151">RELATED LINKS</span></span>
