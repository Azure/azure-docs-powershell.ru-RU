---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestorageservicemetricsproperty
schema: 2.0.0
ms.openlocfilehash: 45192b6b24719bb793e3f443cf2a8cb42abd78ad
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915437"
---
# <span data-ttu-id="2f72f-101">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="2f72f-101">Set-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="2f72f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2f72f-102">SYNOPSIS</span></span>
<span data-ttu-id="2f72f-103">Изменяет свойства метрик для службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="2f72f-103">Modifies metrics properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f72f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2f72f-104">SYNTAX</span></span>

```
Set-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f72f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f72f-105">DESCRIPTION</span></span>
<span data-ttu-id="2f72f-106">Командлет **Set-AzureStorageServiceMetricsProperty** изменяет свойства метрик для службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="2f72f-106">The **Set-AzureStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="2f72f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2f72f-107">EXAMPLES</span></span>

### <span data-ttu-id="2f72f-108">Пример 1: изменение свойств метрик для службы больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="2f72f-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="2f72f-109">Эта команда изменяет метрики версии 1,0 для хранилища больших двоичных объектов на уровень обслуживания.</span><span class="sxs-lookup"><span data-stu-id="2f72f-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="2f72f-110">Метрики службы хранилища Azure сохраняют записи в течение 10 дней.</span><span class="sxs-lookup"><span data-stu-id="2f72f-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="2f72f-111">Так как эта команда задает параметр *PassThru* , команда отображает измененные свойства метрики.</span><span class="sxs-lookup"><span data-stu-id="2f72f-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="2f72f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2f72f-112">PARAMETERS</span></span>

### <span data-ttu-id="2f72f-113">-Context</span><span class="sxs-lookup"><span data-stu-id="2f72f-113">-Context</span></span>
<span data-ttu-id="2f72f-114">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="2f72f-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="2f72f-115">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="2f72f-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2f72f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f72f-116">-DefaultProfile</span></span>
<span data-ttu-id="2f72f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2f72f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f72f-118">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="2f72f-118">-MetricsLevel</span></span>
<span data-ttu-id="2f72f-119">Указывает уровень метрик, который служба хранилища Azure использует для службы.</span><span class="sxs-lookup"><span data-stu-id="2f72f-119">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="2f72f-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="2f72f-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2f72f-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="2f72f-121">None</span></span>
- <span data-ttu-id="2f72f-122">Сервиса</span><span class="sxs-lookup"><span data-stu-id="2f72f-122">Service</span></span>
- <span data-ttu-id="2f72f-123">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="2f72f-123">ServiceAndApi</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsLevel]
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, ServiceAndApi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f72f-124">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="2f72f-124">-MetricsType</span></span>
<span data-ttu-id="2f72f-125">Указывает тип метрики.</span><span class="sxs-lookup"><span data-stu-id="2f72f-125">Specifies a metrics type.</span></span>
<span data-ttu-id="2f72f-126">Этот cmldet задает для типа метрик службы хранилища Azure значение, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="2f72f-126">This cmldet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="2f72f-127">Допустимые значения этого параметра: hours и Minute.</span><span class="sxs-lookup"><span data-stu-id="2f72f-127">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="2f72f-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f72f-128">-PassThru</span></span>
<span data-ttu-id="2f72f-129">Указывает на то, что эти командлеты возвращают обновленные свойства метрики.</span><span class="sxs-lookup"><span data-stu-id="2f72f-129">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="2f72f-130">Если этот параметр не указан, этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="2f72f-130">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="2f72f-131">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="2f72f-131">-RetentionDays</span></span>
<span data-ttu-id="2f72f-132">Указывает количество дней, в течение которых служба хранилища Azure хранит сведения о метриках.</span><span class="sxs-lookup"><span data-stu-id="2f72f-132">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

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

### <span data-ttu-id="2f72f-133">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="2f72f-133">-ServiceType</span></span>
<span data-ttu-id="2f72f-134">Указывает тип службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="2f72f-134">Specifies the storage service type.</span></span>
<span data-ttu-id="2f72f-135">Этот командлет изменяет свойства метрик для типа службы, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="2f72f-135">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="2f72f-136">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="2f72f-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2f72f-137">Большом</span><span class="sxs-lookup"><span data-stu-id="2f72f-137">Blob</span></span> 
- <span data-ttu-id="2f72f-138">Таблич</span><span class="sxs-lookup"><span data-stu-id="2f72f-138">Table</span></span>
- <span data-ttu-id="2f72f-139">Поместить</span><span class="sxs-lookup"><span data-stu-id="2f72f-139">Queue</span></span>
- <span data-ttu-id="2f72f-140">Файл. значение файла в настоящее время не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2f72f-140">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="2f72f-141">-Version</span><span class="sxs-lookup"><span data-stu-id="2f72f-141">-Version</span></span>
<span data-ttu-id="2f72f-142">Указывает версию метрик хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="2f72f-142">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="2f72f-143">Значение по умолчанию — 1,0.</span><span class="sxs-lookup"><span data-stu-id="2f72f-143">The default value is 1.0.</span></span>

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

### <span data-ttu-id="2f72f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f72f-144">CommonParameters</span></span>
<span data-ttu-id="2f72f-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2f72f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f72f-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f72f-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f72f-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2f72f-147">INPUTS</span></span>

### <span data-ttu-id="2f72f-148">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2f72f-148">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2f72f-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f72f-149">OUTPUTS</span></span>

### <span data-ttu-id="2f72f-150">Microsoft. WindowsAzure. Storage. Shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="2f72f-150">Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="2f72f-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="2f72f-151">NOTES</span></span>

## <span data-ttu-id="2f72f-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2f72f-152">RELATED LINKS</span></span>

[<span data-ttu-id="2f72f-153">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="2f72f-153">Get-AzureStorageServiceMetricsProperty</span></span>](./Get-AzureStorageServiceMetricsProperty.md)

[<span data-ttu-id="2f72f-154">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="2f72f-154">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


