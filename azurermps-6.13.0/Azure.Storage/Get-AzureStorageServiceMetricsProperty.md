---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceMetricsProperty.md
ms.openlocfilehash: fdd7a7c655b46eb3fc1ca8673fb8fb5f36dcd850
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561296"
---
# <span data-ttu-id="0467e-101">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="0467e-101">Get-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="0467e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0467e-102">SYNOPSIS</span></span>
<span data-ttu-id="0467e-103">Возвращает свойства метрик для службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="0467e-103">Gets metrics properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0467e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0467e-104">SYNTAX</span></span>

```
Get-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0467e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0467e-105">DESCRIPTION</span></span>
<span data-ttu-id="0467e-106">Командлет **Get-AzureStorageServiceMetricsProperty** получает свойства метрик для службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="0467e-106">The **Get-AzureStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="0467e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0467e-107">EXAMPLES</span></span>

### <span data-ttu-id="0467e-108">Пример 1: получение свойств метрик для службы больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="0467e-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="0467e-109">Эта команда получает свойства метрик для хранилища больших двоичных объектов для типа метрики "Часы".</span><span class="sxs-lookup"><span data-stu-id="0467e-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="0467e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0467e-110">PARAMETERS</span></span>

### <span data-ttu-id="0467e-111">-Context</span><span class="sxs-lookup"><span data-stu-id="0467e-111">-Context</span></span>
<span data-ttu-id="0467e-112">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="0467e-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="0467e-113">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="0467e-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="0467e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0467e-114">-DefaultProfile</span></span>
<span data-ttu-id="0467e-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0467e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0467e-116">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="0467e-116">-MetricsType</span></span>
<span data-ttu-id="0467e-117">Указывает тип метрики.</span><span class="sxs-lookup"><span data-stu-id="0467e-117">Specifies a metrics type.</span></span>
<span data-ttu-id="0467e-118">Этот командлет получает свойства метрик службы хранилища Azure для типа метрики, указанном в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="0467e-118">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="0467e-119">Допустимые значения этого параметра: hours и Minute.</span><span class="sxs-lookup"><span data-stu-id="0467e-119">The acceptable values for this parameter are: Hour and Minute.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.ServiceMetricsType
Parameter Sets: (All)
Aliases:
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0467e-120">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="0467e-120">-ServiceType</span></span>
<span data-ttu-id="0467e-121">Указывает тип службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="0467e-121">Specifies the storage service type.</span></span>
<span data-ttu-id="0467e-122">Этот командлет получает свойства метрик для типа, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="0467e-122">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="0467e-123">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0467e-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0467e-124">Большом</span><span class="sxs-lookup"><span data-stu-id="0467e-124">Blob</span></span> 
- <span data-ttu-id="0467e-125">Таблич</span><span class="sxs-lookup"><span data-stu-id="0467e-125">Table</span></span>
- <span data-ttu-id="0467e-126">Поместить</span><span class="sxs-lookup"><span data-stu-id="0467e-126">Queue</span></span>
- <span data-ttu-id="0467e-127">Файл. значение файла в настоящее время не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0467e-127">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="0467e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0467e-128">CommonParameters</span></span>
<span data-ttu-id="0467e-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0467e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0467e-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0467e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0467e-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0467e-131">INPUTS</span></span>

### <span data-ttu-id="0467e-132">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0467e-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0467e-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0467e-133">OUTPUTS</span></span>

### <span data-ttu-id="0467e-134">Microsoft. WindowsAzure. Storage. Shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="0467e-134">Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="0467e-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="0467e-135">NOTES</span></span>

## <span data-ttu-id="0467e-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0467e-136">RELATED LINKS</span></span>

[<span data-ttu-id="0467e-137">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="0467e-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="0467e-138">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="0467e-138">Set-AzureStorageServiceMetricsProperty</span></span>](./Set-AzureStorageServiceMetricsProperty.md)


