---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 21c182dff12f8dd373000a295f964bd59484e337
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403263"
---
# <span data-ttu-id="8d3b8-101">Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="8d3b8-101">Set-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="8d3b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d3b8-102">SYNOPSIS</span></span>
<span data-ttu-id="8d3b8-103">Изменяет ведение журнала для служб хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="8d3b8-103">Modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="8d3b8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8d3b8-104">SYNTAX</span></span>

```
Set-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d3b8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d3b8-105">DESCRIPTION</span></span>
<span data-ttu-id="8d3b8-106">**Cmdlet Set-AzStorageServiceLoggingProperty** изменяет ведение журнала для служб хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="8d3b8-106">The **Set-AzStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="8d3b8-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8d3b8-107">EXAMPLES</span></span>

### <span data-ttu-id="8d3b8-108">Пример 1. Изменение свойств ведения журнала для службы BLOB-объектов</span><span class="sxs-lookup"><span data-stu-id="8d3b8-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="8d3b8-109">Эта команда изменяет ведение журнала версии 1.0 для хранилища BLOB-устройств, включая операции чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="8d3b8-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="8d3b8-110">Журнал службы хранилища Azure сохраняет записи в течение 10 дней.</span><span class="sxs-lookup"><span data-stu-id="8d3b8-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="8d3b8-111">Так как эта команда указывает параметр *PassThru,* она отображает измененные свойства ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="8d3b8-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="8d3b8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d3b8-112">PARAMETERS</span></span>

### <span data-ttu-id="8d3b8-113">-Контекст</span><span class="sxs-lookup"><span data-stu-id="8d3b8-113">-Context</span></span>
<span data-ttu-id="8d3b8-114">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="8d3b8-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8d3b8-115">Для получения контекста хранилища используйте New-AzStorageContext управления.</span><span class="sxs-lookup"><span data-stu-id="8d3b8-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8d3b8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d3b8-116">-DefaultProfile</span></span>
<span data-ttu-id="8d3b8-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8d3b8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d3b8-118">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="8d3b8-118">-LoggingOperations</span></span>
<span data-ttu-id="8d3b8-119">Указывает массив операций службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="8d3b8-119">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="8d3b8-120">Службы хранилища Azure регистрирует операции, указанные этим параметром.</span><span class="sxs-lookup"><span data-stu-id="8d3b8-120">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="8d3b8-121">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="8d3b8-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8d3b8-122">Нет</span><span class="sxs-lookup"><span data-stu-id="8d3b8-122">None</span></span>
- <span data-ttu-id="8d3b8-123">Чтение</span><span class="sxs-lookup"><span data-stu-id="8d3b8-123">Read</span></span>
- <span data-ttu-id="8d3b8-124">Написание</span><span class="sxs-lookup"><span data-stu-id="8d3b8-124">Write</span></span>
- <span data-ttu-id="8d3b8-125">Удалить</span><span class="sxs-lookup"><span data-stu-id="8d3b8-125">Delete</span></span>
- <span data-ttu-id="8d3b8-126">Все</span><span class="sxs-lookup"><span data-stu-id="8d3b8-126">All</span></span>

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

### <span data-ttu-id="8d3b8-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d3b8-127">-PassThru</span></span>
<span data-ttu-id="8d3b8-128">Указывает на то, что этот cmdlet возвращает обновленные свойства ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="8d3b8-128">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="8d3b8-129">Если этот параметр не задан, этот cmdlet не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="8d3b8-129">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="8d3b8-130">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="8d3b8-130">-RetentionDays</span></span>
<span data-ttu-id="8d3b8-131">Определяет количество дней, в течение дня в течение дня, в течение которое служба хранилища Azure сохраняет данные из журнала.</span><span class="sxs-lookup"><span data-stu-id="8d3b8-131">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

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

### <span data-ttu-id="8d3b8-132">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="8d3b8-132">-ServiceType</span></span>
<span data-ttu-id="8d3b8-133">Тип службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="8d3b8-133">Specifies the storage service type.</span></span>
<span data-ttu-id="8d3b8-134">Этот cmdlet изменяет свойства ведения журнала для типа службы, указанного этим параметром.</span><span class="sxs-lookup"><span data-stu-id="8d3b8-134">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="8d3b8-135">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="8d3b8-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8d3b8-136">BLOB</span><span class="sxs-lookup"><span data-stu-id="8d3b8-136">Blob</span></span> 
- <span data-ttu-id="8d3b8-137">Таблица</span><span class="sxs-lookup"><span data-stu-id="8d3b8-137">Table</span></span>
- <span data-ttu-id="8d3b8-138">Очередь</span><span class="sxs-lookup"><span data-stu-id="8d3b8-138">Queue</span></span>
- <span data-ttu-id="8d3b8-139">Файл, в который в настоящее время не поддерживается значение "Файл".</span><span class="sxs-lookup"><span data-stu-id="8d3b8-139">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="8d3b8-140">-Версия</span><span class="sxs-lookup"><span data-stu-id="8d3b8-140">-Version</span></span>
<span data-ttu-id="8d3b8-141">Указывает версию журнала службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="8d3b8-141">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="8d3b8-142">Значение по умолчанию — 1,0.</span><span class="sxs-lookup"><span data-stu-id="8d3b8-142">The default value is 1.0.</span></span>

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

### <span data-ttu-id="8d3b8-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d3b8-143">CommonParameters</span></span>
<span data-ttu-id="8d3b8-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d3b8-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d3b8-145">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d3b8-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d3b8-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8d3b8-146">INPUTS</span></span>

### <span data-ttu-id="8d3b8-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8d3b8-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8d3b8-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8d3b8-148">OUTPUTS</span></span>

### <span data-ttu-id="8d3b8-149">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="8d3b8-149">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="8d3b8-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8d3b8-150">NOTES</span></span>

## <span data-ttu-id="8d3b8-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8d3b8-151">RELATED LINKS</span></span>

[<span data-ttu-id="8d3b8-152">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="8d3b8-152">Get-AzStorageServiceLoggingProperty</span></span>](./Get-AzStorageServiceLoggingProperty.md)

[<span data-ttu-id="8d3b8-153">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="8d3b8-153">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


