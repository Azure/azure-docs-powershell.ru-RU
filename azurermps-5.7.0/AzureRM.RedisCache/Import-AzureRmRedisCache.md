---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: BC00DEF9-6A93-4DF5-8E5B-C488551BA1D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/import-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Import-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Import-AzureRmRedisCache.md
ms.openlocfilehash: ff7ac13080d3d5cb717cf7efbff322cabf83cc3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561584"
---
# <span data-ttu-id="5ef6b-101">Import-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="5ef6b-101">Import-AzureRmRedisCache</span></span>

## <span data-ttu-id="5ef6b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5ef6b-102">SYNOPSIS</span></span>
<span data-ttu-id="5ef6b-103">Импорт данных из больших двоичных объектов в Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="5ef6b-103">Imports data from blobs to Azure Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ef6b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5ef6b-104">SYNTAX</span></span>

```
Import-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> -Files <String[]> [-Format <String>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ef6b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ef6b-105">DESCRIPTION</span></span>
<span data-ttu-id="5ef6b-106">Командлет **Import-AzureRmRedisCache** импортирует данные из больших двоичных объектов в Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="5ef6b-106">The **Import-AzureRmRedisCache** cmdlet imports data from blobs into Azure Redis Cache.</span></span>

## <span data-ttu-id="5ef6b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5ef6b-107">EXAMPLES</span></span>

### <span data-ttu-id="5ef6b-108">Пример 1: импорт данных</span><span class="sxs-lookup"><span data-stu-id="5ef6b-108">Example 1: Import data</span></span>
```
PS C:\>Import-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Files @("https://mystorageaccount.blob.core.windows.net/container22/blobname?sv=2015-04-05&sr=b&sig=caIwutG2uDa0NZ8mjdNJdgOY8%2F8mhwRuGNdICU%2B0pI4%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwd") -Force
```

<span data-ttu-id="5ef6b-109">Эта команда импортирует данные из большого двоичного объекта, заданного URL-адресом SAS, в кэш Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="5ef6b-109">This command imports data from the blob that is specified by the SAS URL into Azure Redis Cache.</span></span>

## <span data-ttu-id="5ef6b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5ef6b-110">PARAMETERS</span></span>

### <span data-ttu-id="5ef6b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ef6b-111">-DefaultProfile</span></span>
<span data-ttu-id="5ef6b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5ef6b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ef6b-113">-Файлы</span><span class="sxs-lookup"><span data-stu-id="5ef6b-113">-Files</span></span>
<span data-ttu-id="5ef6b-114">Указывает URL-адреса SAS для больших двоичных объектов, содержимое которых этот командлет импортирует в кэш.</span><span class="sxs-lookup"><span data-stu-id="5ef6b-114">Specifies the SAS URLs of blobs whose content this cmdlet imports into the cache.</span></span> <span data-ttu-id="5ef6b-115">URL-адреса SAS можно создать с помощью следующих команд PowerShell:</span><span class="sxs-lookup"><span data-stu-id="5ef6b-115">You can generate the SAS URLs using the following PowerShell commands:</span></span>

<span data-ttu-id="5ef6b-116">$storageAccountContext = New-AzureStorageContext-StorageAccountName "storageName"-StorageAccountKey "</span><span class="sxs-lookup"><span data-stu-id="5ef6b-116">$storageAccountContext = New-AzureStorageContext -StorageAccountName "storageName" -StorageAccountKey "key"</span></span>

<span data-ttu-id="5ef6b-117">$sasKeyForBlob = New-AzureStorageBlobSASToken-Container "containerName" — BLOB "blobName"-разрешение "rwdl"-StartTime ([System. DateTime]:: Now). AddMinutes (-15)-ExpiryTime ([System. DateTime]:: Now). AddHours (5) — контекстный $storageAccountContext — FullUri</span><span class="sxs-lookup"><span data-stu-id="5ef6b-117">$sasKeyForBlob = New-AzureStorageBlobSASToken -Container "containerName" -blob "blobName" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri</span></span>

<span data-ttu-id="5ef6b-118">Import-AzureRmRedisCache-ResourceGroupName "ResourceGroupName"-Names ($sasKeyForBlob) — Force</span><span class="sxs-lookup"><span data-stu-id="5ef6b-118">Import-AzureRmRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Files ($sasKeyForBlob) -Force</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ef6b-119">-Force</span><span class="sxs-lookup"><span data-stu-id="5ef6b-119">-Force</span></span>
<span data-ttu-id="5ef6b-120">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="5ef6b-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5ef6b-121">-Format</span><span class="sxs-lookup"><span data-stu-id="5ef6b-121">-Format</span></span>
<span data-ttu-id="5ef6b-122">Задает формат большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="5ef6b-122">Specifies the format of the blob.</span></span>
<span data-ttu-id="5ef6b-123">В настоящее время RDB является единственным поддерживаемым форматом.</span><span class="sxs-lookup"><span data-stu-id="5ef6b-123">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="5ef6b-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5ef6b-124">-Name</span></span>
<span data-ttu-id="5ef6b-125">Указывает имя кэша.</span><span class="sxs-lookup"><span data-stu-id="5ef6b-125">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="5ef6b-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ef6b-126">-PassThru</span></span>
<span data-ttu-id="5ef6b-127">Указывает на то, что этот командлет возвращает логическое значение, которое указывает, успешно ли выполняется операция.</span><span class="sxs-lookup"><span data-stu-id="5ef6b-127">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="5ef6b-128">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="5ef6b-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5ef6b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ef6b-129">-ResourceGroupName</span></span>
<span data-ttu-id="5ef6b-130">Указывает имя группы ресурсов, содержащей кэш.</span><span class="sxs-lookup"><span data-stu-id="5ef6b-130">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="5ef6b-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ef6b-131">-Confirm</span></span>
<span data-ttu-id="5ef6b-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5ef6b-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ef6b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ef6b-133">-WhatIf</span></span>
<span data-ttu-id="5ef6b-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5ef6b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ef6b-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5ef6b-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ef6b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ef6b-136">CommonParameters</span></span>
<span data-ttu-id="5ef6b-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5ef6b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ef6b-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ef6b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ef6b-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5ef6b-139">INPUTS</span></span>

### <span data-ttu-id="5ef6b-140">Ничего</span><span class="sxs-lookup"><span data-stu-id="5ef6b-140">None</span></span>
<span data-ttu-id="5ef6b-141">Вы можете передавать входные данные командлету по имени свойства, но не по значению.</span><span class="sxs-lookup"><span data-stu-id="5ef6b-141">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="5ef6b-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ef6b-142">OUTPUTS</span></span>

### <span data-ttu-id="5ef6b-143">Ничего</span><span class="sxs-lookup"><span data-stu-id="5ef6b-143">None</span></span>

## <span data-ttu-id="5ef6b-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="5ef6b-144">NOTES</span></span>
* <span data-ttu-id="5ef6b-145">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, Redis, кэш, Интернет, webapp, веб-сайт</span><span class="sxs-lookup"><span data-stu-id="5ef6b-145">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="5ef6b-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ef6b-146">RELATED LINKS</span></span>

[<span data-ttu-id="5ef6b-147">Export-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="5ef6b-147">Export-AzureRmRedisCache</span></span>](./Export-AzureRmRedisCache.md)

[<span data-ttu-id="5ef6b-148">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="5ef6b-148">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="5ef6b-149">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="5ef6b-149">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="5ef6b-150">Сброс — AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="5ef6b-150">Reset-AzureRmRedisCache</span></span>](./Reset-AzureRmRedisCache.md)

[<span data-ttu-id="5ef6b-151">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="5ef6b-151">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


