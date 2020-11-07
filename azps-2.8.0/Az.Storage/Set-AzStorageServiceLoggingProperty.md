---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 43b8c6426fe2d4eceab65fc1b103e62cdb1eb346
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720308"
---
# <span data-ttu-id="afb6d-101">Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="afb6d-101">Set-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="afb6d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="afb6d-102">SYNOPSIS</span></span>
<span data-ttu-id="afb6d-103">Изменяет ведение журнала для служб хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="afb6d-103">Modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="afb6d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="afb6d-104">SYNTAX</span></span>

```
Set-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="afb6d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="afb6d-105">DESCRIPTION</span></span>
<span data-ttu-id="afb6d-106">Командлет **Set-AzStorageServiceLoggingProperty** изменяет ведение журнала для служб хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="afb6d-106">The **Set-AzStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="afb6d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="afb6d-107">EXAMPLES</span></span>

### <span data-ttu-id="afb6d-108">Пример 1: изменение свойств ведения журнала для службы больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="afb6d-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="afb6d-109">Эта команда изменяет ведение журнала версии 1,0 для хранилища BLOB-объектов, включая операции чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="afb6d-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="afb6d-110">Ведение журнала службы хранилища Azure сохраняет записи в течение 10 дней.</span><span class="sxs-lookup"><span data-stu-id="afb6d-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="afb6d-111">Так как эта команда задает параметр *PassThru* , команда отображает измененные свойства ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="afb6d-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="afb6d-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="afb6d-112">PARAMETERS</span></span>

### <span data-ttu-id="afb6d-113">-Context</span><span class="sxs-lookup"><span data-stu-id="afb6d-113">-Context</span></span>
<span data-ttu-id="afb6d-114">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="afb6d-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="afb6d-115">Чтобы получить контекст хранилища, используйте командлет New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="afb6d-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="afb6d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afb6d-116">-DefaultProfile</span></span>
<span data-ttu-id="afb6d-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="afb6d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afb6d-118">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="afb6d-118">-LoggingOperations</span></span>
<span data-ttu-id="afb6d-119">Указывает массив операций службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="afb6d-119">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="afb6d-120">Службы хранилища Azure регистрируют операции, которые указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="afb6d-120">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="afb6d-121">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="afb6d-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="afb6d-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="afb6d-122">None</span></span>
- <span data-ttu-id="afb6d-123">Читаются</span><span class="sxs-lookup"><span data-stu-id="afb6d-123">Read</span></span>
- <span data-ttu-id="afb6d-124">Пишу</span><span class="sxs-lookup"><span data-stu-id="afb6d-124">Write</span></span>
- <span data-ttu-id="afb6d-125">Удаление</span><span class="sxs-lookup"><span data-stu-id="afb6d-125">Delete</span></span>
- <span data-ttu-id="afb6d-126">Весь</span><span class="sxs-lookup"><span data-stu-id="afb6d-126">All</span></span>

```yaml
Type: Microsoft.Azure.Storage.Shared.Protocol.LoggingOperations[]
Parameter Sets: (All)
Aliases:
Accepted values: None, Read, Write, Delete, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afb6d-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="afb6d-127">-PassThru</span></span>
<span data-ttu-id="afb6d-128">Указывает на то, что этот командлет возвращает обновленные свойства ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="afb6d-128">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="afb6d-129">Если этот параметр не указан, этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="afb6d-129">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="afb6d-130">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="afb6d-130">-RetentionDays</span></span>
<span data-ttu-id="afb6d-131">Указывает количество дней, в течение которых служба хранилища Azure сохраняет данные, записанные в журнал.</span><span class="sxs-lookup"><span data-stu-id="afb6d-131">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

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

### <span data-ttu-id="afb6d-132">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="afb6d-132">-ServiceType</span></span>
<span data-ttu-id="afb6d-133">Указывает тип службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="afb6d-133">Specifies the storage service type.</span></span>
<span data-ttu-id="afb6d-134">Этот командлет изменяет свойства ведения журнала для типа службы, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="afb6d-134">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="afb6d-135">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="afb6d-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="afb6d-136">Большом</span><span class="sxs-lookup"><span data-stu-id="afb6d-136">Blob</span></span> 
- <span data-ttu-id="afb6d-137">Таблич</span><span class="sxs-lookup"><span data-stu-id="afb6d-137">Table</span></span>
- <span data-ttu-id="afb6d-138">Поместить</span><span class="sxs-lookup"><span data-stu-id="afb6d-138">Queue</span></span>
- <span data-ttu-id="afb6d-139">Файл. значение файла в настоящее время не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="afb6d-139">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="afb6d-140">-Version</span><span class="sxs-lookup"><span data-stu-id="afb6d-140">-Version</span></span>
<span data-ttu-id="afb6d-141">Указывает версию ведения журнала службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="afb6d-141">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="afb6d-142">Значение по умолчанию — 1,0.</span><span class="sxs-lookup"><span data-stu-id="afb6d-142">The default value is 1.0.</span></span>

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

### <span data-ttu-id="afb6d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afb6d-143">CommonParameters</span></span>
<span data-ttu-id="afb6d-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="afb6d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afb6d-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afb6d-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afb6d-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="afb6d-146">INPUTS</span></span>

### <span data-ttu-id="afb6d-147">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="afb6d-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="afb6d-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="afb6d-148">OUTPUTS</span></span>

### <span data-ttu-id="afb6d-149">Microsoft. Azure. Storage. Sharing. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="afb6d-149">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="afb6d-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="afb6d-150">NOTES</span></span>

## <span data-ttu-id="afb6d-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="afb6d-151">RELATED LINKS</span></span>

[<span data-ttu-id="afb6d-152">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="afb6d-152">Get-AzStorageServiceLoggingProperty</span></span>](./Get-AzStorageServiceLoggingProperty.md)

[<span data-ttu-id="afb6d-153">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="afb6d-153">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


