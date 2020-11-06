---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: ''
schema: 2.0.0
ms.openlocfilehash: 552b1e638034cf0cec5825b742af4984b688cec3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556252"
---
# <span data-ttu-id="1bd03-101">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1bd03-101">Get-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="1bd03-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1bd03-102">SYNOPSIS</span></span>
<span data-ttu-id="1bd03-103">Возвращает политику и политики для сохраненного доступа в очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="1bd03-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="1bd03-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1bd03-104">SYNTAX</span></span>

```
Get-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="1bd03-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1bd03-105">DESCRIPTION</span></span>
<span data-ttu-id="1bd03-106">Командлет **Get-AzureStorageQueueStoredAccessPolicy** включает в себя политику и политики для хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="1bd03-106">The **Get-AzureStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="1bd03-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1bd03-107">EXAMPLES</span></span>

### <span data-ttu-id="1bd03-108">Пример 1: получение политики для сохраненного доступа в очереди</span><span class="sxs-lookup"><span data-stu-id="1bd03-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="1bd03-109">Эта команда получает политику доступа с именем Policy12 в очереди хранения с именем MyQueue.</span><span class="sxs-lookup"><span data-stu-id="1bd03-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="1bd03-110">Пример 2: получение всех сохраненных политик доступа в очереди</span><span class="sxs-lookup"><span data-stu-id="1bd03-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="1bd03-111">Эта команда получает все политики для сохраненных прав доступа в очереди с именем MyQueue.</span><span class="sxs-lookup"><span data-stu-id="1bd03-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="1bd03-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1bd03-112">PARAMETERS</span></span>

### <span data-ttu-id="1bd03-113">-Context</span><span class="sxs-lookup"><span data-stu-id="1bd03-113">-Context</span></span>
<span data-ttu-id="1bd03-114">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="1bd03-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="1bd03-115">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="1bd03-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="1bd03-116">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="1bd03-116">-Policy</span></span>
<span data-ttu-id="1bd03-117">Указывает политику сохраненного доступа, которая включает разрешения для маркера данной подписи общего доступа (SAS).</span><span class="sxs-lookup"><span data-stu-id="1bd03-117">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bd03-118">-Очередь</span><span class="sxs-lookup"><span data-stu-id="1bd03-118">-Queue</span></span>
<span data-ttu-id="1bd03-119">Указывает имя очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="1bd03-119">Specifies the Azure storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1bd03-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bd03-120">CommonParameters</span></span>
<span data-ttu-id="1bd03-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1bd03-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bd03-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bd03-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bd03-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1bd03-123">INPUTS</span></span>

## <span data-ttu-id="1bd03-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1bd03-124">OUTPUTS</span></span>

## <span data-ttu-id="1bd03-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="1bd03-125">NOTES</span></span>

## <span data-ttu-id="1bd03-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1bd03-126">RELATED LINKS</span></span>

[<span data-ttu-id="1bd03-127">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1bd03-127">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="1bd03-128">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1bd03-128">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="1bd03-129">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1bd03-129">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="1bd03-130">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="1bd03-130">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


