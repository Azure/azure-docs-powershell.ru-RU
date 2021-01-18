---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: 4d58b8e323476adda73f4a4827dc263c20bd4cc4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517093"
---
# <span data-ttu-id="ff0e0-101">Get-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="ff0e0-101">Get-AzStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="ff0e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff0e0-102">SYNOPSIS</span></span>
<span data-ttu-id="ff0e0-103">Свойства метрик для службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="ff0e0-103">Gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="ff0e0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ff0e0-104">SYNTAX</span></span>

```
Get-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff0e0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff0e0-105">DESCRIPTION</span></span>
<span data-ttu-id="ff0e0-106">С **помощью cmdlet Get-AzStorageServiceMetricsProperty** можно получить свойства метрик для службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="ff0e0-106">The **Get-AzStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="ff0e0-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ff0e0-107">EXAMPLES</span></span>

### <span data-ttu-id="ff0e0-108">Пример 1. Получить свойства метрик для службы BLOB-объектов</span><span class="sxs-lookup"><span data-stu-id="ff0e0-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="ff0e0-109">Эта команда получает свойства метрик для хранилища BLOB-объектов для типа "Часы".</span><span class="sxs-lookup"><span data-stu-id="ff0e0-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="ff0e0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff0e0-110">PARAMETERS</span></span>

### <span data-ttu-id="ff0e0-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="ff0e0-111">-Context</span></span>
<span data-ttu-id="ff0e0-112">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="ff0e0-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ff0e0-113">Для получения контекста хранилища используйте New-AzStorageContext управления.</span><span class="sxs-lookup"><span data-stu-id="ff0e0-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ff0e0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff0e0-114">-DefaultProfile</span></span>
<span data-ttu-id="ff0e0-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ff0e0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff0e0-116">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="ff0e0-116">-MetricsType</span></span>
<span data-ttu-id="ff0e0-117">Определяет тип метрик.</span><span class="sxs-lookup"><span data-stu-id="ff0e0-117">Specifies a metrics type.</span></span>
<span data-ttu-id="ff0e0-118">Этот cmdlet получает свойства метрик службы хранилища Azure для типа метрик, указанного этим параметром.</span><span class="sxs-lookup"><span data-stu-id="ff0e0-118">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="ff0e0-119">Допустимыми значениями для этого параметра являются часы и минуты.</span><span class="sxs-lookup"><span data-stu-id="ff0e0-119">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="ff0e0-120">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="ff0e0-120">-ServiceType</span></span>
<span data-ttu-id="ff0e0-121">Тип службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="ff0e0-121">Specifies the storage service type.</span></span>
<span data-ttu-id="ff0e0-122">Этот cmdlet получает свойства метрик для типа, указанного этим параметром.</span><span class="sxs-lookup"><span data-stu-id="ff0e0-122">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="ff0e0-123">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="ff0e0-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ff0e0-124">BLOB</span><span class="sxs-lookup"><span data-stu-id="ff0e0-124">Blob</span></span> 
- <span data-ttu-id="ff0e0-125">Таблица</span><span class="sxs-lookup"><span data-stu-id="ff0e0-125">Table</span></span>
- <span data-ttu-id="ff0e0-126">Очередь</span><span class="sxs-lookup"><span data-stu-id="ff0e0-126">Queue</span></span>
- <span data-ttu-id="ff0e0-127">Файл, в который в настоящее время не поддерживается значение "Файл".</span><span class="sxs-lookup"><span data-stu-id="ff0e0-127">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="ff0e0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff0e0-128">CommonParameters</span></span>
<span data-ttu-id="ff0e0-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff0e0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff0e0-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff0e0-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff0e0-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ff0e0-131">INPUTS</span></span>

### <span data-ttu-id="ff0e0-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ff0e0-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ff0e0-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ff0e0-133">OUTPUTS</span></span>

### <span data-ttu-id="ff0e0-134">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="ff0e0-134">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="ff0e0-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ff0e0-135">NOTES</span></span>

## <span data-ttu-id="ff0e0-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ff0e0-136">RELATED LINKS</span></span>

[<span data-ttu-id="ff0e0-137">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ff0e0-137">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="ff0e0-138">Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="ff0e0-138">Set-AzStorageServiceMetricsProperty</span></span>](./Set-AzStorageServiceMetricsProperty.md)


