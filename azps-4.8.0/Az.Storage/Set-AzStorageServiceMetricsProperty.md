---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: d3f32e44e5653d0d6a9c9b5a9a1eee27b66d43cf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235726"
---
# <span data-ttu-id="342d3-101">Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="342d3-101">Set-AzStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="342d3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="342d3-102">SYNOPSIS</span></span>
<span data-ttu-id="342d3-103">Изменяет свойства метрик для службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="342d3-103">Modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="342d3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="342d3-104">SYNTAX</span></span>

```
Set-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="342d3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="342d3-105">DESCRIPTION</span></span>
<span data-ttu-id="342d3-106">Командлет **Set-AzStorageServiceMetricsProperty** изменяет свойства метрик для службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="342d3-106">The **Set-AzStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="342d3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="342d3-107">EXAMPLES</span></span>

### <span data-ttu-id="342d3-108">Пример 1: изменение свойств метрик для службы больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="342d3-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="342d3-109">Эта команда изменяет метрики версии 1,0 для хранилища больших двоичных объектов на уровень обслуживания.</span><span class="sxs-lookup"><span data-stu-id="342d3-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="342d3-110">Метрики службы хранилища Azure сохраняют записи в течение 10 дней.</span><span class="sxs-lookup"><span data-stu-id="342d3-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="342d3-111">Так как эта команда задает параметр *PassThru* , команда отображает измененные свойства метрики.</span><span class="sxs-lookup"><span data-stu-id="342d3-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="342d3-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="342d3-112">PARAMETERS</span></span>

### <span data-ttu-id="342d3-113">-Context</span><span class="sxs-lookup"><span data-stu-id="342d3-113">-Context</span></span>
<span data-ttu-id="342d3-114">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="342d3-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="342d3-115">Чтобы получить контекст хранилища, используйте командлет New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="342d3-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="342d3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="342d3-116">-DefaultProfile</span></span>
<span data-ttu-id="342d3-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="342d3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="342d3-118">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="342d3-118">-MetricsLevel</span></span>
<span data-ttu-id="342d3-119">Указывает уровень метрик, который служба хранилища Azure использует для службы.</span><span class="sxs-lookup"><span data-stu-id="342d3-119">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="342d3-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="342d3-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="342d3-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="342d3-121">None</span></span>
- <span data-ttu-id="342d3-122">Сервиса</span><span class="sxs-lookup"><span data-stu-id="342d3-122">Service</span></span>
- <span data-ttu-id="342d3-123">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="342d3-123">ServiceAndApi</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.Shared.Protocol.MetricsLevel]
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, ServiceAndApi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="342d3-124">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="342d3-124">-MetricsType</span></span>
<span data-ttu-id="342d3-125">Указывает тип метрики.</span><span class="sxs-lookup"><span data-stu-id="342d3-125">Specifies a metrics type.</span></span>
<span data-ttu-id="342d3-126">Этот командлет задает для типа метрик службы хранилища Azure значение, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="342d3-126">This cmdlet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="342d3-127">Допустимые значения этого параметра: hours и Minute.</span><span class="sxs-lookup"><span data-stu-id="342d3-127">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="342d3-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="342d3-128">-PassThru</span></span>
<span data-ttu-id="342d3-129">Указывает на то, что эти командлеты возвращают обновленные свойства метрики.</span><span class="sxs-lookup"><span data-stu-id="342d3-129">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="342d3-130">Если этот параметр не указан, этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="342d3-130">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="342d3-131">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="342d3-131">-RetentionDays</span></span>
<span data-ttu-id="342d3-132">Указывает количество дней, в течение которых служба хранилища Azure хранит сведения о метриках.</span><span class="sxs-lookup"><span data-stu-id="342d3-132">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="342d3-133">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="342d3-133">-ServiceType</span></span>
<span data-ttu-id="342d3-134">Указывает тип службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="342d3-134">Specifies the storage service type.</span></span>
<span data-ttu-id="342d3-135">Этот командлет изменяет свойства метрик для типа службы, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="342d3-135">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="342d3-136">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="342d3-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="342d3-137">Большом</span><span class="sxs-lookup"><span data-stu-id="342d3-137">Blob</span></span> 
- <span data-ttu-id="342d3-138">Таблич</span><span class="sxs-lookup"><span data-stu-id="342d3-138">Table</span></span>
- <span data-ttu-id="342d3-139">Поместить</span><span class="sxs-lookup"><span data-stu-id="342d3-139">Queue</span></span>
- <span data-ttu-id="342d3-140">Файл. значение файла в настоящее время не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="342d3-140">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="342d3-141">-Version</span><span class="sxs-lookup"><span data-stu-id="342d3-141">-Version</span></span>
<span data-ttu-id="342d3-142">Указывает версию метрик хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="342d3-142">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="342d3-143">Значение по умолчанию — 1,0.</span><span class="sxs-lookup"><span data-stu-id="342d3-143">The default value is 1.0.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="342d3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="342d3-144">CommonParameters</span></span>
<span data-ttu-id="342d3-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="342d3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="342d3-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="342d3-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="342d3-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="342d3-147">INPUTS</span></span>

### <span data-ttu-id="342d3-148">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="342d3-148">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="342d3-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="342d3-149">OUTPUTS</span></span>

### <span data-ttu-id="342d3-150">Microsoft. Azure. Storage. Sharing. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="342d3-150">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="342d3-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="342d3-151">NOTES</span></span>

## <span data-ttu-id="342d3-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="342d3-152">RELATED LINKS</span></span>

[<span data-ttu-id="342d3-153">Get-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="342d3-153">Get-AzStorageServiceMetricsProperty</span></span>](./Get-AzStorageServiceMetricsProperty.md)

[<span data-ttu-id="342d3-154">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="342d3-154">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

