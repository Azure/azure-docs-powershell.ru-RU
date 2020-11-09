---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 6e4eced11a9de228f836e80e9f25350e3f09a8c0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246343"
---
# <span data-ttu-id="3636f-101">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="3636f-101">Get-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="3636f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3636f-102">SYNOPSIS</span></span>
<span data-ttu-id="3636f-103">Получение свойств ведения журнала для служб хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="3636f-103">Gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="3636f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3636f-104">SYNTAX</span></span>

```
Get-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3636f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3636f-105">DESCRIPTION</span></span>
<span data-ttu-id="3636f-106">Командлет **Get-AzStorageServiceLoggingProperty** получает свойства ведения журнала для служб хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="3636f-106">The **Get-AzStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="3636f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3636f-107">EXAMPLES</span></span>

### <span data-ttu-id="3636f-108">Пример 1: получение свойств ведения журнала для службы больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="3636f-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="3636f-109">Эта команда получает свойства ведения журнала для хранилища BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="3636f-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="3636f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3636f-110">PARAMETERS</span></span>

### <span data-ttu-id="3636f-111">-Context</span><span class="sxs-lookup"><span data-stu-id="3636f-111">-Context</span></span>
<span data-ttu-id="3636f-112">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="3636f-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3636f-113">Чтобы получить контекст хранилища, используйте командлет New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="3636f-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3636f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3636f-114">-DefaultProfile</span></span>
<span data-ttu-id="3636f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3636f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3636f-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="3636f-116">-ServiceType</span></span>
<span data-ttu-id="3636f-117">Указывает тип службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="3636f-117">Specifies the storage service type.</span></span>
<span data-ttu-id="3636f-118">Этот командлет получает свойства ведения журнала для типа службы, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="3636f-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="3636f-119">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3636f-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3636f-120">Большом</span><span class="sxs-lookup"><span data-stu-id="3636f-120">Blob</span></span> 
- <span data-ttu-id="3636f-121">Таблич</span><span class="sxs-lookup"><span data-stu-id="3636f-121">Table</span></span>
- <span data-ttu-id="3636f-122">Поместить</span><span class="sxs-lookup"><span data-stu-id="3636f-122">Queue</span></span>
- <span data-ttu-id="3636f-123">Файл. значение файла в настоящее время не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3636f-123">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="3636f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3636f-124">CommonParameters</span></span>
<span data-ttu-id="3636f-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3636f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3636f-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3636f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3636f-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3636f-127">INPUTS</span></span>

### <span data-ttu-id="3636f-128">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3636f-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3636f-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3636f-129">OUTPUTS</span></span>

### <span data-ttu-id="3636f-130">Microsoft. Azure. Storage. Sharing. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="3636f-130">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="3636f-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="3636f-131">NOTES</span></span>

## <span data-ttu-id="3636f-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3636f-132">RELATED LINKS</span></span>

[<span data-ttu-id="3636f-133">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="3636f-133">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="3636f-134">Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="3636f-134">Set-AzStorageServiceLoggingProperty</span></span>](./Set-AzStorageServiceLoggingProperty.md)

