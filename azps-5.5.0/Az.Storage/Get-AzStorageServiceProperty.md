---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
ms.openlocfilehash: aff976a684f5a002e2b55f1282dd60756f21f2f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100212257"
---
# <span data-ttu-id="54a0f-101">Get-AzStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="54a0f-101">Get-AzStorageServiceProperty</span></span>

## <span data-ttu-id="54a0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54a0f-102">SYNOPSIS</span></span>
<span data-ttu-id="54a0f-103">Свойства служб хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="54a0f-103">Gets properties for Azure Storage services.</span></span>

## <span data-ttu-id="54a0f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="54a0f-104">SYNTAX</span></span>

```
Get-AzStorageServiceProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54a0f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54a0f-105">DESCRIPTION</span></span>
<span data-ttu-id="54a0f-106">Для служб хранилища Azure свойства служб **Get-AzStorageServiceProperty** получаются.</span><span class="sxs-lookup"><span data-stu-id="54a0f-106">The **Get-AzStorageServiceProperty** cmdlet gets the properties for Azure Storage services.</span></span>

## <span data-ttu-id="54a0f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="54a0f-107">EXAMPLES</span></span>

### <span data-ttu-id="54a0f-108">Пример 1. Получить свойство служб хранилища Azure для службы BLOB-объектов</span><span class="sxs-lookup"><span data-stu-id="54a0f-108">Example 1: Get  Azure Storage services property of the Blob service</span></span>
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

<span data-ttu-id="54a0f-109">Эта команда получает свойство DefaultServiceVersion службы BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="54a0f-109">This command gets DefaultServiceVersion property of the Blob service.</span></span>

## <span data-ttu-id="54a0f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54a0f-110">PARAMETERS</span></span>

### <span data-ttu-id="54a0f-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="54a0f-111">-Context</span></span>
<span data-ttu-id="54a0f-112">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="54a0f-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="54a0f-113">Для получения контекста хранилища используйте New-AzStorageContext управления.</span><span class="sxs-lookup"><span data-stu-id="54a0f-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="54a0f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54a0f-114">-DefaultProfile</span></span>
<span data-ttu-id="54a0f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="54a0f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54a0f-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="54a0f-116">-ServiceType</span></span>
<span data-ttu-id="54a0f-117">Тип службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="54a0f-117">Specifies the storage service type.</span></span>
<span data-ttu-id="54a0f-118">Этот cmdlet получает свойства ведения журнала для типа службы, указанного этим параметром.</span><span class="sxs-lookup"><span data-stu-id="54a0f-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="54a0f-119">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="54a0f-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="54a0f-120">BLOB</span><span class="sxs-lookup"><span data-stu-id="54a0f-120">Blob</span></span> 
- <span data-ttu-id="54a0f-121">Таблица</span><span class="sxs-lookup"><span data-stu-id="54a0f-121">Table</span></span>
- <span data-ttu-id="54a0f-122">Очередь</span><span class="sxs-lookup"><span data-stu-id="54a0f-122">Queue</span></span>
- <span data-ttu-id="54a0f-123">Файл</span><span class="sxs-lookup"><span data-stu-id="54a0f-123">File</span></span>

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

### <span data-ttu-id="54a0f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54a0f-124">CommonParameters</span></span>
<span data-ttu-id="54a0f-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54a0f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54a0f-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54a0f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54a0f-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="54a0f-127">INPUTS</span></span>

### <span data-ttu-id="54a0f-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="54a0f-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="54a0f-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="54a0f-129">OUTPUTS</span></span>

### <span data-ttu-id="54a0f-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="54a0f-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="54a0f-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="54a0f-131">NOTES</span></span>

## <span data-ttu-id="54a0f-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54a0f-132">RELATED LINKS</span></span>
