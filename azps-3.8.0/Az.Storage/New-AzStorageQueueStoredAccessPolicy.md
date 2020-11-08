---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 65afd4039fb772d1ecf522645fe41154dae42981
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073460"
---
# <span data-ttu-id="0449e-101">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0449e-101">New-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="0449e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0449e-102">SYNOPSIS</span></span>
<span data-ttu-id="0449e-103">Создание политики сохраненного доступа для очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="0449e-103">Creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="0449e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0449e-104">SYNTAX</span></span>

```
New-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0449e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0449e-105">DESCRIPTION</span></span>
<span data-ttu-id="0449e-106">Командлет **New-AzStorageQueueStoredAccessPolicy** создает политику сохраненного доступа для очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="0449e-106">The **New-AzStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="0449e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0449e-107">EXAMPLES</span></span>

### <span data-ttu-id="0449e-108">Пример 1: Создание политики сохраненных прав в очереди хранилища</span><span class="sxs-lookup"><span data-stu-id="0449e-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="0449e-109">Эта команда создает политику доступа с именем Policy01 в очереди хранения с именем MyQueue.</span><span class="sxs-lookup"><span data-stu-id="0449e-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="0449e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0449e-110">PARAMETERS</span></span>

### <span data-ttu-id="0449e-111">-Context</span><span class="sxs-lookup"><span data-stu-id="0449e-111">-Context</span></span>
<span data-ttu-id="0449e-112">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="0449e-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="0449e-113">Чтобы получить контекст хранилища, используйте командлет New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="0449e-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="0449e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0449e-114">-DefaultProfile</span></span>
<span data-ttu-id="0449e-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0449e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0449e-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="0449e-116">-ExpiryTime</span></span>
<span data-ttu-id="0449e-117">Указывает время, в течение которого политика хранения сохраненных прав становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="0449e-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0449e-118">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="0449e-118">-Permission</span></span>
<span data-ttu-id="0449e-119">Определяет разрешения в политике сохранения доступа для доступа к очереди хранилища.</span><span class="sxs-lookup"><span data-stu-id="0449e-119">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="0449e-120">Важно отметить, что это строка, например `rwd` (для чтения, записи и удаления).</span><span class="sxs-lookup"><span data-stu-id="0449e-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0449e-121">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="0449e-121">-Policy</span></span>
<span data-ttu-id="0449e-122">Задает имя для политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="0449e-122">Specifies a name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0449e-123">-Очередь</span><span class="sxs-lookup"><span data-stu-id="0449e-123">-Queue</span></span>
<span data-ttu-id="0449e-124">Указывает имя очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="0449e-124">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="0449e-125">-StartTime</span><span class="sxs-lookup"><span data-stu-id="0449e-125">-StartTime</span></span>
<span data-ttu-id="0449e-126">Указывает время вступления в силу политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="0449e-126">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0449e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0449e-127">CommonParameters</span></span>
<span data-ttu-id="0449e-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0449e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0449e-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0449e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0449e-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0449e-130">INPUTS</span></span>

### <span data-ttu-id="0449e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="0449e-131">System.String</span></span>

### <span data-ttu-id="0449e-132">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0449e-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0449e-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0449e-133">OUTPUTS</span></span>

### <span data-ttu-id="0449e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0449e-134">System.String</span></span>

## <span data-ttu-id="0449e-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="0449e-135">NOTES</span></span>

## <span data-ttu-id="0449e-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0449e-136">RELATED LINKS</span></span>

[<span data-ttu-id="0449e-137">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0449e-137">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="0449e-138">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="0449e-138">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="0449e-139">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0449e-139">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="0449e-140">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0449e-140">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)


