---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceMetricsProperty.md
ms.openlocfilehash: 9d7e8f5d69d2f0e570cd7ce7fb21b29eb7f11648
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565082"
---
# <span data-ttu-id="509e9-101">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="509e9-101">Get-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="509e9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="509e9-102">SYNOPSIS</span></span>
<span data-ttu-id="509e9-103">Возвращает свойства метрик для службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="509e9-103">Gets metrics properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="509e9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="509e9-104">SYNTAX</span></span>

```
Get-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="509e9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="509e9-105">DESCRIPTION</span></span>
<span data-ttu-id="509e9-106">Командлет **Get-AzureStorageServiceMetricsProperty** получает свойства метрик для службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="509e9-106">The **Get-AzureStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="509e9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="509e9-107">EXAMPLES</span></span>

### <span data-ttu-id="509e9-108">Пример 1: получение свойств метрик для службы больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="509e9-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="509e9-109">Эта команда получает свойства метрик для хранилища больших двоичных объектов для типа метрики "Часы".</span><span class="sxs-lookup"><span data-stu-id="509e9-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="509e9-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="509e9-110">PARAMETERS</span></span>

### <span data-ttu-id="509e9-111">-Context</span><span class="sxs-lookup"><span data-stu-id="509e9-111">-Context</span></span>
<span data-ttu-id="509e9-112">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="509e9-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="509e9-113">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="509e9-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="509e9-114">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="509e9-114">-MetricsType</span></span>
<span data-ttu-id="509e9-115">Указывает тип метрики.</span><span class="sxs-lookup"><span data-stu-id="509e9-115">Specifies a metrics type.</span></span>
<span data-ttu-id="509e9-116">Этот командлет получает свойства метрик службы хранилища Azure для типа метрики, указанном в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="509e9-116">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="509e9-117">Допустимые значения этого параметра: hours и Minute.</span><span class="sxs-lookup"><span data-stu-id="509e9-117">The acceptable values for this parameter are: Hour and Minute.</span></span>

```yaml
Type: ServiceMetricsType
Parameter Sets: (All)
Aliases: 
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="509e9-118">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="509e9-118">-ServiceType</span></span>
<span data-ttu-id="509e9-119">Указывает тип службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="509e9-119">Specifies the storage service type.</span></span>
<span data-ttu-id="509e9-120">Этот командлет получает свойства метрик для типа, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="509e9-120">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="509e9-121">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="509e9-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="509e9-122">Большом</span><span class="sxs-lookup"><span data-stu-id="509e9-122">Blob</span></span> 
- <span data-ttu-id="509e9-123">Таблич</span><span class="sxs-lookup"><span data-stu-id="509e9-123">Table</span></span>
- <span data-ttu-id="509e9-124">Поместить</span><span class="sxs-lookup"><span data-stu-id="509e9-124">Queue</span></span>
- <span data-ttu-id="509e9-125">Файл</span><span class="sxs-lookup"><span data-stu-id="509e9-125">File</span></span> 

<span data-ttu-id="509e9-126">Значение "файл" в настоящее время не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="509e9-126">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="509e9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="509e9-127">CommonParameters</span></span>
<span data-ttu-id="509e9-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="509e9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="509e9-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="509e9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="509e9-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="509e9-130">INPUTS</span></span>

### <span data-ttu-id="509e9-131">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="509e9-131">IStorageContext</span></span>

<span data-ttu-id="509e9-132">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="509e9-132">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="509e9-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="509e9-133">OUTPUTS</span></span>

### <span data-ttu-id="509e9-134">Microsoft. WindowsAzure. Storage. Shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="509e9-134">Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="509e9-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="509e9-135">NOTES</span></span>

## <span data-ttu-id="509e9-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="509e9-136">RELATED LINKS</span></span>

[<span data-ttu-id="509e9-137">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="509e9-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="509e9-138">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="509e9-138">Set-AzureStorageServiceMetricsProperty</span></span>](./Set-AzureStorageServiceMetricsProperty.md)


