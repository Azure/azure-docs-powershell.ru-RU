---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueue.md
ms.openlocfilehash: 62fc501c267e388498cb1563206d2efac083c058
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561279"
---
# <span data-ttu-id="b04a4-101">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="b04a4-101">New-AzureStorageQueue</span></span>

## <span data-ttu-id="b04a4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b04a4-102">SYNOPSIS</span></span>
<span data-ttu-id="b04a4-103">Создание очереди хранилища.</span><span class="sxs-lookup"><span data-stu-id="b04a4-103">Creates a storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b04a4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b04a4-104">SYNTAX</span></span>

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b04a4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b04a4-105">DESCRIPTION</span></span>
<span data-ttu-id="b04a4-106">Командлет **New-AzureStorageQueue** создает очередь хранилища в Azure.</span><span class="sxs-lookup"><span data-stu-id="b04a4-106">The **New-AzureStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="b04a4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b04a4-107">EXAMPLES</span></span>

### <span data-ttu-id="b04a4-108">Пример 1: создание очереди хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="b04a4-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

<span data-ttu-id="b04a4-109">В этом примере создается очередь хранилища с именем queueabc.</span><span class="sxs-lookup"><span data-stu-id="b04a4-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="b04a4-110">Пример 2: создание нескольких очередей хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="b04a4-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

<span data-ttu-id="b04a4-111">В этом примере создается несколько очередей хранилища.</span><span class="sxs-lookup"><span data-stu-id="b04a4-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="b04a4-112">Он использует метод Split класса String .NET и передает имена в конвейере.</span><span class="sxs-lookup"><span data-stu-id="b04a4-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="b04a4-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b04a4-113">PARAMETERS</span></span>

### <span data-ttu-id="b04a4-114">-Context</span><span class="sxs-lookup"><span data-stu-id="b04a4-114">-Context</span></span>
<span data-ttu-id="b04a4-115">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="b04a4-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="b04a4-116">Вы можете создать его с помощью командлета New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="b04a4-116">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b04a4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b04a4-117">-DefaultProfile</span></span>
<span data-ttu-id="b04a4-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b04a4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b04a4-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b04a4-119">-Name</span></span>
<span data-ttu-id="b04a4-120">Указывает имя очереди.</span><span class="sxs-lookup"><span data-stu-id="b04a4-120">Specifies a name for the queue.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b04a4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b04a4-121">CommonParameters</span></span>
<span data-ttu-id="b04a4-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b04a4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b04a4-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b04a4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b04a4-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b04a4-124">INPUTS</span></span>

### <span data-ttu-id="b04a4-125">System. String</span><span class="sxs-lookup"><span data-stu-id="b04a4-125">System.String</span></span>

### <span data-ttu-id="b04a4-126">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b04a4-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b04a4-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b04a4-127">OUTPUTS</span></span>

### <span data-ttu-id="b04a4-128">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="b04a4-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="b04a4-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="b04a4-129">NOTES</span></span>

## <span data-ttu-id="b04a4-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b04a4-130">RELATED LINKS</span></span>

[<span data-ttu-id="b04a4-131">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="b04a4-131">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="b04a4-132">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="b04a4-132">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


