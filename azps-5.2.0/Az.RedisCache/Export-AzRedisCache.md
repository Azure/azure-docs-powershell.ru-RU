---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: B447E492-D87E-4DA3-A8B0-0BAF603CCC26
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/export-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Export-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Export-AzRedisCache.md
ms.openlocfilehash: fb44ca997fd3b7599c25c5ba986ed0ca0771b3e6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417532"
---
# <span data-ttu-id="3a346-101">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="3a346-101">Export-AzRedisCache</span></span>

## <span data-ttu-id="3a346-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a346-102">SYNOPSIS</span></span>
<span data-ttu-id="3a346-103">Экспорт данных из кэша Azure Redis в контейнер.</span><span class="sxs-lookup"><span data-stu-id="3a346-103">Exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="3a346-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3a346-104">SYNTAX</span></span>

```
Export-AzRedisCache [-ResourceGroupName <String>] -Name <String> -Prefix <String> -Container <String>
 [-Format <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3a346-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a346-105">DESCRIPTION</span></span>
<span data-ttu-id="3a346-106">С **его использованием** можно экспортировать данные из кэша Azure Redis в контейнер.</span><span class="sxs-lookup"><span data-stu-id="3a346-106">The **Export-AzRedisCache** cmdlet exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="3a346-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3a346-107">EXAMPLES</span></span>

### <span data-ttu-id="3a346-108">Пример 1. Экспорт данных</span><span class="sxs-lookup"><span data-stu-id="3a346-108">Example 1: Export data</span></span>
```
PS C:\>Export-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Prefix "blobprefix" -Container "https://mystorageaccount.blob.core.windows.net/container18?sv=2015-04-05&sr=c&sig=HezZtBZ3DURmEGDduauE7pvETY4kqlPI8JCNa8ATmaw%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwdl"
```

<span data-ttu-id="3a346-109">Эта команда экспортирует данные из кэша Azure Redis в контейнер, заданный URL-адресом SAS.</span><span class="sxs-lookup"><span data-stu-id="3a346-109">This command exports data from an Azure Redis Cache instance into the container that is specified by the SAS URL.</span></span>

## <span data-ttu-id="3a346-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a346-110">PARAMETERS</span></span>

### <span data-ttu-id="3a346-111">-Container</span><span class="sxs-lookup"><span data-stu-id="3a346-111">-Container</span></span>
<span data-ttu-id="3a346-112">Url-адрес SAS службы контейнера, в который этот cmdlet экспортирует данные.</span><span class="sxs-lookup"><span data-stu-id="3a346-112">Specifies the Service SAS URL of container where this cmdlet exports data.</span></span> <span data-ttu-id="3a346-113">URL-адрес SAS службы можно создать с помощью следующих команд PowerShell: $storageAccountContext = New-AzStorageContext -StorageAccountName "имяпамя" -StorageAccountKey "key" $sasKeyForContainer = New-AzStorageContainerSASToken -Name "containername" -Permission "rwdl" -StartTime ([System.DateTime]::Now). AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now). AddHours(5) -Context $storageAccountContext -FullUri Export-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Prefix "blobprefix" -Container ($sasKeyForContainer)</span><span class="sxs-lookup"><span data-stu-id="3a346-113">You can generate a Service SAS URL using the following PowerShell commands: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForContainer = New-AzStorageContainerSASToken -Name "containername" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Export-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Prefix "blobprefix" -Container ($sasKeyForContainer)</span></span>

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

### <span data-ttu-id="3a346-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a346-114">-DefaultProfile</span></span>
<span data-ttu-id="3a346-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3a346-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a346-116">-Format</span><span class="sxs-lookup"><span data-stu-id="3a346-116">-Format</span></span>
<span data-ttu-id="3a346-117">Формат BLOB-ля.</span><span class="sxs-lookup"><span data-stu-id="3a346-117">Specifies a format for the blob.</span></span>
<span data-ttu-id="3a346-118">В настоящее время поддерживается только RDB-формат.</span><span class="sxs-lookup"><span data-stu-id="3a346-118">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="3a346-119">-Name</span><span class="sxs-lookup"><span data-stu-id="3a346-119">-Name</span></span>
<span data-ttu-id="3a346-120">Указывает имя кэша.</span><span class="sxs-lookup"><span data-stu-id="3a346-120">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="3a346-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a346-121">-PassThru</span></span>
<span data-ttu-id="3a346-122">Указывает на то, что этот cmdlet возвращает boolean that indicates whether the operation succeeds (Успешно).</span><span class="sxs-lookup"><span data-stu-id="3a346-122">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="3a346-123">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="3a346-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3a346-124">-Префикс</span><span class="sxs-lookup"><span data-stu-id="3a346-124">-Prefix</span></span>
<span data-ttu-id="3a346-125">Указывает префикс, который будет применяться к именам BLOB-имен.</span><span class="sxs-lookup"><span data-stu-id="3a346-125">Specifies a prefix to use for blob names.</span></span>

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

### <span data-ttu-id="3a346-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a346-126">-ResourceGroupName</span></span>
<span data-ttu-id="3a346-127">Имя группы ресурсов, которая содержит кэш.</span><span class="sxs-lookup"><span data-stu-id="3a346-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="3a346-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a346-128">-Confirm</span></span>
<span data-ttu-id="3a346-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a346-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a346-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a346-130">-WhatIf</span></span>
<span data-ttu-id="3a346-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a346-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3a346-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3a346-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a346-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a346-133">CommonParameters</span></span>
<span data-ttu-id="3a346-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a346-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a346-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a346-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a346-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3a346-136">INPUTS</span></span>

### <span data-ttu-id="3a346-137">System.String</span><span class="sxs-lookup"><span data-stu-id="3a346-137">System.String</span></span>

## <span data-ttu-id="3a346-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3a346-138">OUTPUTS</span></span>

### <span data-ttu-id="3a346-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3a346-139">System.Boolean</span></span>

## <span data-ttu-id="3a346-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3a346-140">NOTES</span></span>
* <span data-ttu-id="3a346-141">Ключевые слова: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="3a346-141">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="3a346-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3a346-142">RELATED LINKS</span></span>

[<span data-ttu-id="3a346-143">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="3a346-143">Import-AzRedisCache</span></span>](./Import-AzRedisCache.md)

[<span data-ttu-id="3a346-144">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="3a346-144">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="3a346-145">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="3a346-145">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="3a346-146">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="3a346-146">Reset-AzRedisCache</span></span>](./Reset-AzRedisCache.md)

[<span data-ttu-id="3a346-147">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="3a346-147">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


