---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/reset-Azstoragesyncservercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
ms.openlocfilehash: 5d93249b6bb160d2659ead144d3fabda1af8438d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974008"
---
# <span data-ttu-id="27e34-101">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="27e34-101">Reset-AzStorageSyncServerCertificate</span></span>

## <span data-ttu-id="27e34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27e34-102">SYNOPSIS</span></span>
<span data-ttu-id="27e34-103">Используется только для устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="27e34-103">Use for troubleshooting only.</span></span> <span data-ttu-id="27e34-104">Эта команда позволит свернуть сертификат сервера синхронизации хранилища, используемый для описания идентификаторов сервера, в службу синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="27e34-104">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

## <span data-ttu-id="27e34-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="27e34-105">SYNTAX</span></span>

### <span data-ttu-id="27e34-106">StringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="27e34-106">StringParameterSet (Default)</span></span>
```
Reset-AzStorageSyncServerCertificate [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27e34-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="27e34-107">ObjectParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentObject] <PSStorageSyncService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27e34-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="27e34-108">ParentStringParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27e34-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="27e34-109">DESCRIPTION</span></span>
<span data-ttu-id="27e34-110">Эта команда позволит свернуть сертификат сервера синхронизации хранилища, используемый для описания удостоверения сервера, в службу синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="27e34-110">This command will roll storage sync server certificate used to describe the server identity to the storage sync service.</span></span> <span data-ttu-id="27e34-111">Этот вариант предназначен для использования в сценариях устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="27e34-111">This is meant for to be used in troubleshooting scenarios.</span></span> <span data-ttu-id="27e34-112">При вызове этой команды сертификат сервера заменяется. Обновление службы синхронизации хранилища, зарегистрированной на этом сервере, путем отправки открытой части ключа.</span><span class="sxs-lookup"><span data-stu-id="27e34-112">When calling this command, the server certificate is replaced, updating the storage sync service this server is registered with as well, by submitting the public part of the key.</span></span> <span data-ttu-id="27e34-113">Так как создается новый сертификат, срок его действия также обновляется.</span><span class="sxs-lookup"><span data-stu-id="27e34-113">Since a new certificate is generated, the expiration time of this cert is also updated.</span></span> <span data-ttu-id="27e34-114">Эту команду также можно использовать для обновления просроченного сертификата.</span><span class="sxs-lookup"><span data-stu-id="27e34-114">This command can also be used to update an expired certificate.</span></span> <span data-ttu-id="27e34-115">Это может произойти, если сервер работает в автономном режиме в течение длительного времени.</span><span class="sxs-lookup"><span data-stu-id="27e34-115">This can happen if a server is offline for an extended period of time.</span></span>

## <span data-ttu-id="27e34-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="27e34-116">EXAMPLES</span></span>

### <span data-ttu-id="27e34-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="27e34-117">Example 1</span></span>
```powershell
PS C:\> Reset-AzStorageSyncServerCertificate -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="27e34-118">Эта команда позволит свести локальный сертификат сервера к службе синхронизации хранилища, чтобы защитить его удостоверение.</span><span class="sxs-lookup"><span data-stu-id="27e34-118">This command will roll the local server certificate and inform the corresponding storage sync service of the server's new identity, in a secure way.</span></span>

## <span data-ttu-id="27e34-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27e34-119">PARAMETERS</span></span>

### <span data-ttu-id="27e34-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27e34-120">-DefaultProfile</span></span>
<span data-ttu-id="27e34-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="27e34-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27e34-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="27e34-122">-ParentObject</span></span>
<span data-ttu-id="27e34-123">Объект StorageSyncService, обычно переданный через параметр.</span><span class="sxs-lookup"><span data-stu-id="27e34-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="27e34-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="27e34-124">-ParentResourceId</span></span>
<span data-ttu-id="27e34-125">ИД родительского ресурса StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="27e34-125">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="27e34-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27e34-126">-PassThru</span></span>
<span data-ttu-id="27e34-127">В обычном выполнении этот cmdlet не возвращает никакого значения для успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="27e34-127">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="27e34-128">Если для параметра PassThru задан параметр PassThru, то после успешного выполнения он будет записывать значение в конвейер.</span><span class="sxs-lookup"><span data-stu-id="27e34-128">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="27e34-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27e34-129">-ResourceGroupName</span></span>
<span data-ttu-id="27e34-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="27e34-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="27e34-131">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="27e34-131">-StorageSyncServiceName</span></span>
<span data-ttu-id="27e34-132">Имя службы StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="27e34-132">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="27e34-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27e34-133">-Confirm</span></span>
<span data-ttu-id="27e34-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="27e34-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27e34-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27e34-135">-WhatIf</span></span>
<span data-ttu-id="27e34-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27e34-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="27e34-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="27e34-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27e34-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27e34-138">CommonParameters</span></span>
<span data-ttu-id="27e34-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27e34-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27e34-140">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27e34-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27e34-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="27e34-141">INPUTS</span></span>

### <span data-ttu-id="27e34-142">System.String</span><span class="sxs-lookup"><span data-stu-id="27e34-142">System.String</span></span>

### <span data-ttu-id="27e34-143">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="27e34-143">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="27e34-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="27e34-144">OUTPUTS</span></span>

### <span data-ttu-id="27e34-145">System.Object</span><span class="sxs-lookup"><span data-stu-id="27e34-145">System.Object</span></span>
## <span data-ttu-id="27e34-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="27e34-146">NOTES</span></span>

## <span data-ttu-id="27e34-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="27e34-147">RELATED LINKS</span></span>
