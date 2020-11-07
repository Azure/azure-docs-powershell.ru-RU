---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/reset-Azstoragesyncservercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
ms.openlocfilehash: 4c27cc1cadb7d667793aa297303e539bd8db186f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728472"
---
# <span data-ttu-id="f33c4-101">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="f33c4-101">Reset-AzStorageSyncServerCertificate</span></span>

## <span data-ttu-id="f33c4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f33c4-102">SYNOPSIS</span></span>
<span data-ttu-id="f33c4-103">Используется только для устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="f33c4-103">Use for troubleshooting only.</span></span> <span data-ttu-id="f33c4-104">Эта команда выполняет откат сертификата сервера синхронизации хранилища, используемого для описания удостоверения сервера для службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="f33c4-104">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

## <span data-ttu-id="f33c4-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f33c4-105">SYNTAX</span></span>

### <span data-ttu-id="f33c4-106">ObjectParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f33c4-106">ObjectParameterSet (Default)</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentObject] <PSStorageSyncService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f33c4-107">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="f33c4-107">StringParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f33c4-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="f33c4-108">ParentStringParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f33c4-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f33c4-109">DESCRIPTION</span></span>
<span data-ttu-id="f33c4-110">Эта команда выполнит откат сертификата сервера синхронизации хранилища, используемого для описания удостоверения сервера для службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="f33c4-110">This command will roll storage sync server certificate used to describe the server identity to the storage sync service.</span></span> <span data-ttu-id="f33c4-111">Это предназначено для использования в сценариях устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="f33c4-111">This is meant for to be used in troubleshooting scenarios.</span></span> <span data-ttu-id="f33c4-112">При вызове этой команды серверный сертификат заменяется, обновляется служба синхронизации хранилища, который также регистрируется этим сервером, отправляя открытую часть ключа.</span><span class="sxs-lookup"><span data-stu-id="f33c4-112">When calling this command, the server certificate is replaced, updating the storage sync service this server is registered with as well, by submitting the public part of the key.</span></span> <span data-ttu-id="f33c4-113">После создания нового сертификата срок действия этого сертификата также обновляется.</span><span class="sxs-lookup"><span data-stu-id="f33c4-113">Since a new certificate is generated, the expiration time of this cert is also updated.</span></span> <span data-ttu-id="f33c4-114">Эту команду можно также использовать для обновления сертификата с истекшим сроком действия.</span><span class="sxs-lookup"><span data-stu-id="f33c4-114">This command can also be used to update an expired certificate.</span></span> <span data-ttu-id="f33c4-115">Это может происходить, если сервер работает в автономном режиме в течение длительного периода времени.</span><span class="sxs-lookup"><span data-stu-id="f33c4-115">This can happen if a server is offline for an extended period of time.</span></span>

## <span data-ttu-id="f33c4-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f33c4-116">EXAMPLES</span></span>

### <span data-ttu-id="f33c4-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f33c4-117">Example 1</span></span>
```powershell
PS C:\> Reset-AzStorageSyncServerCertificate -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="f33c4-118">Эта команда будет выполнять накат локального сертификата сервера и уведомлять соответствующую службу синхронизации хранилища нового удостоверения сервера в безопасном виде.</span><span class="sxs-lookup"><span data-stu-id="f33c4-118">This command will roll the local server certificate and inform the corresponding storage sync service of the server's new identity, in a secure way.</span></span>

## <span data-ttu-id="f33c4-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f33c4-119">PARAMETERS</span></span>

### <span data-ttu-id="f33c4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f33c4-120">-DefaultProfile</span></span>
<span data-ttu-id="f33c4-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f33c4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f33c4-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f33c4-122">-ParentObject</span></span>
<span data-ttu-id="f33c4-123">Объект StorageSyncService, обычно передаваемый через параметр.</span><span class="sxs-lookup"><span data-stu-id="f33c4-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="f33c4-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f33c4-124">-ParentResourceId</span></span>
<span data-ttu-id="f33c4-125">Идентификатор родительского ресурса StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="f33c4-125">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="f33c4-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f33c4-126">-PassThru</span></span>
<span data-ttu-id="f33c4-127">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="f33c4-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f33c4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f33c4-128">-ResourceGroupName</span></span>
<span data-ttu-id="f33c4-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f33c4-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="f33c4-130">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="f33c4-130">-StorageSyncServiceName</span></span>
<span data-ttu-id="f33c4-131">Имя StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="f33c4-131">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="f33c4-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f33c4-132">-Confirm</span></span>
<span data-ttu-id="f33c4-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f33c4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f33c4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f33c4-134">-WhatIf</span></span>
<span data-ttu-id="f33c4-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f33c4-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f33c4-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f33c4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f33c4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f33c4-137">CommonParameters</span></span>
<span data-ttu-id="f33c4-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f33c4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f33c4-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f33c4-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f33c4-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f33c4-140">INPUTS</span></span>

### <span data-ttu-id="f33c4-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f33c4-141">System.String</span></span>

### <span data-ttu-id="f33c4-142">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="f33c4-142">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="f33c4-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f33c4-143">OUTPUTS</span></span>

### <span data-ttu-id="f33c4-144">System. Object</span><span class="sxs-lookup"><span data-stu-id="f33c4-144">System.Object</span></span>
## <span data-ttu-id="f33c4-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="f33c4-145">NOTES</span></span>

## <span data-ttu-id="f33c4-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f33c4-146">RELATED LINKS</span></span>
