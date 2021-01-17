---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: d3f32e44e5653d0d6a9c9b5a9a1eee27b66d43cf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403247"
---
# <span data-ttu-id="a6636-101">Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="a6636-101">Set-AzStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="a6636-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6636-102">SYNOPSIS</span></span>
<span data-ttu-id="a6636-103">Изменяет свойства метрик для службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="a6636-103">Modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="a6636-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a6636-104">SYNTAX</span></span>

```
Set-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6636-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6636-105">DESCRIPTION</span></span>
<span data-ttu-id="a6636-106">**Cmdlet Set-AzStorageServiceMetricsProperty** изменяет свойства метрик для службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="a6636-106">The **Set-AzStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="a6636-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a6636-107">EXAMPLES</span></span>

### <span data-ttu-id="a6636-108">Пример 1. Изменение свойств метрик для службы BLOB-объектов</span><span class="sxs-lookup"><span data-stu-id="a6636-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="a6636-109">Эта команда изменяет показатели версии 1.0 для хранилища BLOB-хранилищ на уровень обслуживания.</span><span class="sxs-lookup"><span data-stu-id="a6636-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="a6636-110">Метрик службы хранилища Azure сохраняют записи в течение 10 дней.</span><span class="sxs-lookup"><span data-stu-id="a6636-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="a6636-111">Так как эта команда указывает параметр *PassThru,* она отображает измененные свойства метрик.</span><span class="sxs-lookup"><span data-stu-id="a6636-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="a6636-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6636-112">PARAMETERS</span></span>

### <span data-ttu-id="a6636-113">-Контекст</span><span class="sxs-lookup"><span data-stu-id="a6636-113">-Context</span></span>
<span data-ttu-id="a6636-114">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="a6636-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a6636-115">Для получения контекста хранилища используйте New-AzStorageContext управления.</span><span class="sxs-lookup"><span data-stu-id="a6636-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a6636-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6636-116">-DefaultProfile</span></span>
<span data-ttu-id="a6636-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a6636-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6636-118">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="a6636-118">-MetricsLevel</span></span>
<span data-ttu-id="a6636-119">Определяет уровень метрик, который используется для службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="a6636-119">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="a6636-120">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="a6636-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a6636-121">Нет</span><span class="sxs-lookup"><span data-stu-id="a6636-121">None</span></span>
- <span data-ttu-id="a6636-122">Служба</span><span class="sxs-lookup"><span data-stu-id="a6636-122">Service</span></span>
- <span data-ttu-id="a6636-123">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="a6636-123">ServiceAndApi</span></span>

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

### <span data-ttu-id="a6636-124">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="a6636-124">-MetricsType</span></span>
<span data-ttu-id="a6636-125">Определяет тип метрик.</span><span class="sxs-lookup"><span data-stu-id="a6636-125">Specifies a metrics type.</span></span>
<span data-ttu-id="a6636-126">Этот cmdlet задает для типа метрик службы хранилища Azure значение, указанное этим параметром.</span><span class="sxs-lookup"><span data-stu-id="a6636-126">This cmdlet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="a6636-127">Допустимыми значениями для этого параметра являются часы и минуты.</span><span class="sxs-lookup"><span data-stu-id="a6636-127">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="a6636-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6636-128">-PassThru</span></span>
<span data-ttu-id="a6636-129">Указывает на то, что этот cmdlets возвращает свойства обновленных метрик.</span><span class="sxs-lookup"><span data-stu-id="a6636-129">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="a6636-130">Если этот параметр не задан, этот cmdlet не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a6636-130">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="a6636-131">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="a6636-131">-RetentionDays</span></span>
<span data-ttu-id="a6636-132">Определяет количество дней, в течение дня в течение дня, в течение которое служба хранилища Azure сохраняет данные метрик.</span><span class="sxs-lookup"><span data-stu-id="a6636-132">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

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

### <span data-ttu-id="a6636-133">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="a6636-133">-ServiceType</span></span>
<span data-ttu-id="a6636-134">Тип службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="a6636-134">Specifies the storage service type.</span></span>
<span data-ttu-id="a6636-135">Этот cmdlet изменяет свойства метрик для типа службы, указанного этим параметром.</span><span class="sxs-lookup"><span data-stu-id="a6636-135">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="a6636-136">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="a6636-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a6636-137">BLOB</span><span class="sxs-lookup"><span data-stu-id="a6636-137">Blob</span></span> 
- <span data-ttu-id="a6636-138">Таблица</span><span class="sxs-lookup"><span data-stu-id="a6636-138">Table</span></span>
- <span data-ttu-id="a6636-139">Очередь</span><span class="sxs-lookup"><span data-stu-id="a6636-139">Queue</span></span>
- <span data-ttu-id="a6636-140">Файл, в который в настоящее время не поддерживается значение "Файл".</span><span class="sxs-lookup"><span data-stu-id="a6636-140">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="a6636-141">-Версия</span><span class="sxs-lookup"><span data-stu-id="a6636-141">-Version</span></span>
<span data-ttu-id="a6636-142">Определяет версию метрик хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="a6636-142">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="a6636-143">Значение по умолчанию — 1,0.</span><span class="sxs-lookup"><span data-stu-id="a6636-143">The default value is 1.0.</span></span>

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

### <span data-ttu-id="a6636-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6636-144">CommonParameters</span></span>
<span data-ttu-id="a6636-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6636-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6636-146">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6636-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6636-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a6636-147">INPUTS</span></span>

### <span data-ttu-id="a6636-148">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a6636-148">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a6636-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a6636-149">OUTPUTS</span></span>

### <span data-ttu-id="a6636-150">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="a6636-150">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="a6636-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a6636-151">NOTES</span></span>

## <span data-ttu-id="a6636-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a6636-152">RELATED LINKS</span></span>

[<span data-ttu-id="a6636-153">Get-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="a6636-153">Get-AzStorageServiceMetricsProperty</span></span>](./Get-AzStorageServiceMetricsProperty.md)

[<span data-ttu-id="a6636-154">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a6636-154">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


