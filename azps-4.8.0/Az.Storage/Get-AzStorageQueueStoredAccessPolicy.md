---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: b1e7f305b571c5b40c12dacadf520f9637e076f3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078601"
---
# <span data-ttu-id="f1ea3-101">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f1ea3-101">Get-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="f1ea3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f1ea3-102">SYNOPSIS</span></span>
<span data-ttu-id="f1ea3-103">Возвращает политику и политики для сохраненного доступа в очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="f1ea3-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="f1ea3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f1ea3-104">SYNTAX</span></span>

```
Get-AzStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1ea3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1ea3-105">DESCRIPTION</span></span>
<span data-ttu-id="f1ea3-106">Командлет **Get-AzStorageQueueStoredAccessPolicy** включает в себя политику и политики для хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="f1ea3-106">The **Get-AzStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="f1ea3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f1ea3-107">EXAMPLES</span></span>

### <span data-ttu-id="f1ea3-108">Пример 1: получение политики для сохраненного доступа в очереди</span><span class="sxs-lookup"><span data-stu-id="f1ea3-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="f1ea3-109">Эта команда получает политику доступа с именем Policy12 в очереди хранения с именем MyQueue.</span><span class="sxs-lookup"><span data-stu-id="f1ea3-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="f1ea3-110">Пример 2: получение всех сохраненных политик доступа в очереди</span><span class="sxs-lookup"><span data-stu-id="f1ea3-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="f1ea3-111">Эта команда получает все политики для сохраненных прав доступа в очереди с именем MyQueue.</span><span class="sxs-lookup"><span data-stu-id="f1ea3-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="f1ea3-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f1ea3-112">PARAMETERS</span></span>

### <span data-ttu-id="f1ea3-113">-Context</span><span class="sxs-lookup"><span data-stu-id="f1ea3-113">-Context</span></span>
<span data-ttu-id="f1ea3-114">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="f1ea3-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="f1ea3-115">Чтобы получить контекст хранилища, используйте командлет New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="f1ea3-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f1ea3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1ea3-116">-DefaultProfile</span></span>
<span data-ttu-id="f1ea3-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f1ea3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1ea3-118">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="f1ea3-118">-Policy</span></span>
<span data-ttu-id="f1ea3-119">Указывает политику сохраненного доступа, которая включает разрешения для маркера данной подписи общего доступа (SAS).</span><span class="sxs-lookup"><span data-stu-id="f1ea3-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1ea3-120">-Очередь</span><span class="sxs-lookup"><span data-stu-id="f1ea3-120">-Queue</span></span>
<span data-ttu-id="f1ea3-121">Указывает имя очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="f1ea3-121">Specifies the Azure storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1ea3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1ea3-122">CommonParameters</span></span>
<span data-ttu-id="f1ea3-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f1ea3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1ea3-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1ea3-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1ea3-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f1ea3-125">INPUTS</span></span>

### <span data-ttu-id="f1ea3-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f1ea3-126">System.String</span></span>

### <span data-ttu-id="f1ea3-127">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f1ea3-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f1ea3-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1ea3-128">OUTPUTS</span></span>

### <span data-ttu-id="f1ea3-129">Microsoft. Azure. Storage. Queue. SharedAccessQueuePolicy</span><span class="sxs-lookup"><span data-stu-id="f1ea3-129">Microsoft.Azure.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="f1ea3-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="f1ea3-130">NOTES</span></span>

## <span data-ttu-id="f1ea3-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1ea3-131">RELATED LINKS</span></span>

[<span data-ttu-id="f1ea3-132">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f1ea3-132">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="f1ea3-133">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f1ea3-133">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="f1ea3-134">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f1ea3-134">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="f1ea3-135">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f1ea3-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

