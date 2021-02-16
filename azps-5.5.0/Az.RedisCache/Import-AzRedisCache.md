---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: BC00DEF9-6A93-4DF5-8E5B-C488551BA1D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/import-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Import-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Import-AzRedisCache.md
ms.openlocfilehash: 1f51f156a0f45b014e9ff521adb959bdbd86bef7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217876"
---
# <span data-ttu-id="ac724-101">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ac724-101">Import-AzRedisCache</span></span>

## <span data-ttu-id="ac724-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac724-102">SYNOPSIS</span></span>
<span data-ttu-id="ac724-103">Импорт данных из BLOB-точек в кэш Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="ac724-103">Imports data from blobs to Azure Redis Cache.</span></span>

## <span data-ttu-id="ac724-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ac724-104">SYNTAX</span></span>

```
Import-AzRedisCache [-ResourceGroupName <String>] -Name <String> -Files <String[]> [-Format <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac724-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac724-105">DESCRIPTION</span></span>
<span data-ttu-id="ac724-106">**Cmdlet Import-AzRedisCache** импортирует данные из BLOB-контейнеров в кэш Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="ac724-106">The **Import-AzRedisCache** cmdlet imports data from blobs into Azure Redis Cache.</span></span>

## <span data-ttu-id="ac724-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ac724-107">EXAMPLES</span></span>

### <span data-ttu-id="ac724-108">Пример 1. Импорт данных</span><span class="sxs-lookup"><span data-stu-id="ac724-108">Example 1: Import data</span></span>
```
PS C:\>Import-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Files @("https://mystorageaccount.blob.core.windows.net/container22/blobname?sv=2015-04-05&sr=b&sig=caIwutG2uDa0NZ8mjdNJdgOY8%2F8mhwRuGNdICU%2B0pI4%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwd") -Force
```

<span data-ttu-id="ac724-109">Эта команда импортирует данные из BLOB-сайта, заданного URL-адресом SAS, в кэш Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="ac724-109">This command imports data from the blob that is specified by the SAS URL into Azure Redis Cache.</span></span>

## <span data-ttu-id="ac724-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac724-110">PARAMETERS</span></span>

### <span data-ttu-id="ac724-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac724-111">-DefaultProfile</span></span>
<span data-ttu-id="ac724-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ac724-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac724-113">-Файлы</span><span class="sxs-lookup"><span data-stu-id="ac724-113">-Files</span></span>
<span data-ttu-id="ac724-114">Url-адреса SAS для BLOB-адресов, содержимое которых этот cmdlet импортирует в кэш.</span><span class="sxs-lookup"><span data-stu-id="ac724-114">Specifies the SAS URLs of blobs whose content this cmdlet imports into the cache.</span></span> <span data-ttu-id="ac724-115">URL-адреса SAS можно создавать с помощью следующих команд PowerShell: $storageAccountContext = New-AzStorageContext -StorageAccountName "имяпамя" -StorageAccountKey "key" $sasKeyForBlob = New-AzStorageBlobSASToken -Container "containerName" -blob "blobName" -Permission "rwdl" -StartTime ([System.DateTime]::Now). AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now). AddHours(5) -Context $storageAccountContext -FullUri Import-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Files ($sasKeyForBlob) -Force</span><span class="sxs-lookup"><span data-stu-id="ac724-115">You can generate the SAS URLs using the following PowerShell commands: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForBlob = New-AzStorageBlobSASToken -Container "containerName" -blob "blobName" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Import-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Files ($sasKeyForBlob) -Force</span></span>

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

### <span data-ttu-id="ac724-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ac724-116">-Force</span></span>
<span data-ttu-id="ac724-117">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="ac724-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ac724-118">-Format</span><span class="sxs-lookup"><span data-stu-id="ac724-118">-Format</span></span>
<span data-ttu-id="ac724-119">Формат BLOB-ля.</span><span class="sxs-lookup"><span data-stu-id="ac724-119">Specifies the format of the blob.</span></span>
<span data-ttu-id="ac724-120">В настоящее время поддерживается только RDB-формат.</span><span class="sxs-lookup"><span data-stu-id="ac724-120">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="ac724-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ac724-121">-Name</span></span>
<span data-ttu-id="ac724-122">Указывает имя кэша.</span><span class="sxs-lookup"><span data-stu-id="ac724-122">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="ac724-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac724-123">-PassThru</span></span>
<span data-ttu-id="ac724-124">Указывает на то, что этот cmdlet возвращает boolean that indicates whether the operation succeeds (Успешно).</span><span class="sxs-lookup"><span data-stu-id="ac724-124">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="ac724-125">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ac724-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ac724-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac724-126">-ResourceGroupName</span></span>
<span data-ttu-id="ac724-127">Имя группы ресурсов, которая содержит кэш.</span><span class="sxs-lookup"><span data-stu-id="ac724-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="ac724-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac724-128">-Confirm</span></span>
<span data-ttu-id="ac724-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ac724-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac724-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac724-130">-WhatIf</span></span>
<span data-ttu-id="ac724-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac724-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac724-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ac724-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac724-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac724-133">CommonParameters</span></span>
<span data-ttu-id="ac724-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac724-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac724-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac724-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac724-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ac724-136">INPUTS</span></span>

### <span data-ttu-id="ac724-137">System.String</span><span class="sxs-lookup"><span data-stu-id="ac724-137">System.String</span></span>

### <span data-ttu-id="ac724-138">System.String[]</span><span class="sxs-lookup"><span data-stu-id="ac724-138">System.String[]</span></span>

## <span data-ttu-id="ac724-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ac724-139">OUTPUTS</span></span>

### <span data-ttu-id="ac724-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ac724-140">System.Boolean</span></span>

## <span data-ttu-id="ac724-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ac724-141">NOTES</span></span>
* <span data-ttu-id="ac724-142">Ключевые слова: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="ac724-142">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="ac724-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ac724-143">RELATED LINKS</span></span>

[<span data-ttu-id="ac724-144">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ac724-144">Export-AzRedisCache</span></span>](./Export-AzRedisCache.md)

[<span data-ttu-id="ac724-145">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ac724-145">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="ac724-146">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ac724-146">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="ac724-147">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ac724-147">Reset-AzRedisCache</span></span>](./Reset-AzRedisCache.md)

[<span data-ttu-id="ac724-148">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ac724-148">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


