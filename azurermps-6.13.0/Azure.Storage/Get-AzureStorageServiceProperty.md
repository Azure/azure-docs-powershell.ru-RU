---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceProperty.md
ms.openlocfilehash: a36b1f13f08cd94339f9791512d764a872019672
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566028"
---
# <span data-ttu-id="3bb23-101">Get-AzureStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="3bb23-101">Get-AzureStorageServiceProperty</span></span>

## <span data-ttu-id="3bb23-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3bb23-102">SYNOPSIS</span></span>
<span data-ttu-id="3bb23-103">Получает свойства служб хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="3bb23-103">Gets properties for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3bb23-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3bb23-104">SYNTAX</span></span>

```
Get-AzureStorageServiceProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3bb23-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3bb23-105">DESCRIPTION</span></span>
<span data-ttu-id="3bb23-106">Командлет **Get-AzureStorageServiceProperty** получает свойства служб хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="3bb23-106">The **Get-AzureStorageServiceProperty** cmdlet gets the properties for Azure Storage services.</span></span>

## <span data-ttu-id="3bb23-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3bb23-107">EXAMPLES</span></span>

### <span data-ttu-id="3bb23-108">Пример 1: получение свойства службы хранилища Azure для службы больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="3bb23-108">Example 1: Get  Azure Storage services property of the Blob service</span></span>
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

<span data-ttu-id="3bb23-109">Эта команда получает свойство DefaultServiceVersion службы больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="3bb23-109">This command gets DefaultServiceVersion property of the Blob service.</span></span>

## <span data-ttu-id="3bb23-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3bb23-110">PARAMETERS</span></span>

### <span data-ttu-id="3bb23-111">-Context</span><span class="sxs-lookup"><span data-stu-id="3bb23-111">-Context</span></span>
<span data-ttu-id="3bb23-112">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="3bb23-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3bb23-113">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="3bb23-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3bb23-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bb23-114">-DefaultProfile</span></span>
<span data-ttu-id="3bb23-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3bb23-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bb23-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="3bb23-116">-ServiceType</span></span>
<span data-ttu-id="3bb23-117">Указывает тип службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="3bb23-117">Specifies the storage service type.</span></span>
<span data-ttu-id="3bb23-118">Этот командлет получает свойства ведения журнала для типа службы, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="3bb23-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="3bb23-119">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3bb23-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3bb23-120">Большом</span><span class="sxs-lookup"><span data-stu-id="3bb23-120">Blob</span></span> 
- <span data-ttu-id="3bb23-121">Таблич</span><span class="sxs-lookup"><span data-stu-id="3bb23-121">Table</span></span>
- <span data-ttu-id="3bb23-122">Поместить</span><span class="sxs-lookup"><span data-stu-id="3bb23-122">Queue</span></span>
- <span data-ttu-id="3bb23-123">Файл</span><span class="sxs-lookup"><span data-stu-id="3bb23-123">File</span></span>

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

### <span data-ttu-id="3bb23-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bb23-124">CommonParameters</span></span>
<span data-ttu-id="3bb23-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3bb23-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bb23-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bb23-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bb23-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3bb23-127">INPUTS</span></span>

### <span data-ttu-id="3bb23-128">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3bb23-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3bb23-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3bb23-129">OUTPUTS</span></span>

### <span data-ttu-id="3bb23-130">Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="3bb23-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="3bb23-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="3bb23-131">NOTES</span></span>

## <span data-ttu-id="3bb23-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3bb23-132">RELATED LINKS</span></span>
