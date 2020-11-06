---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: B447E492-D87E-4DA3-A8B0-0BAF603CCC26
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Export-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Export-AzureRmRedisCache.md
ms.openlocfilehash: 0edfec1d98423f444b2291d43e6f2a3489e20b29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567530"
---
# <span data-ttu-id="a4228-101">Export-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a4228-101">Export-AzureRmRedisCache</span></span>

## <span data-ttu-id="a4228-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a4228-102">SYNOPSIS</span></span>
<span data-ttu-id="a4228-103">Экспортирует данные из кэша Azure Redis в контейнер.</span><span class="sxs-lookup"><span data-stu-id="a4228-103">Exports data from Azure Redis Cache to a container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4228-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a4228-104">SYNTAX</span></span>

```
Export-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Prefix <String> -Container <String>
 [-Format <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4228-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4228-105">DESCRIPTION</span></span>
<span data-ttu-id="a4228-106">Командлет **Export-AzureRmRedisCache** экспортирует данные из кэша Azure Redis в контейнер.</span><span class="sxs-lookup"><span data-stu-id="a4228-106">The **Export-AzureRmRedisCache** cmdlet exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="a4228-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a4228-107">EXAMPLES</span></span>

### <span data-ttu-id="a4228-108">Пример 1: экспорт данных</span><span class="sxs-lookup"><span data-stu-id="a4228-108">Example 1: Export data</span></span>
```
PS C:\>Export-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Prefix "blobprefix" -Container "https://mystorageaccount.blob.core.windows.net/container18?sv=2015-04-05&sr=c&sig=HezZtBZ3DURmEGDduauE7pvETY4kqlPI8JCNa8ATmaw%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwdl"
```

<span data-ttu-id="a4228-109">Эта команда экспортирует данные из экземпляра кэша Azure Redis в контейнер, заданный URL-адресом SAS.</span><span class="sxs-lookup"><span data-stu-id="a4228-109">This command exports data from an Azure Redis Cache instance into the container that is specified by the SAS URL.</span></span>

## <span data-ttu-id="a4228-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a4228-110">PARAMETERS</span></span>

### <span data-ttu-id="a4228-111">-Container</span><span class="sxs-lookup"><span data-stu-id="a4228-111">-Container</span></span>
<span data-ttu-id="a4228-112">Указывает URL-адрес SAS службы контейнера, в котором этот командлет экспортирует данные.</span><span class="sxs-lookup"><span data-stu-id="a4228-112">Specifies the Service SAS URL of container where this cmdlet exports data.</span></span> <span data-ttu-id="a4228-113">URL-адрес служб SAS можно создать с помощью следующих команд PowerShell:</span><span class="sxs-lookup"><span data-stu-id="a4228-113">You can generate a Service SAS URL using the following PowerShell commands:</span></span>

<span data-ttu-id="a4228-114">$storageAccountContext = New-AzureStorageContext-StorageAccountName "storageName"-StorageAccountKey "</span><span class="sxs-lookup"><span data-stu-id="a4228-114">$storageAccountContext = New-AzureStorageContext -StorageAccountName "storageName" -StorageAccountKey "key"</span></span>

<span data-ttu-id="a4228-115">$sasKeyForContainer = New-AzureStorageContainerSASToken-Name "containername" — разрешение "rwdl"-StartTime ([System. DateTime]:: Now). AddMinutes (-15)-ExpiryTime ([System. DateTime]:: Now). AddHours (5) — контекстный $storageAccountContext — FullUri</span><span class="sxs-lookup"><span data-stu-id="a4228-115">$sasKeyForContainer = New-AzureStorageContainerSASToken -Name "containername" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri</span></span> 

<span data-ttu-id="a4228-116">Export-AzureRmRedisCache-ResourceGroupName "ResourceGroupName"-Name "cacheName" — prefix "blobprefix"-Container ($sasKeyForContainer)</span><span class="sxs-lookup"><span data-stu-id="a4228-116">Export-AzureRmRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Prefix "blobprefix" -Container ($sasKeyForContainer)</span></span>

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

### <span data-ttu-id="a4228-117">-Format</span><span class="sxs-lookup"><span data-stu-id="a4228-117">-Format</span></span>
<span data-ttu-id="a4228-118">Задает формат большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="a4228-118">Specifies a format for the blob.</span></span>
<span data-ttu-id="a4228-119">В настоящее время RDB является единственным поддерживаемым форматом.</span><span class="sxs-lookup"><span data-stu-id="a4228-119">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="a4228-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a4228-120">-Name</span></span>
<span data-ttu-id="a4228-121">Указывает имя кэша.</span><span class="sxs-lookup"><span data-stu-id="a4228-121">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="a4228-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4228-122">-PassThru</span></span>
<span data-ttu-id="a4228-123">Указывает на то, что этот командлет возвращает логическое значение, которое указывает, успешно ли выполняется операция.</span><span class="sxs-lookup"><span data-stu-id="a4228-123">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="a4228-124">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a4228-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a4228-125">-Prefix (префикс)</span><span class="sxs-lookup"><span data-stu-id="a4228-125">-Prefix</span></span>
<span data-ttu-id="a4228-126">Задает префикс, который будет использоваться для имен BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="a4228-126">Specifies a prefix to use for blob names.</span></span>

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

### <span data-ttu-id="a4228-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4228-127">-ResourceGroupName</span></span>
<span data-ttu-id="a4228-128">Указывает имя группы ресурсов, содержащей кэш.</span><span class="sxs-lookup"><span data-stu-id="a4228-128">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="a4228-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4228-129">-DefaultProfile</span></span>
<span data-ttu-id="a4228-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a4228-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4228-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4228-131">CommonParameters</span></span>
<span data-ttu-id="a4228-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a4228-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4228-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4228-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4228-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a4228-134">INPUTS</span></span>

### <span data-ttu-id="a4228-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="a4228-135">None</span></span>
<span data-ttu-id="a4228-136">Вы можете передавать входные данные командлету по имени свойства, но не по значению.</span><span class="sxs-lookup"><span data-stu-id="a4228-136">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="a4228-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4228-137">OUTPUTS</span></span>

### <span data-ttu-id="a4228-138">Ничего</span><span class="sxs-lookup"><span data-stu-id="a4228-138">None</span></span>

## <span data-ttu-id="a4228-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="a4228-139">NOTES</span></span>
* <span data-ttu-id="a4228-140">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, Redis, кэш, Интернет, webapp, веб-сайт</span><span class="sxs-lookup"><span data-stu-id="a4228-140">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="a4228-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4228-141">RELATED LINKS</span></span>

[<span data-ttu-id="a4228-142">Import-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a4228-142">Import-AzureRmRedisCache</span></span>](./Import-AzureRmRedisCache.md)

[<span data-ttu-id="a4228-143">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a4228-143">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="a4228-144">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a4228-144">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="a4228-145">Сброс — AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a4228-145">Reset-AzureRmRedisCache</span></span>](./Reset-AzureRmRedisCache.md)

[<span data-ttu-id="a4228-146">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a4228-146">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


