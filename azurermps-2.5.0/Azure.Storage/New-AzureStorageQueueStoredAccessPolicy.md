---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 054a5d979a13f5592f062f729e4c8c393a35134a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914274"
---
# <span data-ttu-id="e424b-101">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e424b-101">New-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="e424b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e424b-102">SYNOPSIS</span></span>
<span data-ttu-id="e424b-103">Создание политики сохраненного доступа для очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="e424b-103">Creates a stored access policy for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e424b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e424b-104">SYNTAX</span></span>

```
New-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e424b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e424b-105">DESCRIPTION</span></span>
<span data-ttu-id="e424b-106">Командлет **New-AzureStorageQueueStoredAccessPolicy** создает политику сохраненного доступа для очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="e424b-106">The **New-AzureStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="e424b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e424b-107">EXAMPLES</span></span>

### <span data-ttu-id="e424b-108">Пример 1: Создание политики сохраненных прав в очереди хранилища</span><span class="sxs-lookup"><span data-stu-id="e424b-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="e424b-109">Эта команда создает политику доступа с именем Policy01 в очереди хранения с именем MyQueue.</span><span class="sxs-lookup"><span data-stu-id="e424b-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="e424b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e424b-110">PARAMETERS</span></span>

### <span data-ttu-id="e424b-111">-Context</span><span class="sxs-lookup"><span data-stu-id="e424b-111">-Context</span></span>
<span data-ttu-id="e424b-112">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="e424b-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e424b-113">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="e424b-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e424b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e424b-114">-DefaultProfile</span></span>
<span data-ttu-id="e424b-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e424b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e424b-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="e424b-116">-ExpiryTime</span></span>
<span data-ttu-id="e424b-117">Указывает время, в течение которого политика хранения сохраненных прав становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="e424b-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="e424b-118">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="e424b-118">-Permission</span></span>
<span data-ttu-id="e424b-119">Определяет разрешения в политике сохранения доступа для доступа к очереди хранилища.</span><span class="sxs-lookup"><span data-stu-id="e424b-119">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="e424b-120">Важно отметить, что это строка, например `rwd` (для чтения, записи и удаления).</span><span class="sxs-lookup"><span data-stu-id="e424b-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="e424b-121">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="e424b-121">-Policy</span></span>
<span data-ttu-id="e424b-122">Задает имя для политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="e424b-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="e424b-123">-Очередь</span><span class="sxs-lookup"><span data-stu-id="e424b-123">-Queue</span></span>
<span data-ttu-id="e424b-124">Указывает имя очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="e424b-124">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="e424b-125">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e424b-125">-StartTime</span></span>
<span data-ttu-id="e424b-126">Указывает время вступления в силу политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="e424b-126">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="e424b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e424b-127">CommonParameters</span></span>
<span data-ttu-id="e424b-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e424b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e424b-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e424b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e424b-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e424b-130">INPUTS</span></span>

### <span data-ttu-id="e424b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="e424b-131">System.String</span></span>

### <span data-ttu-id="e424b-132">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e424b-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e424b-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e424b-133">OUTPUTS</span></span>

### <span data-ttu-id="e424b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e424b-134">System.String</span></span>

## <span data-ttu-id="e424b-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="e424b-135">NOTES</span></span>

## <span data-ttu-id="e424b-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e424b-136">RELATED LINKS</span></span>

[<span data-ttu-id="e424b-137">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e424b-137">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="e424b-138">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="e424b-138">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="e424b-139">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e424b-139">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="e424b-140">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e424b-140">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)


