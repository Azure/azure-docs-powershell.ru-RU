---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
ms.openlocfilehash: 1c3f258f4aecbeb492e0e60e274c5e702ae1a3f2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517081"
---
# <span data-ttu-id="a4151-101">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="a4151-101">New-AzStorageQueue</span></span>

## <span data-ttu-id="a4151-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4151-102">SYNOPSIS</span></span>
<span data-ttu-id="a4151-103">Создает очередь хранилища.</span><span class="sxs-lookup"><span data-stu-id="a4151-103">Creates a storage queue.</span></span>

## <span data-ttu-id="a4151-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a4151-104">SYNTAX</span></span>

```
New-AzStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4151-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4151-105">DESCRIPTION</span></span>
<span data-ttu-id="a4151-106">С **его использованием** в Azure создается очередь хранилища.</span><span class="sxs-lookup"><span data-stu-id="a4151-106">The **New-AzStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="a4151-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a4151-107">EXAMPLES</span></span>

### <span data-ttu-id="a4151-108">Пример 1. Создание очереди хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="a4151-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzStorageQueue -Name "queueabc"
```

<span data-ttu-id="a4151-109">В этом примере создается очередь хранилища с именем queueabc.</span><span class="sxs-lookup"><span data-stu-id="a4151-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="a4151-110">Пример 2. Создание нескольких очередей хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="a4151-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzStorageQueue
```

<span data-ttu-id="a4151-111">В этом примере создается несколько очередей хранилища.</span><span class="sxs-lookup"><span data-stu-id="a4151-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="a4151-112">Для этого используется метод разделения класса .NET String, который передает имена в конвейере.</span><span class="sxs-lookup"><span data-stu-id="a4151-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="a4151-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4151-113">PARAMETERS</span></span>

### <span data-ttu-id="a4151-114">-Контекст</span><span class="sxs-lookup"><span data-stu-id="a4151-114">-Context</span></span>
<span data-ttu-id="a4151-115">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="a4151-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="a4151-116">Его можно создать с помощью New-AzStorageContext управления.</span><span class="sxs-lookup"><span data-stu-id="a4151-116">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a4151-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4151-117">-DefaultProfile</span></span>
<span data-ttu-id="a4151-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a4151-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4151-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a4151-119">-Name</span></span>
<span data-ttu-id="a4151-120">Указывает имя очереди.</span><span class="sxs-lookup"><span data-stu-id="a4151-120">Specifies a name for the queue.</span></span>

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

### <span data-ttu-id="a4151-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4151-121">CommonParameters</span></span>
<span data-ttu-id="a4151-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4151-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4151-123">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4151-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4151-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a4151-124">INPUTS</span></span>

### <span data-ttu-id="a4151-125">System.String</span><span class="sxs-lookup"><span data-stu-id="a4151-125">System.String</span></span>

### <span data-ttu-id="a4151-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a4151-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a4151-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a4151-127">OUTPUTS</span></span>

### <span data-ttu-id="a4151-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="a4151-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="a4151-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a4151-129">NOTES</span></span>

## <span data-ttu-id="a4151-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4151-130">RELATED LINKS</span></span>

[<span data-ttu-id="a4151-131">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="a4151-131">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="a4151-132">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="a4151-132">Remove-AzStorageQueue</span></span>](./Remove-AzStorageQueue.md)


