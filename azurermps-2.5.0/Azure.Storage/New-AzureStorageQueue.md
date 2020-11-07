---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeue
schema: 2.0.0
ms.openlocfilehash: a028d2528d74e9372bfca28ccfb085f119486ce7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914282"
---
# <span data-ttu-id="192ce-101">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="192ce-101">New-AzureStorageQueue</span></span>

## <span data-ttu-id="192ce-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="192ce-102">SYNOPSIS</span></span>
<span data-ttu-id="192ce-103">Создание очереди хранилища.</span><span class="sxs-lookup"><span data-stu-id="192ce-103">Creates a storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="192ce-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="192ce-104">SYNTAX</span></span>

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="192ce-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="192ce-105">DESCRIPTION</span></span>
<span data-ttu-id="192ce-106">Командлет **New-AzureStorageQueue** создает очередь хранилища в Azure.</span><span class="sxs-lookup"><span data-stu-id="192ce-106">The **New-AzureStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="192ce-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="192ce-107">EXAMPLES</span></span>

### <span data-ttu-id="192ce-108">Пример 1: создание очереди хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="192ce-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

<span data-ttu-id="192ce-109">В этом примере создается очередь хранилища с именем queueabc.</span><span class="sxs-lookup"><span data-stu-id="192ce-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="192ce-110">Пример 2: создание нескольких очередей хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="192ce-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

<span data-ttu-id="192ce-111">В этом примере создается несколько очередей хранилища.</span><span class="sxs-lookup"><span data-stu-id="192ce-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="192ce-112">Он использует метод Split класса String .NET и передает имена в конвейере.</span><span class="sxs-lookup"><span data-stu-id="192ce-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="192ce-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="192ce-113">PARAMETERS</span></span>

### <span data-ttu-id="192ce-114">-Context</span><span class="sxs-lookup"><span data-stu-id="192ce-114">-Context</span></span>
<span data-ttu-id="192ce-115">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="192ce-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="192ce-116">Вы можете создать его с помощью командлета New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="192ce-116">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="192ce-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="192ce-117">-DefaultProfile</span></span>
<span data-ttu-id="192ce-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="192ce-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="192ce-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="192ce-119">-Name</span></span>
<span data-ttu-id="192ce-120">Указывает имя очереди.</span><span class="sxs-lookup"><span data-stu-id="192ce-120">Specifies a name for the queue.</span></span>

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

### <span data-ttu-id="192ce-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="192ce-121">CommonParameters</span></span>
<span data-ttu-id="192ce-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="192ce-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="192ce-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="192ce-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="192ce-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="192ce-124">INPUTS</span></span>

### <span data-ttu-id="192ce-125">System. String</span><span class="sxs-lookup"><span data-stu-id="192ce-125">System.String</span></span>

### <span data-ttu-id="192ce-126">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="192ce-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="192ce-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="192ce-127">OUTPUTS</span></span>

### <span data-ttu-id="192ce-128">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="192ce-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="192ce-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="192ce-129">NOTES</span></span>

## <span data-ttu-id="192ce-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="192ce-130">RELATED LINKS</span></span>

[<span data-ttu-id="192ce-131">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="192ce-131">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="192ce-132">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="192ce-132">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


