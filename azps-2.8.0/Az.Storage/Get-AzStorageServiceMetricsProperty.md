---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: e1c5b33f449b624f82d49da80dc75d937bb7f87a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907181"
---
# <span data-ttu-id="37064-101">Get-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="37064-101">Get-AzStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="37064-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="37064-102">SYNOPSIS</span></span>
<span data-ttu-id="37064-103">Возвращает свойства метрик для службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="37064-103">Gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="37064-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="37064-104">SYNTAX</span></span>

```
Get-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37064-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="37064-105">DESCRIPTION</span></span>
<span data-ttu-id="37064-106">Командлет **Get-AzStorageServiceMetricsProperty** получает свойства метрик для службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="37064-106">The **Get-AzStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="37064-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="37064-107">EXAMPLES</span></span>

### <span data-ttu-id="37064-108">Пример 1: получение свойств метрик для службы больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="37064-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="37064-109">Эта команда получает свойства метрик для хранилища больших двоичных объектов для типа метрики "Часы".</span><span class="sxs-lookup"><span data-stu-id="37064-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="37064-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="37064-110">PARAMETERS</span></span>

### <span data-ttu-id="37064-111">-Context</span><span class="sxs-lookup"><span data-stu-id="37064-111">-Context</span></span>
<span data-ttu-id="37064-112">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="37064-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="37064-113">Чтобы получить контекст хранилища, используйте командлет New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="37064-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="37064-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37064-114">-DefaultProfile</span></span>
<span data-ttu-id="37064-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="37064-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37064-116">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="37064-116">-MetricsType</span></span>
<span data-ttu-id="37064-117">Указывает тип метрики.</span><span class="sxs-lookup"><span data-stu-id="37064-117">Specifies a metrics type.</span></span>
<span data-ttu-id="37064-118">Этот командлет получает свойства метрик службы хранилища Azure для типа метрики, указанном в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="37064-118">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="37064-119">Допустимые значения этого параметра: hours и Minute.</span><span class="sxs-lookup"><span data-stu-id="37064-119">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="37064-120">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="37064-120">-ServiceType</span></span>
<span data-ttu-id="37064-121">Указывает тип службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="37064-121">Specifies the storage service type.</span></span>
<span data-ttu-id="37064-122">Этот командлет получает свойства метрик для типа, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="37064-122">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="37064-123">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="37064-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="37064-124">Большом</span><span class="sxs-lookup"><span data-stu-id="37064-124">Blob</span></span> 
- <span data-ttu-id="37064-125">Таблич</span><span class="sxs-lookup"><span data-stu-id="37064-125">Table</span></span>
- <span data-ttu-id="37064-126">Поместить</span><span class="sxs-lookup"><span data-stu-id="37064-126">Queue</span></span>
- <span data-ttu-id="37064-127">Файл. значение файла в настоящее время не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="37064-127">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="37064-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37064-128">CommonParameters</span></span>
<span data-ttu-id="37064-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="37064-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37064-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37064-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37064-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="37064-131">INPUTS</span></span>

### <span data-ttu-id="37064-132">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="37064-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="37064-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="37064-133">OUTPUTS</span></span>

### <span data-ttu-id="37064-134">Microsoft. Azure. Storage. Sharing. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="37064-134">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="37064-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="37064-135">NOTES</span></span>

## <span data-ttu-id="37064-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="37064-136">RELATED LINKS</span></span>

[<span data-ttu-id="37064-137">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="37064-137">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="37064-138">Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="37064-138">Set-AzStorageServiceMetricsProperty</span></span>](./Set-AzStorageServiceMetricsProperty.md)


