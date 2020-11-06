---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceLoggingProperty.md
ms.openlocfilehash: fb526bbd33e30e4ea125e9662926c7ea4c7bbb00
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566000"
---
# <span data-ttu-id="16cff-101">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="16cff-101">Set-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="16cff-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="16cff-102">SYNOPSIS</span></span>
<span data-ttu-id="16cff-103">Изменяет ведение журнала для служб хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="16cff-103">Modifies logging for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16cff-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="16cff-104">SYNTAX</span></span>

```
Set-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16cff-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="16cff-105">DESCRIPTION</span></span>
<span data-ttu-id="16cff-106">Командлет **Set-AzureStorageServiceLoggingProperty** изменяет ведение журнала для служб хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="16cff-106">The **Set-AzureStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="16cff-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="16cff-107">EXAMPLES</span></span>

### <span data-ttu-id="16cff-108">Пример 1: изменение свойств ведения журнала для службы больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="16cff-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="16cff-109">Эта команда изменяет ведение журнала версии 1,0 для хранилища BLOB-объектов, включая операции чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="16cff-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="16cff-110">Ведение журнала службы хранилища Azure сохраняет записи в течение 10 дней.</span><span class="sxs-lookup"><span data-stu-id="16cff-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="16cff-111">Так как эта команда задает параметр *PassThru* , команда отображает измененные свойства ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="16cff-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="16cff-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="16cff-112">PARAMETERS</span></span>

### <span data-ttu-id="16cff-113">-Context</span><span class="sxs-lookup"><span data-stu-id="16cff-113">-Context</span></span>
<span data-ttu-id="16cff-114">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="16cff-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="16cff-115">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="16cff-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="16cff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16cff-116">-DefaultProfile</span></span>
<span data-ttu-id="16cff-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="16cff-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16cff-118">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="16cff-118">-LoggingOperations</span></span>
<span data-ttu-id="16cff-119">Указывает массив операций службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="16cff-119">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="16cff-120">Службы хранилища Azure регистрируют операции, которые указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="16cff-120">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="16cff-121">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="16cff-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="16cff-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="16cff-122">None</span></span>
- <span data-ttu-id="16cff-123">Читаются</span><span class="sxs-lookup"><span data-stu-id="16cff-123">Read</span></span>
- <span data-ttu-id="16cff-124">Пишу</span><span class="sxs-lookup"><span data-stu-id="16cff-124">Write</span></span>
- <span data-ttu-id="16cff-125">Удаление</span><span class="sxs-lookup"><span data-stu-id="16cff-125">Delete</span></span>
- <span data-ttu-id="16cff-126">Весь</span><span class="sxs-lookup"><span data-stu-id="16cff-126">All</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingOperations[]
Parameter Sets: (All)
Aliases:
Accepted values: None, Read, Write, Delete, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16cff-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16cff-127">-PassThru</span></span>
<span data-ttu-id="16cff-128">Указывает на то, что этот командлет возвращает обновленные свойства ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="16cff-128">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="16cff-129">Если этот параметр не указан, этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="16cff-129">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="16cff-130">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="16cff-130">-RetentionDays</span></span>
<span data-ttu-id="16cff-131">Указывает количество дней, в течение которых служба хранилища Azure сохраняет данные, записанные в журнал.</span><span class="sxs-lookup"><span data-stu-id="16cff-131">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

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

### <span data-ttu-id="16cff-132">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="16cff-132">-ServiceType</span></span>
<span data-ttu-id="16cff-133">Указывает тип службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="16cff-133">Specifies the storage service type.</span></span>
<span data-ttu-id="16cff-134">Этот командлет изменяет свойства ведения журнала для типа службы, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="16cff-134">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="16cff-135">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="16cff-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="16cff-136">Большом</span><span class="sxs-lookup"><span data-stu-id="16cff-136">Blob</span></span> 
- <span data-ttu-id="16cff-137">Таблич</span><span class="sxs-lookup"><span data-stu-id="16cff-137">Table</span></span>
- <span data-ttu-id="16cff-138">Поместить</span><span class="sxs-lookup"><span data-stu-id="16cff-138">Queue</span></span>
- <span data-ttu-id="16cff-139">Файл. значение файла в настоящее время не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="16cff-139">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="16cff-140">-Version</span><span class="sxs-lookup"><span data-stu-id="16cff-140">-Version</span></span>
<span data-ttu-id="16cff-141">Указывает версию ведения журнала службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="16cff-141">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="16cff-142">Значение по умолчанию — 1,0.</span><span class="sxs-lookup"><span data-stu-id="16cff-142">The default value is 1.0.</span></span>

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

### <span data-ttu-id="16cff-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16cff-143">CommonParameters</span></span>
<span data-ttu-id="16cff-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="16cff-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16cff-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16cff-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16cff-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="16cff-146">INPUTS</span></span>

### <span data-ttu-id="16cff-147">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="16cff-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="16cff-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="16cff-148">OUTPUTS</span></span>

### <span data-ttu-id="16cff-149">Microsoft. WindowsAzure. Storage. Shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="16cff-149">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="16cff-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="16cff-150">NOTES</span></span>

## <span data-ttu-id="16cff-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="16cff-151">RELATED LINKS</span></span>

[<span data-ttu-id="16cff-152">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="16cff-152">Get-AzureStorageServiceLoggingProperty</span></span>](./Get-AzureStorageServiceLoggingProperty.md)

[<span data-ttu-id="16cff-153">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="16cff-153">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


