---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: BC00DEF9-6A93-4DF5-8E5B-C488551BA1D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/import-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Import-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Import-AzRedisCache.md
ms.openlocfilehash: 018518f359c1142f9e20536f795b9080a942beaa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904786"
---
# <span data-ttu-id="c133b-101">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c133b-101">Import-AzRedisCache</span></span>

## <span data-ttu-id="c133b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c133b-102">SYNOPSIS</span></span>
<span data-ttu-id="c133b-103">Импорт данных из больших двоичных объектов в Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="c133b-103">Imports data from blobs to Azure Redis Cache.</span></span>

## <span data-ttu-id="c133b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c133b-104">SYNTAX</span></span>

```
Import-AzRedisCache [-ResourceGroupName <String>] -Name <String> -Files <String[]> [-Format <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c133b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c133b-105">DESCRIPTION</span></span>
<span data-ttu-id="c133b-106">Командлет **Import-AzRedisCache** импортирует данные из больших двоичных объектов в Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="c133b-106">The **Import-AzRedisCache** cmdlet imports data from blobs into Azure Redis Cache.</span></span>

## <span data-ttu-id="c133b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c133b-107">EXAMPLES</span></span>

### <span data-ttu-id="c133b-108">Пример 1: импорт данных</span><span class="sxs-lookup"><span data-stu-id="c133b-108">Example 1: Import data</span></span>
```
PS C:\>Import-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Files @("https://mystorageaccount.blob.core.windows.net/container22/blobname?sv=2015-04-05&sr=b&sig=caIwutG2uDa0NZ8mjdNJdgOY8%2F8mhwRuGNdICU%2B0pI4%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwd") -Force
```

<span data-ttu-id="c133b-109">Эта команда импортирует данные из большого двоичного объекта, заданного URL-адресом SAS, в кэш Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="c133b-109">This command imports data from the blob that is specified by the SAS URL into Azure Redis Cache.</span></span>

## <span data-ttu-id="c133b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c133b-110">PARAMETERS</span></span>

### <span data-ttu-id="c133b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c133b-111">-DefaultProfile</span></span>
<span data-ttu-id="c133b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c133b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c133b-113">-Файлы</span><span class="sxs-lookup"><span data-stu-id="c133b-113">-Files</span></span>
<span data-ttu-id="c133b-114">Указывает URL-адреса SAS для больших двоичных объектов, содержимое которых этот командлет импортирует в кэш.</span><span class="sxs-lookup"><span data-stu-id="c133b-114">Specifies the SAS URLs of blobs whose content this cmdlet imports into the cache.</span></span> <span data-ttu-id="c133b-115">URL-адреса SAS можно создать с помощью следующих команд PowerShell: $storageAccountContext = New-AzStorageContext-StorageAccountName "storageName"-StorageAccountKey "Key" $sasKeyForBlob = New-AzStorageBlobSASToken-Container "blobName" — разрешение "rwdl"-StartTime ([System. DateTime]:: Now). AddMinutes (-15)-ExpiryTime ([System. DateTime]:: Now). AddHours (5) — контекстный $storageAccountContext-FullUri Import-AzRedisCache-ResourceGroupName "ResourceGroupName"-Name "cacheName"-Files ($sasKeyForBlob) — Force</span><span class="sxs-lookup"><span data-stu-id="c133b-115">You can generate the SAS URLs using the following PowerShell commands: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForBlob = New-AzStorageBlobSASToken -Container "containerName" -blob "blobName" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Import-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Files ($sasKeyForBlob) -Force</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c133b-116">-Force</span><span class="sxs-lookup"><span data-stu-id="c133b-116">-Force</span></span>
<span data-ttu-id="c133b-117">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="c133b-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c133b-118">-Format</span><span class="sxs-lookup"><span data-stu-id="c133b-118">-Format</span></span>
<span data-ttu-id="c133b-119">Задает формат большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="c133b-119">Specifies the format of the blob.</span></span>
<span data-ttu-id="c133b-120">В настоящее время RDB является единственным поддерживаемым форматом.</span><span class="sxs-lookup"><span data-stu-id="c133b-120">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="c133b-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c133b-121">-Name</span></span>
<span data-ttu-id="c133b-122">Указывает имя кэша.</span><span class="sxs-lookup"><span data-stu-id="c133b-122">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="c133b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c133b-123">-PassThru</span></span>
<span data-ttu-id="c133b-124">Указывает на то, что этот командлет возвращает логическое значение, которое указывает, успешно ли выполняется операция.</span><span class="sxs-lookup"><span data-stu-id="c133b-124">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="c133b-125">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="c133b-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c133b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c133b-126">-ResourceGroupName</span></span>
<span data-ttu-id="c133b-127">Указывает имя группы ресурсов, содержащей кэш.</span><span class="sxs-lookup"><span data-stu-id="c133b-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="c133b-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c133b-128">-Confirm</span></span>
<span data-ttu-id="c133b-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c133b-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c133b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c133b-130">-WhatIf</span></span>
<span data-ttu-id="c133b-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c133b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c133b-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c133b-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c133b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c133b-133">CommonParameters</span></span>
<span data-ttu-id="c133b-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c133b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c133b-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c133b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c133b-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c133b-136">INPUTS</span></span>

### <span data-ttu-id="c133b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c133b-137">System.String</span></span>

### <span data-ttu-id="c133b-138">System. String []</span><span class="sxs-lookup"><span data-stu-id="c133b-138">System.String[]</span></span>

## <span data-ttu-id="c133b-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c133b-139">OUTPUTS</span></span>

### <span data-ttu-id="c133b-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c133b-140">System.Boolean</span></span>

## <span data-ttu-id="c133b-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="c133b-141">NOTES</span></span>
* <span data-ttu-id="c133b-142">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, Redis, кэш, Интернет, webapp, веб-сайт</span><span class="sxs-lookup"><span data-stu-id="c133b-142">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="c133b-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c133b-143">RELATED LINKS</span></span>

[<span data-ttu-id="c133b-144">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c133b-144">Export-AzRedisCache</span></span>](./Export-AzRedisCache.md)

[<span data-ttu-id="c133b-145">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c133b-145">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="c133b-146">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c133b-146">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="c133b-147">Сброс — AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c133b-147">Reset-AzRedisCache</span></span>](./Reset-AzRedisCache.md)

[<span data-ttu-id="c133b-148">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c133b-148">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


