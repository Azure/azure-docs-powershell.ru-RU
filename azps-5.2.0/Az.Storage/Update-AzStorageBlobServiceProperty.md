---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 84f2303b0907e05bfe03ffacf50f4bcd895500c1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412271"
---
# <span data-ttu-id="bb5d4-101">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="bb5d4-101">Update-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="bb5d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb5d4-102">SYNOPSIS</span></span>
<span data-ttu-id="bb5d4-103">Изменяет свойства службы для службы BLOB-объектов хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="bb5d4-103">Modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="bb5d4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bb5d4-104">SYNTAX</span></span>

### <span data-ttu-id="bb5d4-105">AccountName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bb5d4-105">AccountName (Default)</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultServiceVersion <String>] [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb5d4-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="bb5d4-106">AccountObject</span></span>
```
Update-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultServiceVersion <String>]
 [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb5d4-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="bb5d4-107">BlobServicePropertiesResourceId</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultServiceVersion <String>]
 [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb5d4-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb5d4-108">DESCRIPTION</span></span>
<span data-ttu-id="bb5d4-109">Для службы BLOB-объектов хранилища Azure свойства службы **Update-AzStorageBlobServiceProperty** изменяется.</span><span class="sxs-lookup"><span data-stu-id="bb5d4-109">The **Update-AzStorageBlobServiceProperty** cmdlet modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="bb5d4-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bb5d4-110">EXAMPLES</span></span>

### <span data-ttu-id="bb5d4-111">Пример 1. Настройка службы BLOB-2018 DefaultServiceVersion для 2018-03-28</span><span class="sxs-lookup"><span data-stu-id="bb5d4-111">Example 1: Set Blob service DefaultServiceVersion to 2018-03-28</span></span>
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -DefaultServiceVersion 2018-03-28 

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegroup
DefaultServiceVersion         : 2018-03-28
DeleteRetentionPolicy.Enabled : False
DeleteRetentionPolicy.Days    : 
RestorePolicy.Enabled         : 
RestorePolicy.Days            : 
ChangeFeed                    : 
IsVersioningEnabled           :
```

<span data-ttu-id="bb5d4-112">Эта команда задает для службы Blob Service DefaultServiceVersion значение 2018-03-28.</span><span class="sxs-lookup"><span data-stu-id="bb5d4-112">This command sets the DefaultServiceVersion of Blob Service to 2018-03-28.</span></span>

### <span data-ttu-id="bb5d4-113">Пример 2. Enable Changefeed в службе BLOB-хранилищ учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="bb5d4-113">Example 2: Enable Changefeed on Blob service of a Storage account</span></span>
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EnableChangeFeed $true

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegroup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : False
DeleteRetentionPolicy.Days    : 
RestorePolicy.Enabled         : 
RestorePolicy.Days            : 
ChangeFeed                    : True
IsVersioningEnabled           :
```

<span data-ttu-id="bb5d4-114">Эта команда позволяет использовать changefeed в службе BLOB-устройств службы поддержки веб-канала изменения учетной записи хранения в хранилище BLOB-устройств Azure, прослушивая учетную запись хранилища GPv2 или BLOB-хранилищ для всех событий создания, изменения или удаления BLOB-хранилищ.</span><span class="sxs-lookup"><span data-stu-id="bb5d4-114">This command enables Changefeed on Blob service of a Storage account Change feed support in Azure Blob Storage works by listening to a GPv2 or Blob storage account for any blob level creation, modification, or deletion events.</span></span> <span data-ttu-id="bb5d4-115">Затем он выводит упорядоченный журнал событий для BLOB-$blobchangefeed в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="bb5d4-115">It then outputs an ordered log of events for the blobs stored in the $blobchangefeed container within the storage account.</span></span> <span data-ttu-id="bb5d4-116">Последовательные изменения сохраняются в файле Apache Avro и обрабатываются асинхронно и пошагово.</span><span class="sxs-lookup"><span data-stu-id="bb5d4-116">The serialized changes are persisted as an Apache Avro file and can be processed asynchronously and incrementally.</span></span>

### <span data-ttu-id="bb5d4-117">Пример 3. Enable Versioning on Versioning on Blob service of a Storage account</span><span class="sxs-lookup"><span data-stu-id="bb5d4-117">Example 3: Enable Versioning on Blob service of a Storage account</span></span>
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -IsVersioningEnabled $true

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegroup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : False
DeleteRetentionPolicy.Days    : 
RestorePolicy.Enabled         : 
RestorePolicy.Days            : 
ChangeFeed                    : 
IsVersioningEnabled           : True
```

