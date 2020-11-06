---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: B447E492-D87E-4DA3-A8B0-0BAF603CCC26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/export-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Export-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Export-AzureRmRedisCache.md
ms.openlocfilehash: cd19fe8052ae95f547971452f4364f279f365cac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561591"
---
# <span data-ttu-id="84028-101">Export-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="84028-101">Export-AzureRmRedisCache</span></span>

## <span data-ttu-id="84028-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="84028-102">SYNOPSIS</span></span>
<span data-ttu-id="84028-103">Экспортирует данные из кэша Azure Redis в контейнер.</span><span class="sxs-lookup"><span data-stu-id="84028-103">Exports data from Azure Redis Cache to a container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84028-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="84028-104">SYNTAX</span></span>

```
Export-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> -Prefix <String> -Container <String>
 [-Format <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="84028-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="84028-105">DESCRIPTION</span></span>
<span data-ttu-id="84028-106">Командлет **Export-AzureRmRedisCache** экспортирует данные из кэша Azure Redis в контейнер.</span><span class="sxs-lookup"><span data-stu-id="84028-106">The **Export-AzureRmRedisCache** cmdlet exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="84028-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="84028-107">EXAMPLES</span></span>

### <span data-ttu-id="84028-108">Пример 1: экспорт данных</span><span class="sxs-lookup"><span data-stu-id="84028-108">Example 1: Export data</span></span>
```
PS C:\>Export-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Prefix "blobprefix" -Container "https://mystorageaccount.blob.core.windows.net/container18?sv=2015-04-05&sr=c&sig=HezZtBZ3DURmEGDduauE7pvETY4kqlPI8JCNa8ATmaw%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwdl"
```

<span data-ttu-id="84028-109">Эта команда экспортирует данные из экземпляра кэша Azure Redis в контейнер, заданный URL-адресом SAS.</span><span class="sxs-lookup"><span data-stu-id="84028-109">This command exports data from an Azure Redis Cache instance into the container that is specified by the SAS URL.</span></span>

## <span data-ttu-id="84028-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="84028-110">PARAMETERS</span></span>

### <span data-ttu-id="84028-111">-Container</span><span class="sxs-lookup"><span data-stu-id="84028-111">-Container</span></span>
<span data-ttu-id="84028-112">Указывает URL-адрес SAS службы контейнера, в котором этот командлет экспортирует данные.</span><span class="sxs-lookup"><span data-stu-id="84028-112">Specifies the Service SAS URL of container where this cmdlet exports data.</span></span> <span data-ttu-id="84028-113">URL-адрес служб SAS можно создать с помощью следующих команд PowerShell:</span><span class="sxs-lookup"><span data-stu-id="84028-113">You can generate a Service SAS URL using the following PowerShell commands:</span></span>

<span data-ttu-id="84028-114">$storageAccountContext = New-AzureStorageContext-StorageAccountName "storageName"-StorageAccountKey "</span><span class="sxs-lookup"><span data-stu-id="84028-114">$storageAccountContext = New-AzureStorageContext -StorageAccountName "storageName" -StorageAccountKey "key"</span></span>

<span data-ttu-id="84028-115">$sasKeyForContainer = New-AzureStorageContainerSASToken-Name "containername" — разрешение "rwdl"-StartTime ([System. DateTime]:: Now). AddMinutes (-15)-ExpiryTime ([System. DateTime]:: Now). AddHours (5) — контекстный $storageAccountContext — FullUri</span><span class="sxs-lookup"><span data-stu-id="84028-115">$sasKeyForContainer = New-AzureStorageContainerSASToken -Name "containername" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri</span></span> 

<span data-ttu-id="84028-116">Export-AzureRmRedisCache-ResourceGroupName "ResourceGroupName"-Name "cacheName" — prefix "blobprefix"-Container ($sasKeyForContainer)</span><span class="sxs-lookup"><span data-stu-id="84028-116">Export-AzureRmRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Prefix "blobprefix" -Container ($sasKeyForContainer)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84028-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84028-117">-DefaultProfile</span></span>
<span data-ttu-id="84028-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="84028-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84028-119">-Format</span><span class="sxs-lookup"><span data-stu-id="84028-119">-Format</span></span>
<span data-ttu-id="84028-120">Задает формат большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="84028-120">Specifies a format for the blob.</span></span>
<span data-ttu-id="84028-121">В настоящее время RDB является единственным поддерживаемым форматом.</span><span class="sxs-lookup"><span data-stu-id="84028-121">Currently rdb is the only supported format.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84028-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="84028-122">-Name</span></span>
<span data-ttu-id="84028-123">Указывает имя кэша.</span><span class="sxs-lookup"><span data-stu-id="84028-123">Specifies the name of a cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84028-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84028-124">-PassThru</span></span>
<span data-ttu-id="84028-125">Указывает на то, что этот командлет возвращает логическое значение, которое указывает, успешно ли выполняется операция.</span><span class="sxs-lookup"><span data-stu-id="84028-125">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="84028-126">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="84028-126">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84028-127">-Prefix (префикс)</span><span class="sxs-lookup"><span data-stu-id="84028-127">-Prefix</span></span>
<span data-ttu-id="84028-128">Задает префикс, который будет использоваться для имен BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="84028-128">Specifies a prefix to use for blob names.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84028-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84028-129">-ResourceGroupName</span></span>
<span data-ttu-id="84028-130">Указывает имя группы ресурсов, содержащей кэш.</span><span class="sxs-lookup"><span data-stu-id="84028-130">Specifies the name of the resource group that contains the cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84028-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="84028-131">-Confirm</span></span>
<span data-ttu-id="84028-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="84028-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84028-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84028-133">-WhatIf</span></span>
<span data-ttu-id="84028-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="84028-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="84028-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="84028-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84028-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84028-136">CommonParameters</span></span>
<span data-ttu-id="84028-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="84028-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84028-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84028-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84028-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="84028-139">INPUTS</span></span>

### <span data-ttu-id="84028-140">Ничего</span><span class="sxs-lookup"><span data-stu-id="84028-140">None</span></span>
<span data-ttu-id="84028-141">Вы можете передавать входные данные командлету по имени свойства, но не по значению.</span><span class="sxs-lookup"><span data-stu-id="84028-141">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="84028-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="84028-142">OUTPUTS</span></span>

### <span data-ttu-id="84028-143">Ничего</span><span class="sxs-lookup"><span data-stu-id="84028-143">None</span></span>

## <span data-ttu-id="84028-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="84028-144">NOTES</span></span>
* <span data-ttu-id="84028-145">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, Redis, кэш, Интернет, webapp, веб-сайт</span><span class="sxs-lookup"><span data-stu-id="84028-145">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="84028-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="84028-146">RELATED LINKS</span></span>

[<span data-ttu-id="84028-147">Import-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="84028-147">Import-AzureRmRedisCache</span></span>](./Import-AzureRmRedisCache.md)

[<span data-ttu-id="84028-148">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="84028-148">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="84028-149">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="84028-149">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="84028-150">Сброс — AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="84028-150">Reset-AzureRmRedisCache</span></span>](./Reset-AzureRmRedisCache.md)

[<span data-ttu-id="84028-151">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="84028-151">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


