---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceLoggingProperty.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: a3981ba2b0759afec06bb4cf34bc1e086658765a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732084"
---
# <span data-ttu-id="eb7a5-101">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="eb7a5-101">Get-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="eb7a5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eb7a5-102">SYNOPSIS</span></span>
<span data-ttu-id="eb7a5-103">Получение свойств ведения журнала для служб хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="eb7a5-103">Gets logging properties for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb7a5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eb7a5-104">SYNTAX</span></span>

```
Get-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb7a5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb7a5-105">DESCRIPTION</span></span>
<span data-ttu-id="eb7a5-106">Командлет **Get-AzureStorageServiceLoggingProperty** получает свойства ведения журнала для служб хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="eb7a5-106">The **Get-AzureStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="eb7a5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eb7a5-107">EXAMPLES</span></span>

### <span data-ttu-id="eb7a5-108">Пример 1: получение свойств ведения журнала для службы больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="eb7a5-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="eb7a5-109">Эта команда получает свойства ведения журнала для хранилища BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="eb7a5-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="eb7a5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eb7a5-110">PARAMETERS</span></span>

### <span data-ttu-id="eb7a5-111">-Context</span><span class="sxs-lookup"><span data-stu-id="eb7a5-111">-Context</span></span>
<span data-ttu-id="eb7a5-112">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="eb7a5-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="eb7a5-113">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="eb7a5-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="eb7a5-114">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="eb7a5-114">-ServiceType</span></span>
<span data-ttu-id="eb7a5-115">Указывает тип службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="eb7a5-115">Specifies the storage service type.</span></span>
<span data-ttu-id="eb7a5-116">Этот командлет получает свойства ведения журнала для типа службы, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="eb7a5-116">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="eb7a5-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="eb7a5-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="eb7a5-118">Большом</span><span class="sxs-lookup"><span data-stu-id="eb7a5-118">Blob</span></span> 
- <span data-ttu-id="eb7a5-119">Таблич</span><span class="sxs-lookup"><span data-stu-id="eb7a5-119">Table</span></span>
- <span data-ttu-id="eb7a5-120">Поместить</span><span class="sxs-lookup"><span data-stu-id="eb7a5-120">Queue</span></span>
- <span data-ttu-id="eb7a5-121">Файл</span><span class="sxs-lookup"><span data-stu-id="eb7a5-121">File</span></span>

<span data-ttu-id="eb7a5-122">Значение "файл" в настоящее время не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="eb7a5-122">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="eb7a5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb7a5-123">CommonParameters</span></span>
<span data-ttu-id="eb7a5-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eb7a5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb7a5-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb7a5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb7a5-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eb7a5-126">INPUTS</span></span>

### <span data-ttu-id="eb7a5-127">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="eb7a5-127">IStorageContext</span></span>

<span data-ttu-id="eb7a5-128">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="eb7a5-128">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="eb7a5-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb7a5-129">OUTPUTS</span></span>

### <span data-ttu-id="eb7a5-130">Microsoft. WindowsAzure. Storage. Shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="eb7a5-130">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="eb7a5-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="eb7a5-131">NOTES</span></span>

## <span data-ttu-id="eb7a5-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eb7a5-132">RELATED LINKS</span></span>

[<span data-ttu-id="eb7a5-133">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="eb7a5-133">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="eb7a5-134">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="eb7a5-134">Set-AzureStorageServiceLoggingProperty</span></span>](./Set-AzureStorageServiceLoggingProperty.md)


