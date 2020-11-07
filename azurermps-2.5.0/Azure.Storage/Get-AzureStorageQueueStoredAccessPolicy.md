---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 9ef4be8331c1de38789d25903db9e98f4e2d8cd1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913515"
---
# <span data-ttu-id="c4c4e-101">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c4c4e-101">Get-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="c4c4e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c4c4e-102">SYNOPSIS</span></span>
<span data-ttu-id="c4c4e-103">Возвращает политику и политики для сохраненного доступа в очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c4c4e-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4c4e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c4c4e-104">SYNTAX</span></span>

```
Get-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4c4e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4c4e-105">DESCRIPTION</span></span>
<span data-ttu-id="c4c4e-106">Командлет **Get-AzureStorageQueueStoredAccessPolicy** включает в себя политику и политики для хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c4c4e-106">The **Get-AzureStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="c4c4e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c4c4e-107">EXAMPLES</span></span>

### <span data-ttu-id="c4c4e-108">Пример 1: получение политики для сохраненного доступа в очереди</span><span class="sxs-lookup"><span data-stu-id="c4c4e-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="c4c4e-109">Эта команда получает политику доступа с именем Policy12 в очереди хранения с именем MyQueue.</span><span class="sxs-lookup"><span data-stu-id="c4c4e-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="c4c4e-110">Пример 2: получение всех сохраненных политик доступа в очереди</span><span class="sxs-lookup"><span data-stu-id="c4c4e-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="c4c4e-111">Эта команда получает все политики для сохраненных прав доступа в очереди с именем MyQueue.</span><span class="sxs-lookup"><span data-stu-id="c4c4e-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="c4c4e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c4c4e-112">PARAMETERS</span></span>

### <span data-ttu-id="c4c4e-113">-Context</span><span class="sxs-lookup"><span data-stu-id="c4c4e-113">-Context</span></span>
<span data-ttu-id="c4c4e-114">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c4c4e-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="c4c4e-115">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="c4c4e-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c4c4e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4c4e-116">-DefaultProfile</span></span>
<span data-ttu-id="c4c4e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c4c4e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4c4e-118">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="c4c4e-118">-Policy</span></span>
<span data-ttu-id="c4c4e-119">Указывает политику сохраненного доступа, которая включает разрешения для маркера данной подписи общего доступа (SAS).</span><span class="sxs-lookup"><span data-stu-id="c4c4e-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="c4c4e-120">-Очередь</span><span class="sxs-lookup"><span data-stu-id="c4c4e-120">-Queue</span></span>
<span data-ttu-id="c4c4e-121">Указывает имя очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c4c4e-121">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="c4c4e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4c4e-122">CommonParameters</span></span>
<span data-ttu-id="c4c4e-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c4c4e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4c4e-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4c4e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4c4e-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c4c4e-125">INPUTS</span></span>

### <span data-ttu-id="c4c4e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c4c4e-126">System.String</span></span>

### <span data-ttu-id="c4c4e-127">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c4c4e-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c4c4e-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4c4e-128">OUTPUTS</span></span>

### <span data-ttu-id="c4c4e-129">Microsoft. WindowsAzure. Storage. Queue. SharedAccessQueuePolicy</span><span class="sxs-lookup"><span data-stu-id="c4c4e-129">Microsoft.WindowsAzure.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="c4c4e-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="c4c4e-130">NOTES</span></span>

## <span data-ttu-id="c4c4e-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c4c4e-131">RELATED LINKS</span></span>

[<span data-ttu-id="c4c4e-132">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c4c4e-132">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="c4c4e-133">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c4c4e-133">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="c4c4e-134">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c4c4e-134">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="c4c4e-135">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="c4c4e-135">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


