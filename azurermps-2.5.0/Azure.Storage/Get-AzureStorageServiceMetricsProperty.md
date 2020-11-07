---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageservicemetricsproperty
schema: 2.0.0
ms.openlocfilehash: 1d7d536d7815206f942a89da4458f4669c0c9fd2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913512"
---
# <span data-ttu-id="4da2a-101">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="4da2a-101">Get-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="4da2a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4da2a-102">SYNOPSIS</span></span>
<span data-ttu-id="4da2a-103">Возвращает свойства метрик для службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4da2a-103">Gets metrics properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4da2a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4da2a-104">SYNTAX</span></span>

```
Get-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4da2a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4da2a-105">DESCRIPTION</span></span>
<span data-ttu-id="4da2a-106">Командлет **Get-AzureStorageServiceMetricsProperty** получает свойства метрик для службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4da2a-106">The **Get-AzureStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="4da2a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4da2a-107">EXAMPLES</span></span>

### <span data-ttu-id="4da2a-108">Пример 1: получение свойств метрик для службы больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="4da2a-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="4da2a-109">Эта команда получает свойства метрик для хранилища больших двоичных объектов для типа метрики "Часы".</span><span class="sxs-lookup"><span data-stu-id="4da2a-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="4da2a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4da2a-110">PARAMETERS</span></span>

### <span data-ttu-id="4da2a-111">-Context</span><span class="sxs-lookup"><span data-stu-id="4da2a-111">-Context</span></span>
<span data-ttu-id="4da2a-112">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4da2a-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4da2a-113">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="4da2a-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4da2a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4da2a-114">-DefaultProfile</span></span>
<span data-ttu-id="4da2a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4da2a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4da2a-116">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="4da2a-116">-MetricsType</span></span>
<span data-ttu-id="4da2a-117">Указывает тип метрики.</span><span class="sxs-lookup"><span data-stu-id="4da2a-117">Specifies a metrics type.</span></span>
<span data-ttu-id="4da2a-118">Этот командлет получает свойства метрик службы хранилища Azure для типа метрики, указанном в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="4da2a-118">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="4da2a-119">Допустимые значения этого параметра: hours и Minute.</span><span class="sxs-lookup"><span data-stu-id="4da2a-119">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="4da2a-120">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="4da2a-120">-ServiceType</span></span>
<span data-ttu-id="4da2a-121">Указывает тип службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="4da2a-121">Specifies the storage service type.</span></span>
<span data-ttu-id="4da2a-122">Этот командлет получает свойства метрик для типа, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="4da2a-122">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="4da2a-123">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="4da2a-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4da2a-124">Большом</span><span class="sxs-lookup"><span data-stu-id="4da2a-124">Blob</span></span> 
- <span data-ttu-id="4da2a-125">Таблич</span><span class="sxs-lookup"><span data-stu-id="4da2a-125">Table</span></span>
- <span data-ttu-id="4da2a-126">Поместить</span><span class="sxs-lookup"><span data-stu-id="4da2a-126">Queue</span></span>
- <span data-ttu-id="4da2a-127">Файл. значение файла в настоящее время не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4da2a-127">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="4da2a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4da2a-128">CommonParameters</span></span>
<span data-ttu-id="4da2a-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4da2a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4da2a-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4da2a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4da2a-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4da2a-131">INPUTS</span></span>

### <span data-ttu-id="4da2a-132">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4da2a-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4da2a-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4da2a-133">OUTPUTS</span></span>

### <span data-ttu-id="4da2a-134">Microsoft. WindowsAzure. Storage. Shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="4da2a-134">Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="4da2a-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="4da2a-135">NOTES</span></span>

## <span data-ttu-id="4da2a-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4da2a-136">RELATED LINKS</span></span>

[<span data-ttu-id="4da2a-137">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="4da2a-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="4da2a-138">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="4da2a-138">Set-AzureStorageServiceMetricsProperty</span></span>](./Set-AzureStorageServiceMetricsProperty.md)


