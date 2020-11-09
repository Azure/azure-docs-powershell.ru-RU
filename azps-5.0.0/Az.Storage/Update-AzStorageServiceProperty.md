---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageServiceProperty.md
ms.openlocfilehash: e94bb90ffeda257dd024c1cf9b834764455cd6aa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318302"
---
# <span data-ttu-id="f6015-101">Update-AzStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="f6015-101">Update-AzStorageServiceProperty</span></span>

## <span data-ttu-id="f6015-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f6015-102">SYNOPSIS</span></span>
<span data-ttu-id="f6015-103">Изменяет свойства службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="f6015-103">Modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="f6015-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f6015-104">SYNTAX</span></span>

```
Update-AzStorageServiceProperty [-ServiceType] <StorageServiceType> [-DefaultServiceVersion <String>]
 [-PassThru] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f6015-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6015-105">DESCRIPTION</span></span>
<span data-ttu-id="f6015-106">Командлет **Update-AzStorageServiceProperty** изменяет свойства службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="f6015-106">The **Update-AzStorageServiceProperty** cmdlet modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="f6015-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f6015-107">EXAMPLES</span></span>

### <span data-ttu-id="f6015-108">Пример 1: Настройка службы BLOB-объектов DefaultServiceVersion в 2017-04-17</span><span class="sxs-lookup"><span data-stu-id="f6015-108">Example 1: Set Blob Service DefaultServiceVersion to 2017-04-17</span></span>
```
C:\PS>Update-AzStorageServiceProperty -ServiceType Blob -DefaultServiceVersion 2017-04-17
```

<span data-ttu-id="f6015-109">Эта команда задает DefaultServiceVersion для службы больших двоичных объектов в 2017-04-17</span><span class="sxs-lookup"><span data-stu-id="f6015-109">This command Set the DefaultServiceVersion of Blob Service to 2017-04-17</span></span>

## <span data-ttu-id="f6015-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f6015-110">PARAMETERS</span></span>

### <span data-ttu-id="f6015-111">-Context</span><span class="sxs-lookup"><span data-stu-id="f6015-111">-Context</span></span>
<span data-ttu-id="f6015-112">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="f6015-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f6015-113">Чтобы получить контекст хранилища, используйте командлет New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="f6015-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6015-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6015-114">-DefaultProfile</span></span>
<span data-ttu-id="f6015-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f6015-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6015-116">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="f6015-116">-DefaultServiceVersion</span></span>
<span data-ttu-id="f6015-117">DefaultServiceVersion указывает версию по умолчанию, используемую для запросов к службе больших двоичных объектов, если не указана версия входящего запроса.</span><span class="sxs-lookup"><span data-stu-id="f6015-117">DefaultServiceVersion indicates the default version to use for requests to the Blob service if an incoming request's version is not specified.</span></span> <span data-ttu-id="f6015-118">Возможные значения включают версию 2008-10-27 и все более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="f6015-118">Possible values include version 2008-10-27 and all more recent versions.</span></span> <span data-ttu-id="f6015-119">Дополнительные сведения см. в разделе https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-az-storage-services</span><span class="sxs-lookup"><span data-stu-id="f6015-119">See more details in https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-az-storage-services</span></span>

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

### <span data-ttu-id="f6015-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f6015-120">-PassThru</span></span>
<span data-ttu-id="f6015-121">Показать ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="f6015-121">Display ServiceProperties</span></span>

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

### <span data-ttu-id="f6015-122">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="f6015-122">-ServiceType</span></span>
<span data-ttu-id="f6015-123">Указывает тип службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="f6015-123">Specifies the storage service type.</span></span>
<span data-ttu-id="f6015-124">Этот командлет получает свойства ведения журнала для типа службы, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="f6015-124">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="f6015-125">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f6015-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f6015-126">Большом</span><span class="sxs-lookup"><span data-stu-id="f6015-126">Blob</span></span> 
- <span data-ttu-id="f6015-127">Таблич</span><span class="sxs-lookup"><span data-stu-id="f6015-127">Table</span></span>
- <span data-ttu-id="f6015-128">Поместить</span><span class="sxs-lookup"><span data-stu-id="f6015-128">Queue</span></span>
- <span data-ttu-id="f6015-129">Файл</span><span class="sxs-lookup"><span data-stu-id="f6015-129">File</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6015-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6015-130">-Confirm</span></span>
<span data-ttu-id="f6015-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f6015-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6015-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6015-132">-WhatIf</span></span>
<span data-ttu-id="f6015-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f6015-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6015-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f6015-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6015-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6015-135">CommonParameters</span></span>
<span data-ttu-id="f6015-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f6015-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6015-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6015-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6015-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f6015-138">INPUTS</span></span>

### <span data-ttu-id="f6015-139">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f6015-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f6015-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6015-140">OUTPUTS</span></span>

### <span data-ttu-id="f6015-141">Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="f6015-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="f6015-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="f6015-142">NOTES</span></span>

## <span data-ttu-id="f6015-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f6015-143">RELATED LINKS</span></span>
