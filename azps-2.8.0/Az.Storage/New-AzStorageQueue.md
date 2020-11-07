---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
ms.openlocfilehash: df6f616aacb066ec17aa089b8d91226a5bd171b8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904478"
---
# <span data-ttu-id="cdb2a-101">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="cdb2a-101">New-AzStorageQueue</span></span>

## <span data-ttu-id="cdb2a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cdb2a-102">SYNOPSIS</span></span>
<span data-ttu-id="cdb2a-103">Создание очереди хранилища.</span><span class="sxs-lookup"><span data-stu-id="cdb2a-103">Creates a storage queue.</span></span>

## <span data-ttu-id="cdb2a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cdb2a-104">SYNTAX</span></span>

```
New-AzStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cdb2a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cdb2a-105">DESCRIPTION</span></span>
<span data-ttu-id="cdb2a-106">Командлет **New-AzStorageQueue** создает очередь хранилища в Azure.</span><span class="sxs-lookup"><span data-stu-id="cdb2a-106">The **New-AzStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="cdb2a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cdb2a-107">EXAMPLES</span></span>

### <span data-ttu-id="cdb2a-108">Пример 1: создание очереди хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="cdb2a-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzStorageQueue -Name "queueabc"
```

<span data-ttu-id="cdb2a-109">В этом примере создается очередь хранилища с именем queueabc.</span><span class="sxs-lookup"><span data-stu-id="cdb2a-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="cdb2a-110">Пример 2: создание нескольких очередей хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="cdb2a-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzStorageQueue
```

<span data-ttu-id="cdb2a-111">В этом примере создается несколько очередей хранилища.</span><span class="sxs-lookup"><span data-stu-id="cdb2a-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="cdb2a-112">Он использует метод Split класса String .NET и передает имена в конвейере.</span><span class="sxs-lookup"><span data-stu-id="cdb2a-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="cdb2a-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cdb2a-113">PARAMETERS</span></span>

### <span data-ttu-id="cdb2a-114">-Context</span><span class="sxs-lookup"><span data-stu-id="cdb2a-114">-Context</span></span>
<span data-ttu-id="cdb2a-115">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="cdb2a-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="cdb2a-116">Вы можете создать его с помощью командлета New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="cdb2a-116">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="cdb2a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdb2a-117">-DefaultProfile</span></span>
<span data-ttu-id="cdb2a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cdb2a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdb2a-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cdb2a-119">-Name</span></span>
<span data-ttu-id="cdb2a-120">Указывает имя очереди.</span><span class="sxs-lookup"><span data-stu-id="cdb2a-120">Specifies a name for the queue.</span></span>

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

### <span data-ttu-id="cdb2a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdb2a-121">CommonParameters</span></span>
<span data-ttu-id="cdb2a-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cdb2a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdb2a-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdb2a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdb2a-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cdb2a-124">INPUTS</span></span>

### <span data-ttu-id="cdb2a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="cdb2a-125">System.String</span></span>

### <span data-ttu-id="cdb2a-126">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="cdb2a-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="cdb2a-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cdb2a-127">OUTPUTS</span></span>

### <span data-ttu-id="cdb2a-128">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="cdb2a-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="cdb2a-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="cdb2a-129">NOTES</span></span>

## <span data-ttu-id="cdb2a-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cdb2a-130">RELATED LINKS</span></span>

[<span data-ttu-id="cdb2a-131">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="cdb2a-131">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="cdb2a-132">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="cdb2a-132">Remove-AzStorageQueue</span></span>](./Remove-AzStorageQueue.md)


