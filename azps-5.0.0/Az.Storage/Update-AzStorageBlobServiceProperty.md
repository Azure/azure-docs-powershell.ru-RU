---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 84f2303b0907e05bfe03ffacf50f4bcd895500c1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316889"
---
# <span data-ttu-id="b9060-101">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="b9060-101">Update-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="b9060-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b9060-102">SYNOPSIS</span></span>
<span data-ttu-id="b9060-103">Изменяет свойства службы для службы больших двоичных объектов хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="b9060-103">Modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="b9060-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b9060-104">SYNTAX</span></span>

### <span data-ttu-id="b9060-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b9060-105">AccountName (Default)</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultServiceVersion <String>] [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9060-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="b9060-106">AccountObject</span></span>
```
Update-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultServiceVersion <String>]
 [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9060-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="b9060-107">BlobServicePropertiesResourceId</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultServiceVersion <String>]
 [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9060-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9060-108">DESCRIPTION</span></span>
<span data-ttu-id="b9060-109">Командлет **Update-AzStorageBlobServiceProperty** изменяет свойства службы для службы BLOB-объектов хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="b9060-109">The **Update-AzStorageBlobServiceProperty** cmdlet modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="b9060-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b9060-110">EXAMPLES</span></span>

### <span data-ttu-id="b9060-111">Пример 1: Настройка службы BLOB-объектов DefaultServiceVersion в 2018-03-28</span><span class="sxs-lookup"><span data-stu-id="b9060-111">Example 1: Set Blob service DefaultServiceVersion to 2018-03-28</span></span>
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

<span data-ttu-id="b9060-112">Эта команда задает DefaultServiceVersion для службы больших двоичных объектов в 2018-03-28.</span><span class="sxs-lookup"><span data-stu-id="b9060-112">This command sets the DefaultServiceVersion of Blob Service to 2018-03-28.</span></span>

### <span data-ttu-id="b9060-113">Пример 2: включение changefeed в службе BLOB для учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="b9060-113">Example 2: Enable Changefeed on Blob service of a Storage account</span></span>
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

<span data-ttu-id="b9060-114">Эта команда включает changefeed в службе BLOB для учетной записи хранения в хранилище больших двоичных объектов Azure, прослушивая ее с помощью учетной записи хранения GPv2 или BLOB для событий создания, изменения и удаления уровня BLOB.</span><span class="sxs-lookup"><span data-stu-id="b9060-114">This command enables Changefeed on Blob service of a Storage account Change feed support in Azure Blob Storage works by listening to a GPv2 or Blob storage account for any blob level creation, modification, or deletion events.</span></span> <span data-ttu-id="b9060-115">Затем он выводит упорядоченный журнал событий для больших двоичных объектов, хранящихся в контейнере $blobchangefeed в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b9060-115">It then outputs an ordered log of events for the blobs stored in the $blobchangefeed container within the storage account.</span></span> <span data-ttu-id="b9060-116">Сериализованные изменения сохраняются как файл Apache Avro и могут обрабатываться асинхронно и инкрементно.</span><span class="sxs-lookup"><span data-stu-id="b9060-116">The serialized changes are persisted as an Apache Avro file and can be processed asynchronously and incrementally.</span></span>

### <span data-ttu-id="b9060-117">Пример 3: Включение управления версиями в службе BLOB для учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="b9060-117">Example 3: Enable Versioning on Blob service of a Storage account</span></span>
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

<span data-ttu-id="b9060-118">Эта команда включает управление версиями в службе BLOB для учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="b9060-118">This command enables Versioning on Blob service of a Storage account</span></span>

## <span data-ttu-id="b9060-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b9060-119">PARAMETERS</span></span>

### <span data-ttu-id="b9060-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9060-120">-DefaultProfile</span></span>
<span data-ttu-id="b9060-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b9060-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9060-122">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="b9060-122">-DefaultServiceVersion</span></span>
<span data-ttu-id="b9060-123">Версия службы по умолчанию для установки</span><span class="sxs-lookup"><span data-stu-id="b9060-123">Default Service Version to Set</span></span>

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

### <span data-ttu-id="b9060-124">-EnableChangeFeed</span><span class="sxs-lookup"><span data-stu-id="b9060-124">-EnableChangeFeed</span></span>
<span data-ttu-id="b9060-125">Включите ведение журнала изменений на веб-канале для учетной записи хранения, выбрав значение $true, отключите ведение журнала на веб-канале, выбрав значение $false.</span><span class="sxs-lookup"><span data-stu-id="b9060-125">Enable Change Feed logging for the storage account by set to $true, disable Change Feed logging by set to $false.</span></span>

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

### <span data-ttu-id="b9060-126">-IsVersioningEnabled</span><span class="sxs-lookup"><span data-stu-id="b9060-126">-IsVersioningEnabled</span></span>
<span data-ttu-id="b9060-127">Возвращает или задает параметр для управления версиями, если задано значение true.</span><span class="sxs-lookup"><span data-stu-id="b9060-127">Gets or sets versioning is enabled if set to true.</span></span>

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

### <span data-ttu-id="b9060-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9060-128">-ResourceGroupName</span></span>
<span data-ttu-id="b9060-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b9060-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="b9060-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9060-130">-ResourceId</span></span>
<span data-ttu-id="b9060-131">Введите идентификатор ресурса учетной записи хранения или идентификатор ресурса свойств службы BLOB.</span><span class="sxs-lookup"><span data-stu-id="b9060-131">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="b9060-132">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="b9060-132">-StorageAccount</span></span>
<span data-ttu-id="b9060-133">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="b9060-133">Storage account object</span></span>

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

### <span data-ttu-id="b9060-134">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b9060-134">-StorageAccountName</span></span>
<span data-ttu-id="b9060-135">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b9060-135">Storage Account Name.</span></span>

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

### <span data-ttu-id="b9060-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b9060-136">-Confirm</span></span>
<span data-ttu-id="b9060-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b9060-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9060-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9060-138">-WhatIf</span></span>
<span data-ttu-id="b9060-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b9060-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9060-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b9060-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9060-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9060-141">CommonParameters</span></span>
<span data-ttu-id="b9060-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b9060-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9060-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9060-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9060-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b9060-144">INPUTS</span></span>

### <span data-ttu-id="b9060-145">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b9060-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="b9060-146">System. String</span><span class="sxs-lookup"><span data-stu-id="b9060-146">System.String</span></span>

## <span data-ttu-id="b9060-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9060-147">OUTPUTS</span></span>

### <span data-ttu-id="b9060-148">Microsoft. Azure. Commands. Management. Storage. Models. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="b9060-148">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="b9060-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="b9060-149">NOTES</span></span>

## <span data-ttu-id="b9060-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9060-150">RELATED LINKS</span></span>
