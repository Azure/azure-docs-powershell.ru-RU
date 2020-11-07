---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
ms.openlocfilehash: 408025a6cbd2c174d5f26158535699fbd1dc5cb9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728646"
---
# <span data-ttu-id="80cf8-101">Get-AzStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="80cf8-101">Get-AzStorageServiceProperty</span></span>

## <span data-ttu-id="80cf8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="80cf8-102">SYNOPSIS</span></span>
<span data-ttu-id="80cf8-103">Получает свойства служб хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="80cf8-103">Gets properties for Azure Storage services.</span></span>

## <span data-ttu-id="80cf8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="80cf8-104">SYNTAX</span></span>

```
Get-AzStorageServiceProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80cf8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="80cf8-105">DESCRIPTION</span></span>
<span data-ttu-id="80cf8-106">Командлет **Get-AzStorageServiceProperty** получает свойства служб хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="80cf8-106">The **Get-AzStorageServiceProperty** cmdlet gets the properties for Azure Storage services.</span></span>

## <span data-ttu-id="80cf8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="80cf8-107">EXAMPLES</span></span>

### <span data-ttu-id="80cf8-108">Пример 1: получение свойства службы хранилища Azure для службы больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="80cf8-108">Example 1: Get  Azure Storage services property of the Blob service</span></span>
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

<span data-ttu-id="80cf8-109">Эта команда получает свойство DefaultServiceVersion службы больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="80cf8-109">This command gets DefaultServiceVersion property of the Blob service.</span></span>

## <span data-ttu-id="80cf8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="80cf8-110">PARAMETERS</span></span>

### <span data-ttu-id="80cf8-111">-Context</span><span class="sxs-lookup"><span data-stu-id="80cf8-111">-Context</span></span>
<span data-ttu-id="80cf8-112">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="80cf8-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="80cf8-113">Чтобы получить контекст хранилища, используйте командлет New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="80cf8-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="80cf8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80cf8-114">-DefaultProfile</span></span>
<span data-ttu-id="80cf8-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="80cf8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80cf8-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="80cf8-116">-ServiceType</span></span>
<span data-ttu-id="80cf8-117">Указывает тип службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="80cf8-117">Specifies the storage service type.</span></span>
<span data-ttu-id="80cf8-118">Этот командлет получает свойства ведения журнала для типа службы, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="80cf8-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="80cf8-119">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="80cf8-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="80cf8-120">Большом</span><span class="sxs-lookup"><span data-stu-id="80cf8-120">Blob</span></span> 
- <span data-ttu-id="80cf8-121">Таблич</span><span class="sxs-lookup"><span data-stu-id="80cf8-121">Table</span></span>
- <span data-ttu-id="80cf8-122">Поместить</span><span class="sxs-lookup"><span data-stu-id="80cf8-122">Queue</span></span>
- <span data-ttu-id="80cf8-123">Файл</span><span class="sxs-lookup"><span data-stu-id="80cf8-123">File</span></span>

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

### <span data-ttu-id="80cf8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80cf8-124">CommonParameters</span></span>
<span data-ttu-id="80cf8-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="80cf8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80cf8-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80cf8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80cf8-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="80cf8-127">INPUTS</span></span>

### <span data-ttu-id="80cf8-128">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="80cf8-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="80cf8-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="80cf8-129">OUTPUTS</span></span>

### <span data-ttu-id="80cf8-130">Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="80cf8-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="80cf8-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="80cf8-131">NOTES</span></span>

## <span data-ttu-id="80cf8-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="80cf8-132">RELATED LINKS</span></span>
