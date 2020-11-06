---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueue.md
ms.openlocfilehash: 6363b8030571d6cf3e89b30229395b16cdb5f44b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565070"
---
# <span data-ttu-id="d5743-101">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="d5743-101">New-AzureStorageQueue</span></span>

## <span data-ttu-id="d5743-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d5743-102">SYNOPSIS</span></span>
<span data-ttu-id="d5743-103">Создание очереди хранилища.</span><span class="sxs-lookup"><span data-stu-id="d5743-103">Creates a storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5743-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d5743-104">SYNTAX</span></span>

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="d5743-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5743-105">DESCRIPTION</span></span>
<span data-ttu-id="d5743-106">Командлет **New-AzureStorageQueue** создает очередь хранилища в Azure.</span><span class="sxs-lookup"><span data-stu-id="d5743-106">The **New-AzureStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="d5743-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d5743-107">EXAMPLES</span></span>

### <span data-ttu-id="d5743-108">Пример 1: создание очереди хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="d5743-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

<span data-ttu-id="d5743-109">В этом примере создается очередь хранилища с именем queueabc.</span><span class="sxs-lookup"><span data-stu-id="d5743-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="d5743-110">Пример 2: создание нескольких очередей хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="d5743-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

<span data-ttu-id="d5743-111">В этом примере создается несколько очередей хранилища.</span><span class="sxs-lookup"><span data-stu-id="d5743-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="d5743-112">Он использует метод Split класса String .NET и передает имена в конвейере.</span><span class="sxs-lookup"><span data-stu-id="d5743-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="d5743-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d5743-113">PARAMETERS</span></span>

### <span data-ttu-id="d5743-114">-Context</span><span class="sxs-lookup"><span data-stu-id="d5743-114">-Context</span></span>
<span data-ttu-id="d5743-115">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="d5743-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="d5743-116">Вы можете создать его с помощью командлета New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="d5743-116">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d5743-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d5743-117">-Name</span></span>
<span data-ttu-id="d5743-118">Указывает имя очереди.</span><span class="sxs-lookup"><span data-stu-id="d5743-118">Specifies a name for the queue.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5743-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5743-119">CommonParameters</span></span>
<span data-ttu-id="d5743-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d5743-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5743-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5743-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5743-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d5743-122">INPUTS</span></span>

### <span data-ttu-id="d5743-123">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d5743-123">IStorageContext</span></span>

<span data-ttu-id="d5743-124">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="d5743-124">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="d5743-125">Подстрок</span><span class="sxs-lookup"><span data-stu-id="d5743-125">String</span></span>

<span data-ttu-id="d5743-126">Параметр Name принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="d5743-126">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="d5743-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5743-127">OUTPUTS</span></span>

### <span data-ttu-id="d5743-128">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="d5743-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="d5743-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="d5743-129">NOTES</span></span>

## <span data-ttu-id="d5743-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d5743-130">RELATED LINKS</span></span>

[<span data-ttu-id="d5743-131">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="d5743-131">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="d5743-132">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="d5743-132">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


