---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: ''
schema: 2.0.0
ms.openlocfilehash: b9117d5a4149842ffd136caf1c986c70a4b5e187
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556240"
---
# <span data-ttu-id="0d4ea-101">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="0d4ea-101">Get-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="0d4ea-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0d4ea-102">SYNOPSIS</span></span>
<span data-ttu-id="0d4ea-103">Возвращает свойства метрик для службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="0d4ea-103">Gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="0d4ea-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0d4ea-104">SYNTAX</span></span>

```
Get-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="0d4ea-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d4ea-105">DESCRIPTION</span></span>
<span data-ttu-id="0d4ea-106">Командлет **Get-AzureStorageServiceMetricsProperty** получает свойства метрик для службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="0d4ea-106">The **Get-AzureStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="0d4ea-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0d4ea-107">EXAMPLES</span></span>

### <span data-ttu-id="0d4ea-108">Пример 1: получение свойств метрик для службы больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="0d4ea-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="0d4ea-109">Эта команда получает свойства метрик для хранилища больших двоичных объектов для типа метрики "Часы".</span><span class="sxs-lookup"><span data-stu-id="0d4ea-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="0d4ea-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0d4ea-110">PARAMETERS</span></span>

### <span data-ttu-id="0d4ea-111">-Context</span><span class="sxs-lookup"><span data-stu-id="0d4ea-111">-Context</span></span>
<span data-ttu-id="0d4ea-112">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="0d4ea-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="0d4ea-113">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="0d4ea-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="0d4ea-114">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="0d4ea-114">-MetricsType</span></span>
<span data-ttu-id="0d4ea-115">Указывает тип метрики.</span><span class="sxs-lookup"><span data-stu-id="0d4ea-115">Specifies a metrics type.</span></span>
<span data-ttu-id="0d4ea-116">Этот командлет получает свойства метрик службы хранилища Azure для типа метрики, указанном в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="0d4ea-116">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="0d4ea-117">Допустимые значения этого параметра: hours и Minute.</span><span class="sxs-lookup"><span data-stu-id="0d4ea-117">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="0d4ea-118">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="0d4ea-118">-ServiceType</span></span>
<span data-ttu-id="0d4ea-119">Указывает тип службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="0d4ea-119">Specifies the storage service type.</span></span>
<span data-ttu-id="0d4ea-120">Этот командлет получает свойства метрик для типа, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="0d4ea-120">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="0d4ea-121">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0d4ea-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0d4ea-122">Большом</span><span class="sxs-lookup"><span data-stu-id="0d4ea-122">Blob</span></span> 
- <span data-ttu-id="0d4ea-123">Таблич</span><span class="sxs-lookup"><span data-stu-id="0d4ea-123">Table</span></span>
- <span data-ttu-id="0d4ea-124">Поместить</span><span class="sxs-lookup"><span data-stu-id="0d4ea-124">Queue</span></span>
- <span data-ttu-id="0d4ea-125">Файл</span><span class="sxs-lookup"><span data-stu-id="0d4ea-125">File</span></span> 

<span data-ttu-id="0d4ea-126">Значение "файл" в настоящее время не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0d4ea-126">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="0d4ea-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d4ea-127">CommonParameters</span></span>
<span data-ttu-id="0d4ea-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0d4ea-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d4ea-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d4ea-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d4ea-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0d4ea-130">INPUTS</span></span>

## <span data-ttu-id="0d4ea-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d4ea-131">OUTPUTS</span></span>

## <span data-ttu-id="0d4ea-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="0d4ea-132">NOTES</span></span>

## <span data-ttu-id="0d4ea-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d4ea-133">RELATED LINKS</span></span>

[<span data-ttu-id="0d4ea-134">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="0d4ea-134">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="0d4ea-135">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="0d4ea-135">Set-AzureStorageServiceMetricsProperty</span></span>](./Set-AzureStorageServiceMetricsProperty.md)


