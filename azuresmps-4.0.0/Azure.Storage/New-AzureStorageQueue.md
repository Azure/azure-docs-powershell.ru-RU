---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 76876cb76e65c913401d62fc7f08b3cb8b5626c0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555899"
---
# <span data-ttu-id="bbc12-101">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="bbc12-101">New-AzureStorageQueue</span></span>

## <span data-ttu-id="bbc12-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bbc12-102">SYNOPSIS</span></span>
<span data-ttu-id="bbc12-103">Создание очереди хранилища.</span><span class="sxs-lookup"><span data-stu-id="bbc12-103">Creates a storage queue.</span></span>

## <span data-ttu-id="bbc12-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bbc12-104">SYNTAX</span></span>

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="bbc12-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bbc12-105">DESCRIPTION</span></span>
<span data-ttu-id="bbc12-106">Командлет **New-AzureStorageQueue** создает очередь хранилища в Azure.</span><span class="sxs-lookup"><span data-stu-id="bbc12-106">The **New-AzureStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="bbc12-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bbc12-107">EXAMPLES</span></span>

### <span data-ttu-id="bbc12-108">Пример 1: создание очереди хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="bbc12-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

<span data-ttu-id="bbc12-109">В этом примере создается очередь хранилища с именем queueabc.</span><span class="sxs-lookup"><span data-stu-id="bbc12-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="bbc12-110">Пример 2: создание нескольких очередей хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="bbc12-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

<span data-ttu-id="bbc12-111">В этом примере создается несколько очередей хранилища.</span><span class="sxs-lookup"><span data-stu-id="bbc12-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="bbc12-112">Он использует метод Split класса String .NET и передает имена в конвейере.</span><span class="sxs-lookup"><span data-stu-id="bbc12-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="bbc12-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bbc12-113">PARAMETERS</span></span>

### <span data-ttu-id="bbc12-114">-Context</span><span class="sxs-lookup"><span data-stu-id="bbc12-114">-Context</span></span>
<span data-ttu-id="bbc12-115">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="bbc12-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="bbc12-116">Вы можете создать его с помощью командлета New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="bbc12-116">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="bbc12-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bbc12-117">-Name</span></span>
<span data-ttu-id="bbc12-118">Указывает имя очереди.</span><span class="sxs-lookup"><span data-stu-id="bbc12-118">Specifies a name for the queue.</span></span>

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

### <span data-ttu-id="bbc12-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbc12-119">CommonParameters</span></span>
<span data-ttu-id="bbc12-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bbc12-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbc12-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbc12-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbc12-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bbc12-122">INPUTS</span></span>

## <span data-ttu-id="bbc12-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bbc12-123">OUTPUTS</span></span>

## <span data-ttu-id="bbc12-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="bbc12-124">NOTES</span></span>

## <span data-ttu-id="bbc12-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bbc12-125">RELATED LINKS</span></span>

[<span data-ttu-id="bbc12-126">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="bbc12-126">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="bbc12-127">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="bbc12-127">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


