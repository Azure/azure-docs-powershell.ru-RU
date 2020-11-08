---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
ms.openlocfilehash: aff976a684f5a002e2b55f1282dd60756f21f2f2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066750"
---
# <span data-ttu-id="a5b35-101">Get-AzStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="a5b35-101">Get-AzStorageServiceProperty</span></span>

## <span data-ttu-id="a5b35-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a5b35-102">SYNOPSIS</span></span>
<span data-ttu-id="a5b35-103">Получает свойства служб хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="a5b35-103">Gets properties for Azure Storage services.</span></span>

## <span data-ttu-id="a5b35-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a5b35-104">SYNTAX</span></span>

```
Get-AzStorageServiceProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5b35-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5b35-105">DESCRIPTION</span></span>
<span data-ttu-id="a5b35-106">Командлет **Get-AzStorageServiceProperty** получает свойства служб хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="a5b35-106">The **Get-AzStorageServiceProperty** cmdlet gets the properties for Azure Storage services.</span></span>

## <span data-ttu-id="a5b35-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a5b35-107">EXAMPLES</span></span>

### <span data-ttu-id="a5b35-108">Пример 1: получение свойства службы хранилища Azure для службы больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="a5b35-108">Example 1: Get  Azure Storage services property of the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceProperty -ServiceType Blob

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

<span data-ttu-id="a5b35-109">Эта команда получает свойство DefaultServiceVersion службы больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="a5b35-109">This command gets DefaultServiceVersion property of the Blob service.</span></span>

## <span data-ttu-id="a5b35-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a5b35-110">PARAMETERS</span></span>

### <span data-ttu-id="a5b35-111">-Context</span><span class="sxs-lookup"><span data-stu-id="a5b35-111">-Context</span></span>
<span data-ttu-id="a5b35-112">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="a5b35-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a5b35-113">Чтобы получить контекст хранилища, используйте командлет New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="a5b35-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a5b35-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5b35-114">-DefaultProfile</span></span>
<span data-ttu-id="a5b35-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a5b35-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5b35-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="a5b35-116">-ServiceType</span></span>
<span data-ttu-id="a5b35-117">Указывает тип службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="a5b35-117">Specifies the storage service type.</span></span>
<span data-ttu-id="a5b35-118">Этот командлет получает свойства ведения журнала для типа службы, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="a5b35-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="a5b35-119">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a5b35-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a5b35-120">Большом</span><span class="sxs-lookup"><span data-stu-id="a5b35-120">Blob</span></span> 
- <span data-ttu-id="a5b35-121">Таблич</span><span class="sxs-lookup"><span data-stu-id="a5b35-121">Table</span></span>
- <span data-ttu-id="a5b35-122">Поместить</span><span class="sxs-lookup"><span data-stu-id="a5b35-122">Queue</span></span>
- <span data-ttu-id="a5b35-123">Файл</span><span class="sxs-lookup"><span data-stu-id="a5b35-123">File</span></span>

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

### <span data-ttu-id="a5b35-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5b35-124">CommonParameters</span></span>
<span data-ttu-id="a5b35-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a5b35-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5b35-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5b35-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5b35-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a5b35-127">INPUTS</span></span>

### <span data-ttu-id="a5b35-128">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a5b35-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a5b35-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5b35-129">OUTPUTS</span></span>

### <span data-ttu-id="a5b35-130">Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="a5b35-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="a5b35-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="a5b35-131">NOTES</span></span>

## <span data-ttu-id="a5b35-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a5b35-132">RELATED LINKS</span></span>
