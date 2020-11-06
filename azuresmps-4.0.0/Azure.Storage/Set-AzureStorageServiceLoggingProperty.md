---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: ''
schema: 2.0.0
ms.openlocfilehash: dd1acb41a6f67fb281500ad8a0d37cb3c2e0a6dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556360"
---
# <span data-ttu-id="f28a0-101">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="f28a0-101">Set-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="f28a0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f28a0-102">SYNOPSIS</span></span>
<span data-ttu-id="f28a0-103">Изменяет ведение журнала для служб хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="f28a0-103">Modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="f28a0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f28a0-104">SYNTAX</span></span>

```
Set-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="f28a0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f28a0-105">DESCRIPTION</span></span>
<span data-ttu-id="f28a0-106">Командлет **Set-AzureStorageServiceLoggingProperty** изменяет ведение журнала для служб хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="f28a0-106">The **Set-AzureStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="f28a0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f28a0-107">EXAMPLES</span></span>

### <span data-ttu-id="f28a0-108">Пример 1: изменение свойств ведения журнала для службы больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="f28a0-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="f28a0-109">Эта команда изменяет ведение журнала версии 1,0 для хранилища BLOB-объектов, включая операции чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="f28a0-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="f28a0-110">Ведение журнала службы хранилища Azure сохраняет записи в течение 10 дней.</span><span class="sxs-lookup"><span data-stu-id="f28a0-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="f28a0-111">Так как эта команда задает параметр *PassThru* , команда отображает измененные свойства ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="f28a0-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="f28a0-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f28a0-112">PARAMETERS</span></span>

### <span data-ttu-id="f28a0-113">-Context</span><span class="sxs-lookup"><span data-stu-id="f28a0-113">-Context</span></span>
<span data-ttu-id="f28a0-114">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="f28a0-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f28a0-115">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="f28a0-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f28a0-116">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="f28a0-116">-LoggingOperations</span></span>
<span data-ttu-id="f28a0-117">Указывает массив операций службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="f28a0-117">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="f28a0-118">Службы хранилища Azure регистрируют операции, которые указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="f28a0-118">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="f28a0-119">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f28a0-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f28a0-120">Ничего</span><span class="sxs-lookup"><span data-stu-id="f28a0-120">None</span></span>
- <span data-ttu-id="f28a0-121">Читаются</span><span class="sxs-lookup"><span data-stu-id="f28a0-121">Read</span></span>
- <span data-ttu-id="f28a0-122">Пишу</span><span class="sxs-lookup"><span data-stu-id="f28a0-122">Write</span></span>
- <span data-ttu-id="f28a0-123">Удаление</span><span class="sxs-lookup"><span data-stu-id="f28a0-123">Delete</span></span>
- <span data-ttu-id="f28a0-124">Весь</span><span class="sxs-lookup"><span data-stu-id="f28a0-124">All</span></span>

```yaml
Type: LoggingOperations[]
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read, Write, Delete, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f28a0-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f28a0-125">-PassThru</span></span>
<span data-ttu-id="f28a0-126">Указывает на то, что этот командлет возвращает обновленные свойства ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="f28a0-126">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="f28a0-127">Если этот параметр не указан, этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f28a0-127">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="f28a0-128">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="f28a0-128">-RetentionDays</span></span>
<span data-ttu-id="f28a0-129">Указывает количество дней, в течение которых служба хранилища Azure сохраняет данные, записанные в журнал.</span><span class="sxs-lookup"><span data-stu-id="f28a0-129">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

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

### <span data-ttu-id="f28a0-130">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="f28a0-130">-ServiceType</span></span>
<span data-ttu-id="f28a0-131">Указывает тип службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="f28a0-131">Specifies the storage service type.</span></span>
<span data-ttu-id="f28a0-132">Этот командлет изменяет свойства ведения журнала для типа службы, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="f28a0-132">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="f28a0-133">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f28a0-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f28a0-134">Большом</span><span class="sxs-lookup"><span data-stu-id="f28a0-134">Blob</span></span> 
- <span data-ttu-id="f28a0-135">Таблич</span><span class="sxs-lookup"><span data-stu-id="f28a0-135">Table</span></span>
- <span data-ttu-id="f28a0-136">Поместить</span><span class="sxs-lookup"><span data-stu-id="f28a0-136">Queue</span></span>
- <span data-ttu-id="f28a0-137">Файл</span><span class="sxs-lookup"><span data-stu-id="f28a0-137">File</span></span>

<span data-ttu-id="f28a0-138">Значение "файл" в настоящее время не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f28a0-138">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="f28a0-139">-Version</span><span class="sxs-lookup"><span data-stu-id="f28a0-139">-Version</span></span>
<span data-ttu-id="f28a0-140">Указывает версию ведения журнала службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="f28a0-140">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="f28a0-141">Значение по умолчанию — 1,0.</span><span class="sxs-lookup"><span data-stu-id="f28a0-141">The default value is 1.0.</span></span>

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

### <span data-ttu-id="f28a0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f28a0-142">CommonParameters</span></span>
<span data-ttu-id="f28a0-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f28a0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f28a0-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f28a0-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f28a0-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f28a0-145">INPUTS</span></span>

## <span data-ttu-id="f28a0-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f28a0-146">OUTPUTS</span></span>

## <span data-ttu-id="f28a0-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="f28a0-147">NOTES</span></span>

## <span data-ttu-id="f28a0-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f28a0-148">RELATED LINKS</span></span>

[<span data-ttu-id="f28a0-149">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="f28a0-149">Get-AzureStorageServiceLoggingProperty</span></span>](./Get-AzureStorageServiceLoggingProperty.md)

[<span data-ttu-id="f28a0-150">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="f28a0-150">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


