---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: ''
schema: 2.0.0
ms.openlocfilehash: d615c0a807c12640f20a72b97a2c11c2efcd5b28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556247"
---
# <span data-ttu-id="3322c-101">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="3322c-101">Get-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="3322c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3322c-102">SYNOPSIS</span></span>
<span data-ttu-id="3322c-103">Получение свойств ведения журнала для служб хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="3322c-103">Gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="3322c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3322c-104">SYNTAX</span></span>

```
Get-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="3322c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3322c-105">DESCRIPTION</span></span>
<span data-ttu-id="3322c-106">Командлет **Get-AzureStorageServiceLoggingProperty** получает свойства ведения журнала для служб хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="3322c-106">The **Get-AzureStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="3322c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3322c-107">EXAMPLES</span></span>

### <span data-ttu-id="3322c-108">Пример 1: получение свойств ведения журнала для службы больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="3322c-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="3322c-109">Эта команда получает свойства ведения журнала для хранилища BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="3322c-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="3322c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3322c-110">PARAMETERS</span></span>

### <span data-ttu-id="3322c-111">-Context</span><span class="sxs-lookup"><span data-stu-id="3322c-111">-Context</span></span>
<span data-ttu-id="3322c-112">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="3322c-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3322c-113">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="3322c-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3322c-114">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="3322c-114">-ServiceType</span></span>
<span data-ttu-id="3322c-115">Указывает тип службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="3322c-115">Specifies the storage service type.</span></span>
<span data-ttu-id="3322c-116">Этот командлет получает свойства ведения журнала для типа службы, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="3322c-116">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="3322c-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3322c-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3322c-118">Большом</span><span class="sxs-lookup"><span data-stu-id="3322c-118">Blob</span></span> 
- <span data-ttu-id="3322c-119">Таблич</span><span class="sxs-lookup"><span data-stu-id="3322c-119">Table</span></span>
- <span data-ttu-id="3322c-120">Поместить</span><span class="sxs-lookup"><span data-stu-id="3322c-120">Queue</span></span>
- <span data-ttu-id="3322c-121">Файл</span><span class="sxs-lookup"><span data-stu-id="3322c-121">File</span></span>

<span data-ttu-id="3322c-122">Значение "файл" в настоящее время не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3322c-122">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="3322c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3322c-123">CommonParameters</span></span>
<span data-ttu-id="3322c-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3322c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3322c-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3322c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3322c-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3322c-126">INPUTS</span></span>

## <span data-ttu-id="3322c-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3322c-127">OUTPUTS</span></span>

## <span data-ttu-id="3322c-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="3322c-128">NOTES</span></span>

## <span data-ttu-id="3322c-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3322c-129">RELATED LINKS</span></span>

[<span data-ttu-id="3322c-130">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="3322c-130">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="3322c-131">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="3322c-131">Set-AzureStorageServiceLoggingProperty</span></span>](./Set-AzureStorageServiceLoggingProperty.md)


