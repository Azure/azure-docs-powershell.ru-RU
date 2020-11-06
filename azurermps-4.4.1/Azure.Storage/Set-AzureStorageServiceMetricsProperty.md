---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceMetricsProperty.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 3f295d42075054d676852c42028dc2e9fd8b82b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568369"
---
# <span data-ttu-id="07139-101">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="07139-101">Set-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="07139-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="07139-102">SYNOPSIS</span></span>
<span data-ttu-id="07139-103">Изменяет свойства метрик для службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="07139-103">Modifies metrics properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07139-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="07139-104">SYNTAX</span></span>

```
Set-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="07139-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="07139-105">DESCRIPTION</span></span>
<span data-ttu-id="07139-106">Командлет **Set-AzureStorageServiceMetricsProperty** изменяет свойства метрик для службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="07139-106">The **Set-AzureStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="07139-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="07139-107">EXAMPLES</span></span>

### <span data-ttu-id="07139-108">Пример 1: изменение свойств метрик для службы больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="07139-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="07139-109">Эта команда изменяет метрики версии 1,0 для хранилища больших двоичных объектов на уровень обслуживания.</span><span class="sxs-lookup"><span data-stu-id="07139-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="07139-110">Метрики службы хранилища Azure сохраняют записи в течение 10 дней.</span><span class="sxs-lookup"><span data-stu-id="07139-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="07139-111">Так как эта команда задает параметр *PassThru* , команда отображает измененные свойства метрики.</span><span class="sxs-lookup"><span data-stu-id="07139-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="07139-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="07139-112">PARAMETERS</span></span>

### <span data-ttu-id="07139-113">-Context</span><span class="sxs-lookup"><span data-stu-id="07139-113">-Context</span></span>
<span data-ttu-id="07139-114">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="07139-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="07139-115">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="07139-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="07139-116">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="07139-116">-MetricsLevel</span></span>
<span data-ttu-id="07139-117">Указывает уровень метрик, который служба хранилища Azure использует для службы.</span><span class="sxs-lookup"><span data-stu-id="07139-117">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="07139-118">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="07139-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="07139-119">Ничего</span><span class="sxs-lookup"><span data-stu-id="07139-119">None</span></span>
- <span data-ttu-id="07139-120">Сервиса</span><span class="sxs-lookup"><span data-stu-id="07139-120">Service</span></span>
- <span data-ttu-id="07139-121">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="07139-121">ServiceAndApi</span></span>

```yaml
Type: MetricsLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Service, ServiceAndApi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07139-122">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="07139-122">-MetricsType</span></span>
<span data-ttu-id="07139-123">Указывает тип метрики.</span><span class="sxs-lookup"><span data-stu-id="07139-123">Specifies a metrics type.</span></span>
<span data-ttu-id="07139-124">Этот cmldet задает для типа метрик службы хранилища Azure значение, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="07139-124">This cmldet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="07139-125">Допустимые значения этого параметра: hours и Minute.</span><span class="sxs-lookup"><span data-stu-id="07139-125">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="07139-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="07139-126">-PassThru</span></span>
<span data-ttu-id="07139-127">Указывает на то, что эти командлеты возвращают обновленные свойства метрики.</span><span class="sxs-lookup"><span data-stu-id="07139-127">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="07139-128">Если этот параметр не указан, этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="07139-128">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07139-129">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="07139-129">-RetentionDays</span></span>
<span data-ttu-id="07139-130">Указывает количество дней, в течение которых служба хранилища Azure хранит сведения о метриках.</span><span class="sxs-lookup"><span data-stu-id="07139-130">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07139-131">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="07139-131">-ServiceType</span></span>
<span data-ttu-id="07139-132">Указывает тип службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="07139-132">Specifies the storage service type.</span></span>
<span data-ttu-id="07139-133">Этот командлет изменяет свойства метрик для типа службы, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="07139-133">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="07139-134">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="07139-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="07139-135">Большом</span><span class="sxs-lookup"><span data-stu-id="07139-135">Blob</span></span> 
- <span data-ttu-id="07139-136">Таблич</span><span class="sxs-lookup"><span data-stu-id="07139-136">Table</span></span>
- <span data-ttu-id="07139-137">Поместить</span><span class="sxs-lookup"><span data-stu-id="07139-137">Queue</span></span>
- <span data-ttu-id="07139-138">Файл</span><span class="sxs-lookup"><span data-stu-id="07139-138">File</span></span>

<span data-ttu-id="07139-139">Значение "файл" в настоящее время не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="07139-139">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="07139-140">-Version</span><span class="sxs-lookup"><span data-stu-id="07139-140">-Version</span></span>
<span data-ttu-id="07139-141">Указывает версию метрик хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="07139-141">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="07139-142">Значение по умолчанию — 1,0.</span><span class="sxs-lookup"><span data-stu-id="07139-142">The default value is 1.0.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07139-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07139-143">CommonParameters</span></span>
<span data-ttu-id="07139-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="07139-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07139-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07139-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07139-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="07139-146">INPUTS</span></span>

### <span data-ttu-id="07139-147">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="07139-147">IStorageContext</span></span>

<span data-ttu-id="07139-148">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="07139-148">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="07139-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="07139-149">OUTPUTS</span></span>

### <span data-ttu-id="07139-150">Microsoft. WindowsAzure. Storage. Shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="07139-150">Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="07139-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="07139-151">NOTES</span></span>

## <span data-ttu-id="07139-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="07139-152">RELATED LINKS</span></span>

[<span data-ttu-id="07139-153">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="07139-153">Get-AzureStorageServiceMetricsProperty</span></span>](./Get-AzureStorageServiceMetricsProperty.md)

[<span data-ttu-id="07139-154">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="07139-154">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


