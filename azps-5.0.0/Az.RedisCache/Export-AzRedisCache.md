---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: B447E492-D87E-4DA3-A8B0-0BAF603CCC26
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/export-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Export-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Export-AzRedisCache.md
ms.openlocfilehash: fb44ca997fd3b7599c25c5ba986ed0ca0771b3e6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249163"
---
# <span data-ttu-id="8c9ff-101">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="8c9ff-101">Export-AzRedisCache</span></span>

## <span data-ttu-id="8c9ff-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8c9ff-102">SYNOPSIS</span></span>
<span data-ttu-id="8c9ff-103">Экспортирует данные из кэша Azure Redis в контейнер.</span><span class="sxs-lookup"><span data-stu-id="8c9ff-103">Exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="8c9ff-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8c9ff-104">SYNTAX</span></span>

```
Export-AzRedisCache [-ResourceGroupName <String>] -Name <String> -Prefix <String> -Container <String>
 [-Format <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8c9ff-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c9ff-105">DESCRIPTION</span></span>
<span data-ttu-id="8c9ff-106">Командлет **Export-AzRedisCache** экспортирует данные из кэша Azure Redis в контейнер.</span><span class="sxs-lookup"><span data-stu-id="8c9ff-106">The **Export-AzRedisCache** cmdlet exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="8c9ff-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8c9ff-107">EXAMPLES</span></span>

### <span data-ttu-id="8c9ff-108">Пример 1: экспорт данных</span><span class="sxs-lookup"><span data-stu-id="8c9ff-108">Example 1: Export data</span></span>
```
PS C:\>Export-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Prefix "blobprefix" -Container "https://mystorageaccount.blob.core.windows.net/container18?sv=2015-04-05&sr=c&sig=HezZtBZ3DURmEGDduauE7pvETY4kqlPI8JCNa8ATmaw%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwdl"
```

<span data-ttu-id="8c9ff-109">Эта команда экспортирует данные из экземпляра кэша Azure Redis в контейнер, заданный URL-адресом SAS.</span><span class="sxs-lookup"><span data-stu-id="8c9ff-109">This command exports data from an Azure Redis Cache instance into the container that is specified by the SAS URL.</span></span>

## <span data-ttu-id="8c9ff-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8c9ff-110">PARAMETERS</span></span>

### <span data-ttu-id="8c9ff-111">-Container</span><span class="sxs-lookup"><span data-stu-id="8c9ff-111">-Container</span></span>
<span data-ttu-id="8c9ff-112">Указывает URL-адрес SAS службы контейнера, в котором этот командлет экспортирует данные.</span><span class="sxs-lookup"><span data-stu-id="8c9ff-112">Specifies the Service SAS URL of container where this cmdlet exports data.</span></span> <span data-ttu-id="8c9ff-113">URL-адрес служб SAS можно создать с помощью следующих команд PowerShell: $storageAccountContext = New-AzStorageContext-StorageAccountName "storageName"-StorageAccountKey "Key" $sasKeyForContainer = New-AzStorageContainerSASToken-Name "containername" — разрешение "rwdl"-StartTime ([System. DateTime]:: Now). AddMinutes (-15)-ExpiryTime ([System. DateTime]:: Now). AddHours (5) — контекстный $storageAccountContext-FullUri Export-AzRedisCache-ResourceGroupName "ResourceGroupName"-Name "cacheName"-prefix "blobprefix"-Container ($sasKeyForContainer)</span><span class="sxs-lookup"><span data-stu-id="8c9ff-113">You can generate a Service SAS URL using the following PowerShell commands: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForContainer = New-AzStorageContainerSASToken -Name "containername" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Export-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Prefix "blobprefix" -Container ($sasKeyForContainer)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c9ff-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c9ff-114">-DefaultProfile</span></span>
<span data-ttu-id="8c9ff-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8c9ff-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c9ff-116">-Format</span><span class="sxs-lookup"><span data-stu-id="8c9ff-116">-Format</span></span>
<span data-ttu-id="8c9ff-117">Задает формат большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="8c9ff-117">Specifies a format for the blob.</span></span>
<span data-ttu-id="8c9ff-118">В настоящее время RDB является единственным поддерживаемым форматом.</span><span class="sxs-lookup"><span data-stu-id="8c9ff-118">Currently rdb is the only supported format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c9ff-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8c9ff-119">-Name</span></span>
<span data-ttu-id="8c9ff-120">Указывает имя кэша.</span><span class="sxs-lookup"><span data-stu-id="8c9ff-120">Specifies the name of a cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c9ff-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c9ff-121">-PassThru</span></span>
<span data-ttu-id="8c9ff-122">Указывает на то, что этот командлет возвращает логическое значение, которое указывает, успешно ли выполняется операция.</span><span class="sxs-lookup"><span data-stu-id="8c9ff-122">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="8c9ff-123">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="8c9ff-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8c9ff-124">-Prefix (префикс)</span><span class="sxs-lookup"><span data-stu-id="8c9ff-124">-Prefix</span></span>
<span data-ttu-id="8c9ff-125">Задает префикс, который будет использоваться для имен BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="8c9ff-125">Specifies a prefix to use for blob names.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c9ff-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c9ff-126">-ResourceGroupName</span></span>
<span data-ttu-id="8c9ff-127">Указывает имя группы ресурсов, содержащей кэш.</span><span class="sxs-lookup"><span data-stu-id="8c9ff-127">Specifies the name of the resource group that contains the cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c9ff-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c9ff-128">-Confirm</span></span>
<span data-ttu-id="8c9ff-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8c9ff-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c9ff-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c9ff-130">-WhatIf</span></span>
<span data-ttu-id="8c9ff-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8c9ff-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8c9ff-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8c9ff-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c9ff-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c9ff-133">CommonParameters</span></span>
<span data-ttu-id="8c9ff-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8c9ff-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c9ff-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c9ff-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c9ff-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8c9ff-136">INPUTS</span></span>

### <span data-ttu-id="8c9ff-137">System. String</span><span class="sxs-lookup"><span data-stu-id="8c9ff-137">System.String</span></span>

## <span data-ttu-id="8c9ff-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c9ff-138">OUTPUTS</span></span>

### <span data-ttu-id="8c9ff-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8c9ff-139">System.Boolean</span></span>

## <span data-ttu-id="8c9ff-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="8c9ff-140">NOTES</span></span>
* <span data-ttu-id="8c9ff-141">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, Redis, кэш, Интернет, webapp, веб-сайт</span><span class="sxs-lookup"><span data-stu-id="8c9ff-141">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="8c9ff-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8c9ff-142">RELATED LINKS</span></span>

[<span data-ttu-id="8c9ff-143">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="8c9ff-143">Import-AzRedisCache</span></span>](./Import-AzRedisCache.md)

[<span data-ttu-id="8c9ff-144">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="8c9ff-144">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="8c9ff-145">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="8c9ff-145">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="8c9ff-146">Сброс — AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="8c9ff-146">Reset-AzRedisCache</span></span>](./Reset-AzRedisCache.md)

[<span data-ttu-id="8c9ff-147">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="8c9ff-147">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


