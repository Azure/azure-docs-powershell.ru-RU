---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceProperty.md
ms.openlocfilehash: 28727ed903030c360b436edfac3d4cfb2a5d38ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565080"
---
# <span data-ttu-id="6e4bb-101">Get-AzureStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="6e4bb-101">Get-AzureStorageServiceProperty</span></span>

## <span data-ttu-id="6e4bb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6e4bb-102">SYNOPSIS</span></span>
<span data-ttu-id="6e4bb-103">Получает свойства служб хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="6e4bb-103">Gets properties for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e4bb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6e4bb-104">SYNTAX</span></span>

```
Get-AzureStorageServiceProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="6e4bb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e4bb-105">DESCRIPTION</span></span>
<span data-ttu-id="6e4bb-106">Командлет **Get-AzureStorageServiceProperty** получает свойства служб хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="6e4bb-106">The **Get-AzureStorageServiceProperty** cmdlet gets the properties for Azure Storage services.</span></span>

## <span data-ttu-id="6e4bb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6e4bb-107">EXAMPLES</span></span>

### <span data-ttu-id="6e4bb-108">Пример 1: получение свойства службы хранилища Azure для службы больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="6e4bb-108">Example 1: Get  Azure Storage services property of the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceProperty -ServiceType Blob

Logging.Version                     : 1.0
Logging.LoggingOperations           : None
Logging.RetentionDays               : 
HourMetrics.Version                 : 1.0
HourMetrics.MetricsLevel            : ServiceAndApi
HourMetrics.RetentionDays           : 7
MinuteMetrics.Version               : 1.0
MinuteMetrics.MetricsLevel          : None
MinuteMetrics.RetentionDays         : 
DeleteRetentionPolicy.Enabled       : True
DeleteRetentionPolicy.RetentionDays : 70
Cors                                : 
DefaultServiceVersion               : 2017-07-29

```

<span data-ttu-id="6e4bb-109">Эта команда получает свойство DefaultServiceVersion службы больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="6e4bb-109">This command gets DefaultServiceVersion property of the Blob service.</span></span>

## <span data-ttu-id="6e4bb-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6e4bb-110">PARAMETERS</span></span>

### <span data-ttu-id="6e4bb-111">-Context</span><span class="sxs-lookup"><span data-stu-id="6e4bb-111">-Context</span></span>
<span data-ttu-id="6e4bb-112">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="6e4bb-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="6e4bb-113">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="6e4bb-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e4bb-114">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="6e4bb-114">-ServiceType</span></span>
<span data-ttu-id="6e4bb-115">Указывает тип службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="6e4bb-115">Specifies the storage service type.</span></span>
<span data-ttu-id="6e4bb-116">Этот командлет получает свойства ведения журнала для типа службы, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="6e4bb-116">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="6e4bb-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="6e4bb-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6e4bb-118">Большом</span><span class="sxs-lookup"><span data-stu-id="6e4bb-118">Blob</span></span> 
- <span data-ttu-id="6e4bb-119">Таблич</span><span class="sxs-lookup"><span data-stu-id="6e4bb-119">Table</span></span>
- <span data-ttu-id="6e4bb-120">Поместить</span><span class="sxs-lookup"><span data-stu-id="6e4bb-120">Queue</span></span>
- <span data-ttu-id="6e4bb-121">Файл</span><span class="sxs-lookup"><span data-stu-id="6e4bb-121">File</span></span>

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e4bb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e4bb-122">CommonParameters</span></span>
<span data-ttu-id="6e4bb-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6e4bb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e4bb-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e4bb-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e4bb-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6e4bb-125">INPUTS</span></span>

### <span data-ttu-id="6e4bb-126">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6e4bb-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6e4bb-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e4bb-127">OUTPUTS</span></span>

### <span data-ttu-id="6e4bb-128">Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="6e4bb-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="6e4bb-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="6e4bb-129">NOTES</span></span>

## <span data-ttu-id="6e4bb-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6e4bb-130">RELATED LINKS</span></span>

