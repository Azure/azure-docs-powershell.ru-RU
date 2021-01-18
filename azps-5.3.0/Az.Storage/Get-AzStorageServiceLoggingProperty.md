---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 6e4eced11a9de228f836e80e9f25350e3f09a8c0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517101"
---
# <span data-ttu-id="18791-101">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="18791-101">Get-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="18791-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18791-102">SYNOPSIS</span></span>
<span data-ttu-id="18791-103">Получает свойства ведения журнала для служб хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="18791-103">Gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="18791-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="18791-104">SYNTAX</span></span>

```
Get-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18791-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="18791-105">DESCRIPTION</span></span>
<span data-ttu-id="18791-106">Чтобы получить свойства для служб хранилища Azure, можно получить свойства для **get-AzStorageServiceLoggingProperty.**</span><span class="sxs-lookup"><span data-stu-id="18791-106">The **Get-AzStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="18791-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="18791-107">EXAMPLES</span></span>

### <span data-ttu-id="18791-108">Пример 1. Получить свойства ведения журнала для службы BLOB-объектов</span><span class="sxs-lookup"><span data-stu-id="18791-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="18791-109">Эта команда получает свойства ведения журнала для хранилища BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="18791-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="18791-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18791-110">PARAMETERS</span></span>

### <span data-ttu-id="18791-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="18791-111">-Context</span></span>
<span data-ttu-id="18791-112">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="18791-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="18791-113">Для получения контекста хранилища используйте New-AzStorageContext управления.</span><span class="sxs-lookup"><span data-stu-id="18791-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="18791-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18791-114">-DefaultProfile</span></span>
<span data-ttu-id="18791-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="18791-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18791-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="18791-116">-ServiceType</span></span>
<span data-ttu-id="18791-117">Тип службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="18791-117">Specifies the storage service type.</span></span>
<span data-ttu-id="18791-118">Этот cmdlet получает свойства ведения журнала для типа службы, указанного этим параметром.</span><span class="sxs-lookup"><span data-stu-id="18791-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="18791-119">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="18791-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="18791-120">BLOB</span><span class="sxs-lookup"><span data-stu-id="18791-120">Blob</span></span> 
- <span data-ttu-id="18791-121">Таблица</span><span class="sxs-lookup"><span data-stu-id="18791-121">Table</span></span>
- <span data-ttu-id="18791-122">Очередь</span><span class="sxs-lookup"><span data-stu-id="18791-122">Queue</span></span>
- <span data-ttu-id="18791-123">Файл Со значением "Файл" в настоящее время не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="18791-123">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="18791-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18791-124">CommonParameters</span></span>
<span data-ttu-id="18791-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18791-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18791-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18791-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18791-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="18791-127">INPUTS</span></span>

### <span data-ttu-id="18791-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="18791-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="18791-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="18791-129">OUTPUTS</span></span>

### <span data-ttu-id="18791-130">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="18791-130">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="18791-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="18791-131">NOTES</span></span>

## <span data-ttu-id="18791-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="18791-132">RELATED LINKS</span></span>

[<span data-ttu-id="18791-133">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="18791-133">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="18791-134">Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="18791-134">Set-AzStorageServiceLoggingProperty</span></span>](./Set-AzStorageServiceLoggingProperty.md)


