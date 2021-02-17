---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: d3f32e44e5653d0d6a9c9b5a9a1eee27b66d43cf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100222916"
---
# <span data-ttu-id="bbf4f-101">Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="bbf4f-101">Set-AzStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="bbf4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbf4f-102">SYNOPSIS</span></span>
<span data-ttu-id="bbf4f-103">Изменяет свойства метрик для службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="bbf4f-103">Modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="bbf4f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bbf4f-104">SYNTAX</span></span>

```
Set-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbf4f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bbf4f-105">DESCRIPTION</span></span>
<span data-ttu-id="bbf4f-106">**Cmdlet Set-AzStorageServiceMetricsProperty** изменяет свойства метрик для службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="bbf4f-106">The **Set-AzStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="bbf4f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bbf4f-107">EXAMPLES</span></span>

### <span data-ttu-id="bbf4f-108">Пример 1. Изменение свойств метрик для службы BLOB-объектов</span><span class="sxs-lookup"><span data-stu-id="bbf4f-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="bbf4f-109">Эта команда изменяет показатели версии 1.0 для хранилища BLOB-хранилищ на уровень обслуживания.</span><span class="sxs-lookup"><span data-stu-id="bbf4f-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="bbf4f-110">Метрик службы хранилища Azure сохраняют записи в течение 10 дней.</span><span class="sxs-lookup"><span data-stu-id="bbf4f-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="bbf4f-111">Так как эта команда указывает параметр *PassThru,* она отображает измененные свойства метрик.</span><span class="sxs-lookup"><span data-stu-id="bbf4f-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="bbf4f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bbf4f-112">PARAMETERS</span></span>

### <span data-ttu-id="bbf4f-113">-Контекст</span><span class="sxs-lookup"><span data-stu-id="bbf4f-113">-Context</span></span>
<span data-ttu-id="bbf4f-114">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="bbf4f-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="bbf4f-115">Для получения контекста хранилища используйте New-AzStorageContext управления.</span><span class="sxs-lookup"><span data-stu-id="bbf4f-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="bbf4f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbf4f-116">-DefaultProfile</span></span>
<span data-ttu-id="bbf4f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bbf4f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbf4f-118">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="bbf4f-118">-MetricsLevel</span></span>
<span data-ttu-id="bbf4f-119">Определяет уровень метрик, который используется для службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="bbf4f-119">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="bbf4f-120">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="bbf4f-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bbf4f-121">Нет</span><span class="sxs-lookup"><span data-stu-id="bbf4f-121">None</span></span>
- <span data-ttu-id="bbf4f-122">Служба</span><span class="sxs-lookup"><span data-stu-id="bbf4f-122">Service</span></span>
- <span data-ttu-id="bbf4f-123">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="bbf4f-123">ServiceAndApi</span></span>

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

### <span data-ttu-id="bbf4f-124">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="bbf4f-124">-MetricsType</span></span>
<span data-ttu-id="bbf4f-125">Определяет тип метрик.</span><span class="sxs-lookup"><span data-stu-id="bbf4f-125">Specifies a metrics type.</span></span>
<span data-ttu-id="bbf4f-126">Этот cmdlet задает для типа метрик службы хранилища Azure значение, указанное этим параметром.</span><span class="sxs-lookup"><span data-stu-id="bbf4f-126">This cmdlet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="bbf4f-127">Допустимыми значениями для этого параметра являются часы и минуты.</span><span class="sxs-lookup"><span data-stu-id="bbf4f-127">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="bbf4f-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bbf4f-128">-PassThru</span></span>
<span data-ttu-id="bbf4f-129">Указывает на то, что этот cmdlets возвращает свойства обновленных метрик.</span><span class="sxs-lookup"><span data-stu-id="bbf4f-129">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="bbf4f-130">Если этот параметр не задан, этот cmdlet не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="bbf4f-130">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="bbf4f-131">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="bbf4f-131">-RetentionDays</span></span>
<span data-ttu-id="bbf4f-132">Определяет количество дней, в течение дня в течение дня, в течение которое служба хранилища Azure сохраняет данные метрик.</span><span class="sxs-lookup"><span data-stu-id="bbf4f-132">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

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

### <span data-ttu-id="bbf4f-133">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="bbf4f-133">-ServiceType</span></span>
<span data-ttu-id="bbf4f-134">Тип службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="bbf4f-134">Specifies the storage service type.</span></span>
<span data-ttu-id="bbf4f-135">Этот cmdlet изменяет свойства метрик для типа службы, указанного этим параметром.</span><span class="sxs-lookup"><span data-stu-id="bbf4f-135">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="bbf4f-136">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="bbf4f-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bbf4f-137">BLOB</span><span class="sxs-lookup"><span data-stu-id="bbf4f-137">Blob</span></span> 
- <span data-ttu-id="bbf4f-138">Таблица</span><span class="sxs-lookup"><span data-stu-id="bbf4f-138">Table</span></span>
- <span data-ttu-id="bbf4f-139">Очередь</span><span class="sxs-lookup"><span data-stu-id="bbf4f-139">Queue</span></span>
- <span data-ttu-id="bbf4f-140">Файл Со значением "Файл" в настоящее время не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="bbf4f-140">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="bbf4f-141">-Версия</span><span class="sxs-lookup"><span data-stu-id="bbf4f-141">-Version</span></span>
<span data-ttu-id="bbf4f-142">Определяет версию метрик хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="bbf4f-142">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="bbf4f-143">Значение по умолчанию — 1,0.</span><span class="sxs-lookup"><span data-stu-id="bbf4f-143">The default value is 1.0.</span></span>

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

### <span data-ttu-id="bbf4f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbf4f-144">CommonParameters</span></span>
<span data-ttu-id="bbf4f-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbf4f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbf4f-146">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbf4f-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbf4f-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bbf4f-147">INPUTS</span></span>

### <span data-ttu-id="bbf4f-148">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="bbf4f-148">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="bbf4f-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bbf4f-149">OUTPUTS</span></span>

### <span data-ttu-id="bbf4f-150">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="bbf4f-150">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="bbf4f-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bbf4f-151">NOTES</span></span>

## <span data-ttu-id="bbf4f-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bbf4f-152">RELATED LINKS</span></span>

[<span data-ttu-id="bbf4f-153">Get-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="bbf4f-153">Get-AzStorageServiceMetricsProperty</span></span>](./Get-AzStorageServiceMetricsProperty.md)

[<span data-ttu-id="bbf4f-154">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="bbf4f-154">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


