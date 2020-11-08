---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 21c182dff12f8dd373000a295f964bd59484e337
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245762"
---
# <span data-ttu-id="c7763-101">Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="c7763-101">Set-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="c7763-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c7763-102">SYNOPSIS</span></span>
<span data-ttu-id="c7763-103">Изменяет ведение журнала для служб хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c7763-103">Modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="c7763-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c7763-104">SYNTAX</span></span>

```
Set-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7763-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7763-105">DESCRIPTION</span></span>
<span data-ttu-id="c7763-106">Командлет **Set-AzStorageServiceLoggingProperty** изменяет ведение журнала для служб хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c7763-106">The **Set-AzStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="c7763-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c7763-107">EXAMPLES</span></span>

### <span data-ttu-id="c7763-108">Пример 1: изменение свойств ведения журнала для службы больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="c7763-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="c7763-109">Эта команда изменяет ведение журнала версии 1,0 для хранилища BLOB-объектов, включая операции чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="c7763-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="c7763-110">Ведение журнала службы хранилища Azure сохраняет записи в течение 10 дней.</span><span class="sxs-lookup"><span data-stu-id="c7763-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="c7763-111">Так как эта команда задает параметр *PassThru* , команда отображает измененные свойства ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="c7763-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="c7763-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c7763-112">PARAMETERS</span></span>

### <span data-ttu-id="c7763-113">-Context</span><span class="sxs-lookup"><span data-stu-id="c7763-113">-Context</span></span>
<span data-ttu-id="c7763-114">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c7763-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c7763-115">Чтобы получить контекст хранилища, используйте командлет New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="c7763-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c7763-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7763-116">-DefaultProfile</span></span>
<span data-ttu-id="c7763-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c7763-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7763-118">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="c7763-118">-LoggingOperations</span></span>
<span data-ttu-id="c7763-119">Указывает массив операций службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c7763-119">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="c7763-120">Службы хранилища Azure регистрируют операции, которые указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="c7763-120">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="c7763-121">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c7763-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c7763-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="c7763-122">None</span></span>
- <span data-ttu-id="c7763-123">Читаются</span><span class="sxs-lookup"><span data-stu-id="c7763-123">Read</span></span>
- <span data-ttu-id="c7763-124">Пишу</span><span class="sxs-lookup"><span data-stu-id="c7763-124">Write</span></span>
- <span data-ttu-id="c7763-125">Удаление</span><span class="sxs-lookup"><span data-stu-id="c7763-125">Delete</span></span>
- <span data-ttu-id="c7763-126">Весь</span><span class="sxs-lookup"><span data-stu-id="c7763-126">All</span></span>

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

### <span data-ttu-id="c7763-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7763-127">-PassThru</span></span>
<span data-ttu-id="c7763-128">Указывает на то, что этот командлет возвращает обновленные свойства ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="c7763-128">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="c7763-129">Если этот параметр не указан, этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c7763-129">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="c7763-130">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="c7763-130">-RetentionDays</span></span>
<span data-ttu-id="c7763-131">Указывает количество дней, в течение которых служба хранилища Azure сохраняет данные, записанные в журнал.</span><span class="sxs-lookup"><span data-stu-id="c7763-131">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

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

### <span data-ttu-id="c7763-132">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="c7763-132">-ServiceType</span></span>
<span data-ttu-id="c7763-133">Указывает тип службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="c7763-133">Specifies the storage service type.</span></span>
<span data-ttu-id="c7763-134">Этот командлет изменяет свойства ведения журнала для типа службы, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="c7763-134">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="c7763-135">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c7763-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c7763-136">Большом</span><span class="sxs-lookup"><span data-stu-id="c7763-136">Blob</span></span> 
- <span data-ttu-id="c7763-137">Таблич</span><span class="sxs-lookup"><span data-stu-id="c7763-137">Table</span></span>
- <span data-ttu-id="c7763-138">Поместить</span><span class="sxs-lookup"><span data-stu-id="c7763-138">Queue</span></span>
- <span data-ttu-id="c7763-139">Файл. значение файла в настоящее время не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c7763-139">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="c7763-140">-Version</span><span class="sxs-lookup"><span data-stu-id="c7763-140">-Version</span></span>
<span data-ttu-id="c7763-141">Указывает версию ведения журнала службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c7763-141">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="c7763-142">Значение по умолчанию — 1,0.</span><span class="sxs-lookup"><span data-stu-id="c7763-142">The default value is 1.0.</span></span>

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

### <span data-ttu-id="c7763-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7763-143">CommonParameters</span></span>
<span data-ttu-id="c7763-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c7763-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7763-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7763-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7763-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c7763-146">INPUTS</span></span>

### <span data-ttu-id="c7763-147">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c7763-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c7763-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7763-148">OUTPUTS</span></span>

### <span data-ttu-id="c7763-149">Microsoft. Azure. Storage. Sharing. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="c7763-149">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="c7763-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="c7763-150">NOTES</span></span>

## <span data-ttu-id="c7763-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c7763-151">RELATED LINKS</span></span>

[<span data-ttu-id="c7763-152">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="c7763-152">Get-AzStorageServiceLoggingProperty</span></span>](./Get-AzStorageServiceLoggingProperty.md)

[<span data-ttu-id="c7763-153">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="c7763-153">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