<span data-ttu-id="bb5d4-118">Эта команда включает возможность управления версиями в службе BLOB-хранилищ учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="bb5d4-118">This command enables Versioning on Blob service of a Storage account</span></span>

## <span data-ttu-id="bb5d4-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb5d4-119">PARAMETERS</span></span>

### <span data-ttu-id="bb5d4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb5d4-120">-DefaultProfile</span></span>
<span data-ttu-id="bb5d4-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bb5d4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb5d4-122">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="bb5d4-122">-DefaultServiceVersion</span></span>
<span data-ttu-id="bb5d4-123">Версия службы по умолчанию для настройки</span><span class="sxs-lookup"><span data-stu-id="bb5d4-123">Default Service Version to Set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb5d4-124">-EnableChangeFeed</span><span class="sxs-lookup"><span data-stu-id="bb5d4-124">-EnableChangeFeed</span></span>
<span data-ttu-id="bb5d4-125">Включите ведение журнала изменения веб-канала для учетной записи хранения, заключив $true, отключите его, заключив для $false.</span><span class="sxs-lookup"><span data-stu-id="bb5d4-125">Enable Change Feed logging for the storage account by set to $true, disable Change Feed logging by set to $false.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb5d4-126">-IsVersioningEnabled</span><span class="sxs-lookup"><span data-stu-id="bb5d4-126">-IsVersioningEnabled</span></span>
<span data-ttu-id="bb5d4-127">Если установлено это в этом случае, включено или настроено переключение версий.</span><span class="sxs-lookup"><span data-stu-id="bb5d4-127">Gets or sets versioning is enabled if set to true.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb5d4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb5d4-128">-ResourceGroupName</span></span>
<span data-ttu-id="bb5d4-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bb5d4-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb5d4-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb5d4-130">-ResourceId</span></span>
<span data-ttu-id="bb5d4-131">Ввести ИД ресурса учетной записи хранения или свойства службы BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="bb5d4-131">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb5d4-132">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="bb5d4-132">-StorageAccount</span></span>
<span data-ttu-id="bb5d4-133">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="bb5d4-133">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb5d4-134">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="bb5d4-134">-StorageAccountName</span></span>
<span data-ttu-id="bb5d4-135">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="bb5d4-135">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb5d4-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bb5d4-136">-Confirm</span></span>
<span data-ttu-id="bb5d4-137">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb5d4-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb5d4-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb5d4-138">-WhatIf</span></span>
<span data-ttu-id="bb5d4-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb5d4-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb5d4-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bb5d4-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb5d4-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb5d4-141">CommonParameters</span></span>
<span data-ttu-id="bb5d4-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb5d4-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb5d4-143">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb5d4-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb5d4-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bb5d4-144">INPUTS</span></span>

### <span data-ttu-id="bb5d4-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bb5d4-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="bb5d4-146">System.String</span><span class="sxs-lookup"><span data-stu-id="bb5d4-146">System.String</span></span>

## <span data-ttu-id="bb5d4-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bb5d4-147">OUTPUTS</span></span>

### <span data-ttu-id="bb5d4-148">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="bb5d4-148">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="bb5d4-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bb5d4-149">NOTES</span></span>

## <span data-ttu-id="bb5d4-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bb5d4-150">RELATED LINKS</span></span>
