---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceLoggingProperty.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: baba161c849918c95d5e1df91330dfd96a4c5629
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568373"
---
# <span data-ttu-id="9c566-101">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="9c566-101">Set-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="9c566-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9c566-102">SYNOPSIS</span></span>
<span data-ttu-id="9c566-103">Изменяет ведение журнала для служб хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="9c566-103">Modifies logging for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c566-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9c566-104">SYNTAX</span></span>

```
Set-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="9c566-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c566-105">DESCRIPTION</span></span>
<span data-ttu-id="9c566-106">Командлет **Set-AzureStorageServiceLoggingProperty** изменяет ведение журнала для служб хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="9c566-106">The **Set-AzureStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="9c566-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9c566-107">EXAMPLES</span></span>

### <span data-ttu-id="9c566-108">Пример 1: изменение свойств ведения журнала для службы больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="9c566-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="9c566-109">Эта команда изменяет ведение журнала версии 1,0 для хранилища BLOB-объектов, включая операции чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="9c566-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="9c566-110">Ведение журнала службы хранилища Azure сохраняет записи в течение 10 дней.</span><span class="sxs-lookup"><span data-stu-id="9c566-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="9c566-111">Так как эта команда задает параметр *PassThru* , команда отображает измененные свойства ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="9c566-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="9c566-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9c566-112">PARAMETERS</span></span>

### <span data-ttu-id="9c566-113">-Context</span><span class="sxs-lookup"><span data-stu-id="9c566-113">-Context</span></span>
<span data-ttu-id="9c566-114">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="9c566-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="9c566-115">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="9c566-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="9c566-116">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="9c566-116">-LoggingOperations</span></span>
<span data-ttu-id="9c566-117">Указывает массив операций службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="9c566-117">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="9c566-118">Службы хранилища Azure регистрируют операции, которые указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="9c566-118">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="9c566-119">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9c566-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9c566-120">Ничего</span><span class="sxs-lookup"><span data-stu-id="9c566-120">None</span></span>
- <span data-ttu-id="9c566-121">Читаются</span><span class="sxs-lookup"><span data-stu-id="9c566-121">Read</span></span>
- <span data-ttu-id="9c566-122">Пишу</span><span class="sxs-lookup"><span data-stu-id="9c566-122">Write</span></span>
- <span data-ttu-id="9c566-123">Удаление</span><span class="sxs-lookup"><span data-stu-id="9c566-123">Delete</span></span>
- <span data-ttu-id="9c566-124">Весь</span><span class="sxs-lookup"><span data-stu-id="9c566-124">All</span></span>

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

### <span data-ttu-id="9c566-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c566-125">-PassThru</span></span>
<span data-ttu-id="9c566-126">Указывает на то, что этот командлет возвращает обновленные свойства ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="9c566-126">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="9c566-127">Если этот параметр не указан, этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="9c566-127">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="9c566-128">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="9c566-128">-RetentionDays</span></span>
<span data-ttu-id="9c566-129">Указывает количество дней, в течение которых служба хранилища Azure сохраняет данные, записанные в журнал.</span><span class="sxs-lookup"><span data-stu-id="9c566-129">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

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

### <span data-ttu-id="9c566-130">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="9c566-130">-ServiceType</span></span>
<span data-ttu-id="9c566-131">Указывает тип службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="9c566-131">Specifies the storage service type.</span></span>
<span data-ttu-id="9c566-132">Этот командлет изменяет свойства ведения журнала для типа службы, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="9c566-132">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="9c566-133">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9c566-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9c566-134">Большом</span><span class="sxs-lookup"><span data-stu-id="9c566-134">Blob</span></span> 
- <span data-ttu-id="9c566-135">Таблич</span><span class="sxs-lookup"><span data-stu-id="9c566-135">Table</span></span>
- <span data-ttu-id="9c566-136">Поместить</span><span class="sxs-lookup"><span data-stu-id="9c566-136">Queue</span></span>
- <span data-ttu-id="9c566-137">Файл</span><span class="sxs-lookup"><span data-stu-id="9c566-137">File</span></span>

<span data-ttu-id="9c566-138">Значение "файл" в настоящее время не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9c566-138">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="9c566-139">-Version</span><span class="sxs-lookup"><span data-stu-id="9c566-139">-Version</span></span>
<span data-ttu-id="9c566-140">Указывает версию ведения журнала службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="9c566-140">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="9c566-141">Значение по умолчанию — 1,0.</span><span class="sxs-lookup"><span data-stu-id="9c566-141">The default value is 1.0.</span></span>

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

### <span data-ttu-id="9c566-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c566-142">CommonParameters</span></span>
<span data-ttu-id="9c566-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9c566-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c566-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c566-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c566-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9c566-145">INPUTS</span></span>

### <span data-ttu-id="9c566-146">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9c566-146">IStorageContext</span></span>

<span data-ttu-id="9c566-147">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="9c566-147">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="9c566-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c566-148">OUTPUTS</span></span>

### <span data-ttu-id="9c566-149">Microsoft. WindowsAzure. Storage. Shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="9c566-149">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="9c566-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="9c566-150">NOTES</span></span>

## <span data-ttu-id="9c566-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9c566-151">RELATED LINKS</span></span>

[<span data-ttu-id="9c566-152">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="9c566-152">Get-AzureStorageServiceLoggingProperty</span></span>](./Get-AzureStorageServiceLoggingProperty.md)

[<span data-ttu-id="9c566-153">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="9c566-153">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


