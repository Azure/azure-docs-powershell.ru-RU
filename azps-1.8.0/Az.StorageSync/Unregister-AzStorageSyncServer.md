---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/unregister-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
ms.openlocfilehash: 87734d63d28785282ad3285ef8cce0a574ba30e3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728468"
---
# <span data-ttu-id="b207c-101">Unregister-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="b207c-101">Unregister-AzStorageSyncServer</span></span>

## <span data-ttu-id="b207c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b207c-102">SYNOPSIS</span></span>
<span data-ttu-id="b207c-103">Предупреждение: Отмена регистрации сервера приводит к каскадному удалению всех конечных точек сервера на этом сервере.</span><span class="sxs-lookup"><span data-stu-id="b207c-103">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="b207c-104">Эта команда отменит регистрацию сервера, так как служба синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="b207c-104">This command will unregister a server it's the storage sync service.</span></span>

## <span data-ttu-id="b207c-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b207c-105">SYNTAX</span></span>

### <span data-ttu-id="b207c-106">InputObjectParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b207c-106">InputObjectParameterSet (Default)</span></span>
```
Unregister-AzStorageSyncServer [-InputObject] <PSRegisteredServer> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b207c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b207c-107">ResourceIdParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b207c-108">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="b207c-108">StringParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-ServerId] <Guid> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b207c-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b207c-109">DESCRIPTION</span></span>
<span data-ttu-id="b207c-110">Эта команда отменит регистрацию сервера в службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="b207c-110">This command will unregister a server from the storage sync service.</span></span> <span data-ttu-id="b207c-111">Предупреждение: Отмена регистрации сервера приводит к каскадному удалению всех конечных точек сервера на этом сервере.</span><span class="sxs-lookup"><span data-stu-id="b207c-111">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="b207c-112">Его следует вызывать только в том случае, если вы уверены, что путь на этом сервере больше не нужно синхронизировать.</span><span class="sxs-lookup"><span data-stu-id="b207c-112">It should only be called when you are certain that no path on this server is to be synced anymore.</span></span>

## <span data-ttu-id="b207c-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b207c-113">EXAMPLES</span></span>

### <span data-ttu-id="b207c-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b207c-114">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> Unregister-AzStorageSyncServer -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -ServerId $RegisteredServer.ServerId
```

<span data-ttu-id="b207c-115">Эта команда отменит регистрацию сервера, вынуждая каскадное удаление всех конечных точек сервера на этом сервере.</span><span class="sxs-lookup"><span data-stu-id="b207c-115">This command will unregister the server, causing cascading deletes of all server endpoints on this server.</span></span>

## <span data-ttu-id="b207c-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b207c-116">PARAMETERS</span></span>

### <span data-ttu-id="b207c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b207c-117">-AsJob</span></span>
<span data-ttu-id="b207c-118">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b207c-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b207c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b207c-119">-DefaultProfile</span></span>
<span data-ttu-id="b207c-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b207c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b207c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="b207c-121">-Force</span></span>
<span data-ttu-id="b207c-122">Укажите, чтобы пропустить подтверждение этой команды.</span><span class="sxs-lookup"><span data-stu-id="b207c-122">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="b207c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b207c-123">-InputObject</span></span>
<span data-ttu-id="b207c-124">Входной объект RegisteredServer, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="b207c-124">RegisteredServer Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="b207c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b207c-125">-PassThru</span></span>
<span data-ttu-id="b207c-126">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="b207c-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b207c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b207c-127">-ResourceGroupName</span></span>
<span data-ttu-id="b207c-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b207c-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="b207c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b207c-129">-ResourceId</span></span>
<span data-ttu-id="b207c-130">Идентификатор ресурса RegisteredServer</span><span class="sxs-lookup"><span data-stu-id="b207c-130">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="b207c-131">-ServerId</span><span class="sxs-lookup"><span data-stu-id="b207c-131">-ServerId</span></span>
<span data-ttu-id="b207c-132">Имя RegisteredServer.</span><span class="sxs-lookup"><span data-stu-id="b207c-132">Name of the RegisteredServer.</span></span>

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

### <span data-ttu-id="b207c-133">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="b207c-133">-StorageSyncServiceName</span></span>
<span data-ttu-id="b207c-134">Имя StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="b207c-134">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="b207c-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b207c-135">-Confirm</span></span>
<span data-ttu-id="b207c-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b207c-136">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b207c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b207c-137">-WhatIf</span></span>
<span data-ttu-id="b207c-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b207c-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b207c-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b207c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b207c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b207c-140">CommonParameters</span></span>
<span data-ttu-id="b207c-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b207c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b207c-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b207c-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b207c-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b207c-143">INPUTS</span></span>

### <span data-ttu-id="b207c-144">Microsoft. Azure. Commands. StorageSync. Models. PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="b207c-144">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

### <span data-ttu-id="b207c-145">System. String</span><span class="sxs-lookup"><span data-stu-id="b207c-145">System.String</span></span>

### <span data-ttu-id="b207c-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b207c-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b207c-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b207c-147">OUTPUTS</span></span>

### <span data-ttu-id="b207c-148">System. Object</span><span class="sxs-lookup"><span data-stu-id="b207c-148">System.Object</span></span>
## <span data-ttu-id="b207c-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="b207c-149">NOTES</span></span>

## <span data-ttu-id="b207c-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b207c-150">RELATED LINKS</span></span>
