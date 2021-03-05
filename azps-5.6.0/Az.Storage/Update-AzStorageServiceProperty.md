---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/update-azstorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageServiceProperty.md
ms.openlocfilehash: 952f66bfffef4d8f7636098a8280cd26b6fc7f5d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973208"
---
# <span data-ttu-id="be0f0-101">Update-AzStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="be0f0-101">Update-AzStorageServiceProperty</span></span>

## <span data-ttu-id="be0f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be0f0-102">SYNOPSIS</span></span>
<span data-ttu-id="be0f0-103">Изменяет свойства службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="be0f0-103">Modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="be0f0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="be0f0-104">SYNTAX</span></span>

```
Update-AzStorageServiceProperty [-ServiceType] <StorageServiceType> [-DefaultServiceVersion <String>]
 [-PassThru] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="be0f0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="be0f0-105">DESCRIPTION</span></span>
<span data-ttu-id="be0f0-106">Для службы хранилища Azure свойства службы **Update-AzStorageServiceProperty** изменяется.</span><span class="sxs-lookup"><span data-stu-id="be0f0-106">The **Update-AzStorageServiceProperty** cmdlet modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="be0f0-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="be0f0-107">EXAMPLES</span></span>

### <span data-ttu-id="be0f0-108">Пример 1. Настройка службы BLOB-2017-04-17 по умолчанию</span><span class="sxs-lookup"><span data-stu-id="be0f0-108">Example 1: Set Blob Service DefaultServiceVersion to 2017-04-17</span></span>
```
C:\PS>Update-AzStorageServiceProperty -ServiceType Blob -DefaultServiceVersion 2017-04-17
```

<span data-ttu-id="be0f0-109">Эта команда для настройки службы BLOB-клиентов DefaultServiceVersion на 2017-04-17</span><span class="sxs-lookup"><span data-stu-id="be0f0-109">This command Set the DefaultServiceVersion of Blob Service to 2017-04-17</span></span>

## <span data-ttu-id="be0f0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be0f0-110">PARAMETERS</span></span>

### <span data-ttu-id="be0f0-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="be0f0-111">-Context</span></span>
<span data-ttu-id="be0f0-112">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="be0f0-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="be0f0-113">Для получения контекста хранилища используйте New-AzStorageContext управления.</span><span class="sxs-lookup"><span data-stu-id="be0f0-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="be0f0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be0f0-114">-DefaultProfile</span></span>
<span data-ttu-id="be0f0-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="be0f0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be0f0-116">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="be0f0-116">-DefaultServiceVersion</span></span>
<span data-ttu-id="be0f0-117">Значение DefaultServiceVersion указывает на версию, используемую по умолчанию для запросов к службе BLOB-потери, если версия входящих запросов не указана.</span><span class="sxs-lookup"><span data-stu-id="be0f0-117">DefaultServiceVersion indicates the default version to use for requests to the Blob service if an incoming request's version is not specified.</span></span> <span data-ttu-id="be0f0-118">Возможные значения: версия 2008-10-27 и более новые версии.</span><span class="sxs-lookup"><span data-stu-id="be0f0-118">Possible values include version 2008-10-27 and all more recent versions.</span></span> <span data-ttu-id="be0f0-119">Дополнительные сведения см. в https://docs.microsoft.com/rest/api/storageservices/versioning-for-the-az-storage-services</span><span class="sxs-lookup"><span data-stu-id="be0f0-119">See more details in https://docs.microsoft.com/rest/api/storageservices/versioning-for-the-az-storage-services</span></span>

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

### <span data-ttu-id="be0f0-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="be0f0-120">-PassThru</span></span>
<span data-ttu-id="be0f0-121">Отображение свойств службы</span><span class="sxs-lookup"><span data-stu-id="be0f0-121">Display ServiceProperties</span></span>

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

### <span data-ttu-id="be0f0-122">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="be0f0-122">-ServiceType</span></span>
<span data-ttu-id="be0f0-123">Тип службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="be0f0-123">Specifies the storage service type.</span></span>
<span data-ttu-id="be0f0-124">Этот cmdlet получает свойства ведения журнала для типа службы, указанного этим параметром.</span><span class="sxs-lookup"><span data-stu-id="be0f0-124">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="be0f0-125">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="be0f0-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="be0f0-126">BLOB</span><span class="sxs-lookup"><span data-stu-id="be0f0-126">Blob</span></span> 
- <span data-ttu-id="be0f0-127">Таблица</span><span class="sxs-lookup"><span data-stu-id="be0f0-127">Table</span></span>
- <span data-ttu-id="be0f0-128">Очередь</span><span class="sxs-lookup"><span data-stu-id="be0f0-128">Queue</span></span>
- <span data-ttu-id="be0f0-129">Файл</span><span class="sxs-lookup"><span data-stu-id="be0f0-129">File</span></span>

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

### <span data-ttu-id="be0f0-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be0f0-130">-Confirm</span></span>
<span data-ttu-id="be0f0-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be0f0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be0f0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be0f0-132">-WhatIf</span></span>
<span data-ttu-id="be0f0-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be0f0-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="be0f0-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="be0f0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be0f0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be0f0-135">CommonParameters</span></span>
<span data-ttu-id="be0f0-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be0f0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be0f0-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be0f0-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be0f0-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="be0f0-138">INPUTS</span></span>

### <span data-ttu-id="be0f0-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="be0f0-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="be0f0-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="be0f0-140">OUTPUTS</span></span>

### <span data-ttu-id="be0f0-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="be0f0-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="be0f0-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="be0f0-142">NOTES</span></span>

## <span data-ttu-id="be0f0-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="be0f0-143">RELATED LINKS</span></span>
