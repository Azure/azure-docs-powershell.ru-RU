---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: b1e7f305b571c5b40c12dacadf520f9637e076f3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241872"
---
# <span data-ttu-id="ac39d-101">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ac39d-101">Get-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="ac39d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac39d-102">SYNOPSIS</span></span>
<span data-ttu-id="ac39d-103">Получает хранимую политику доступа или политики для очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="ac39d-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="ac39d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ac39d-104">SYNTAX</span></span>

```
Get-AzStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac39d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac39d-105">DESCRIPTION</span></span>
<span data-ttu-id="ac39d-106">С **его** учетом можно получить список политик доступа для очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="ac39d-106">The **Get-AzStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="ac39d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ac39d-107">EXAMPLES</span></span>

### <span data-ttu-id="ac39d-108">Пример 1. Получить хранимую политику доступа в очереди</span><span class="sxs-lookup"><span data-stu-id="ac39d-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="ac39d-109">Эта команда получает политику доступа "Политика12" в очереди хранилища MyQueue.</span><span class="sxs-lookup"><span data-stu-id="ac39d-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="ac39d-110">Пример 2. Все хранимые политики доступа в очереди</span><span class="sxs-lookup"><span data-stu-id="ac39d-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="ac39d-111">Эта команда получает все хранимые политики доступа в очереди MyQueue.</span><span class="sxs-lookup"><span data-stu-id="ac39d-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="ac39d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac39d-112">PARAMETERS</span></span>

### <span data-ttu-id="ac39d-113">-Контекст</span><span class="sxs-lookup"><span data-stu-id="ac39d-113">-Context</span></span>
<span data-ttu-id="ac39d-114">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="ac39d-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="ac39d-115">Для получения контекста хранилища используйте New-AzStorageContext управления.</span><span class="sxs-lookup"><span data-stu-id="ac39d-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ac39d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac39d-116">-DefaultProfile</span></span>
<span data-ttu-id="ac39d-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ac39d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac39d-118">-Политика</span><span class="sxs-lookup"><span data-stu-id="ac39d-118">-Policy</span></span>
<span data-ttu-id="ac39d-119">Определяет хранимую политику доступа, которая включает разрешения для маркера подписи общего доступа (SAS).</span><span class="sxs-lookup"><span data-stu-id="ac39d-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="ac39d-120">-Queue</span><span class="sxs-lookup"><span data-stu-id="ac39d-120">-Queue</span></span>
<span data-ttu-id="ac39d-121">Указывает имя очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="ac39d-121">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="ac39d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac39d-122">CommonParameters</span></span>
<span data-ttu-id="ac39d-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac39d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac39d-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac39d-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac39d-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ac39d-125">INPUTS</span></span>

### <span data-ttu-id="ac39d-126">System.String</span><span class="sxs-lookup"><span data-stu-id="ac39d-126">System.String</span></span>

### <span data-ttu-id="ac39d-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ac39d-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ac39d-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ac39d-128">OUTPUTS</span></span>

### <span data-ttu-id="ac39d-129">Microsoft.Azure.Storage.Queue.SharedAccessQueuePolicy</span><span class="sxs-lookup"><span data-stu-id="ac39d-129">Microsoft.Azure.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="ac39d-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ac39d-130">NOTES</span></span>

## <span data-ttu-id="ac39d-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ac39d-131">RELATED LINKS</span></span>

[<span data-ttu-id="ac39d-132">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ac39d-132">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="ac39d-133">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ac39d-133">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="ac39d-134">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ac39d-134">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="ac39d-135">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ac39d-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


