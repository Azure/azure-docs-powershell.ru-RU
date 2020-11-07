---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueueStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 78815aaa29c46e455f24ce0daac167b2806b6c20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733417"
---
# <span data-ttu-id="a47ed-101">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a47ed-101">Get-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="a47ed-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a47ed-102">SYNOPSIS</span></span>
<span data-ttu-id="a47ed-103">Возвращает политику и политики для сохраненного доступа в очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="a47ed-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a47ed-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a47ed-104">SYNTAX</span></span>

```
Get-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="a47ed-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a47ed-105">DESCRIPTION</span></span>
<span data-ttu-id="a47ed-106">Командлет **Get-AzureStorageQueueStoredAccessPolicy** включает в себя политику и политики для хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="a47ed-106">The **Get-AzureStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="a47ed-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a47ed-107">EXAMPLES</span></span>

### <span data-ttu-id="a47ed-108">Пример 1: получение политики для сохраненного доступа в очереди</span><span class="sxs-lookup"><span data-stu-id="a47ed-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="a47ed-109">Эта команда получает политику доступа с именем Policy12 в очереди хранения с именем MyQueue.</span><span class="sxs-lookup"><span data-stu-id="a47ed-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="a47ed-110">Пример 2: получение всех сохраненных политик доступа в очереди</span><span class="sxs-lookup"><span data-stu-id="a47ed-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="a47ed-111">Эта команда получает все политики для сохраненных прав доступа в очереди с именем MyQueue.</span><span class="sxs-lookup"><span data-stu-id="a47ed-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="a47ed-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a47ed-112">PARAMETERS</span></span>

### <span data-ttu-id="a47ed-113">-Context</span><span class="sxs-lookup"><span data-stu-id="a47ed-113">-Context</span></span>
<span data-ttu-id="a47ed-114">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="a47ed-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="a47ed-115">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="a47ed-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a47ed-116">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="a47ed-116">-Policy</span></span>
<span data-ttu-id="a47ed-117">Указывает политику сохраненного доступа, которая включает разрешения для маркера данной подписи общего доступа (SAS).</span><span class="sxs-lookup"><span data-stu-id="a47ed-117">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="a47ed-118">-Очередь</span><span class="sxs-lookup"><span data-stu-id="a47ed-118">-Queue</span></span>
<span data-ttu-id="a47ed-119">Указывает имя очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="a47ed-119">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="a47ed-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a47ed-120">CommonParameters</span></span>
<span data-ttu-id="a47ed-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a47ed-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a47ed-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a47ed-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a47ed-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a47ed-123">INPUTS</span></span>

### <span data-ttu-id="a47ed-124">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a47ed-124">IStorageContext</span></span>

<span data-ttu-id="a47ed-125">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="a47ed-125">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="a47ed-126">Подстрок</span><span class="sxs-lookup"><span data-stu-id="a47ed-126">String</span></span>

<span data-ttu-id="a47ed-127">Параметр "Queue" принимает значение типа String из конвейера</span><span class="sxs-lookup"><span data-stu-id="a47ed-127">Parameter 'Queue' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="a47ed-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a47ed-128">OUTPUTS</span></span>

### <span data-ttu-id="a47ed-129">Microsoft. WindowsAzure. Storage. Queue. SharedAccessQueuePolicy</span><span class="sxs-lookup"><span data-stu-id="a47ed-129">Microsoft.WindowsAzure.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="a47ed-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="a47ed-130">NOTES</span></span>

## <span data-ttu-id="a47ed-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a47ed-131">RELATED LINKS</span></span>

[<span data-ttu-id="a47ed-132">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a47ed-132">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="a47ed-133">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a47ed-133">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="a47ed-134">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a47ed-134">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="a47ed-135">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="a47ed-135">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


