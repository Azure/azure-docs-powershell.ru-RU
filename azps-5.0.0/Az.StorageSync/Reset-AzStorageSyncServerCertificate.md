---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/reset-Azstoragesyncservercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
ms.openlocfilehash: 41caebb8b43c7c050aef2dac77daf51eebdaf42a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246000"
---
# <span data-ttu-id="dc34b-101">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="dc34b-101">Reset-AzStorageSyncServerCertificate</span></span>

## <span data-ttu-id="dc34b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dc34b-102">SYNOPSIS</span></span>
<span data-ttu-id="dc34b-103">Используется только для устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="dc34b-103">Use for troubleshooting only.</span></span> <span data-ttu-id="dc34b-104">Эта команда выполняет откат сертификата сервера синхронизации хранилища, используемого для описания удостоверения сервера для службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="dc34b-104">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

## <span data-ttu-id="dc34b-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dc34b-105">SYNTAX</span></span>

### <span data-ttu-id="dc34b-106">StringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dc34b-106">StringParameterSet (Default)</span></span>
```
Reset-AzStorageSyncServerCertificate [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc34b-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc34b-107">ObjectParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentObject] <PSStorageSyncService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc34b-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc34b-108">ParentStringParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc34b-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc34b-109">DESCRIPTION</span></span>
<span data-ttu-id="dc34b-110">Эта команда выполнит откат сертификата сервера синхронизации хранилища, используемого для описания удостоверения сервера для службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="dc34b-110">This command will roll storage sync server certificate used to describe the server identity to the storage sync service.</span></span> <span data-ttu-id="dc34b-111">Это предназначено для использования в сценариях устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="dc34b-111">This is meant for to be used in troubleshooting scenarios.</span></span> <span data-ttu-id="dc34b-112">При вызове этой команды серверный сертификат заменяется, обновляется служба синхронизации хранилища, который также регистрируется этим сервером, отправляя открытую часть ключа.</span><span class="sxs-lookup"><span data-stu-id="dc34b-112">When calling this command, the server certificate is replaced, updating the storage sync service this server is registered with as well, by submitting the public part of the key.</span></span> <span data-ttu-id="dc34b-113">После создания нового сертификата срок действия этого сертификата также обновляется.</span><span class="sxs-lookup"><span data-stu-id="dc34b-113">Since a new certificate is generated, the expiration time of this cert is also updated.</span></span> <span data-ttu-id="dc34b-114">Эту команду можно также использовать для обновления сертификата с истекшим сроком действия.</span><span class="sxs-lookup"><span data-stu-id="dc34b-114">This command can also be used to update an expired certificate.</span></span> <span data-ttu-id="dc34b-115">Это может происходить, если сервер работает в автономном режиме в течение длительного периода времени.</span><span class="sxs-lookup"><span data-stu-id="dc34b-115">This can happen if a server is offline for an extended period of time.</span></span>

## <span data-ttu-id="dc34b-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dc34b-116">EXAMPLES</span></span>

### <span data-ttu-id="dc34b-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dc34b-117">Example 1</span></span>
```powershell
PS C:\> Reset-AzStorageSyncServerCertificate -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="dc34b-118">Эта команда будет выполнять накат локального сертификата сервера и уведомлять соответствующую службу синхронизации хранилища нового удостоверения сервера в безопасном виде.</span><span class="sxs-lookup"><span data-stu-id="dc34b-118">This command will roll the local server certificate and inform the corresponding storage sync service of the server's new identity, in a secure way.</span></span>

## <span data-ttu-id="dc34b-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dc34b-119">PARAMETERS</span></span>

### <span data-ttu-id="dc34b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc34b-120">-DefaultProfile</span></span>
<span data-ttu-id="dc34b-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dc34b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc34b-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="dc34b-122">-ParentObject</span></span>
<span data-ttu-id="dc34b-123">Объект StorageSyncService, обычно передаваемый через параметр.</span><span class="sxs-lookup"><span data-stu-id="dc34b-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="dc34b-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="dc34b-124">-ParentResourceId</span></span>
<span data-ttu-id="dc34b-125">Идентификатор родительского ресурса StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="dc34b-125">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="dc34b-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc34b-126">-PassThru</span></span>
<span data-ttu-id="dc34b-127">При нормальном выполнении этот командлет не возвращает значение в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="dc34b-127">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="dc34b-128">Если вы предоставляете параметр PassThru, командлет запишет значение в конвейер после успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="dc34b-128">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="dc34b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc34b-129">-ResourceGroupName</span></span>
<span data-ttu-id="dc34b-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dc34b-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="dc34b-131">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="dc34b-131">-StorageSyncServiceName</span></span>
<span data-ttu-id="dc34b-132">Имя StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="dc34b-132">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="dc34b-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc34b-133">-Confirm</span></span>
<span data-ttu-id="dc34b-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dc34b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc34b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc34b-135">-WhatIf</span></span>
<span data-ttu-id="dc34b-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dc34b-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dc34b-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dc34b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc34b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc34b-138">CommonParameters</span></span>
<span data-ttu-id="dc34b-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dc34b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc34b-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc34b-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc34b-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dc34b-141">INPUTS</span></span>

### <span data-ttu-id="dc34b-142">System. String</span><span class="sxs-lookup"><span data-stu-id="dc34b-142">System.String</span></span>

### <span data-ttu-id="dc34b-143">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="dc34b-143">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="dc34b-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc34b-144">OUTPUTS</span></span>

### <span data-ttu-id="dc34b-145">System. Object</span><span class="sxs-lookup"><span data-stu-id="dc34b-145">System.Object</span></span>
## <span data-ttu-id="dc34b-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="dc34b-146">NOTES</span></span>

## <span data-ttu-id="dc34b-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc34b-147">RELATED LINKS</span></span>