---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: ef54976ed06eb47da803470a3d4c163a8b294743
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570172"
---
# <span data-ttu-id="bc102-101">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bc102-101">New-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="bc102-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bc102-102">SYNOPSIS</span></span>
<span data-ttu-id="bc102-103">Создание политики сохраненного доступа для очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="bc102-103">Creates a stored access policy for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc102-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bc102-104">SYNTAX</span></span>

```
New-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="bc102-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc102-105">DESCRIPTION</span></span>
<span data-ttu-id="bc102-106">Командлет **New-AzureStorageQueueStoredAccessPolicy** создает политику сохраненного доступа для очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="bc102-106">The **New-AzureStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="bc102-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bc102-107">EXAMPLES</span></span>

### <span data-ttu-id="bc102-108">Пример 1: Создание политики сохраненных прав в очереди хранилища</span><span class="sxs-lookup"><span data-stu-id="bc102-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="bc102-109">Эта команда создает политику доступа с именем Policy01 в очереди хранения с именем MyQueue.</span><span class="sxs-lookup"><span data-stu-id="bc102-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="bc102-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bc102-110">PARAMETERS</span></span>

### <span data-ttu-id="bc102-111">-Context</span><span class="sxs-lookup"><span data-stu-id="bc102-111">-Context</span></span>
<span data-ttu-id="bc102-112">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="bc102-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="bc102-113">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="bc102-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="bc102-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="bc102-114">-ExpiryTime</span></span>
<span data-ttu-id="bc102-115">Указывает время, в течение которого политика хранения сохраненных прав становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="bc102-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc102-116">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="bc102-116">-Permission</span></span>
<span data-ttu-id="bc102-117">Определяет разрешения в политике сохранения доступа для доступа к очереди хранилища.</span><span class="sxs-lookup"><span data-stu-id="bc102-117">Specifies permissions in the stored access policy to access the storage queue.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc102-118">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="bc102-118">-Policy</span></span>
<span data-ttu-id="bc102-119">Задает имя для политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="bc102-119">Specifies a name for the stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc102-120">-Очередь</span><span class="sxs-lookup"><span data-stu-id="bc102-120">-Queue</span></span>
<span data-ttu-id="bc102-121">Указывает имя очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="bc102-121">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="bc102-122">-StartTime</span><span class="sxs-lookup"><span data-stu-id="bc102-122">-StartTime</span></span>
<span data-ttu-id="bc102-123">Указывает время вступления в силу политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="bc102-123">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc102-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc102-124">CommonParameters</span></span>
<span data-ttu-id="bc102-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bc102-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc102-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc102-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc102-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bc102-127">INPUTS</span></span>

### <span data-ttu-id="bc102-128">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="bc102-128">IStorageContext</span></span>

<span data-ttu-id="bc102-129">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="bc102-129">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="bc102-130">Подстрок</span><span class="sxs-lookup"><span data-stu-id="bc102-130">String</span></span>

<span data-ttu-id="bc102-131">Параметр "Queue" принимает значение типа String из конвейера</span><span class="sxs-lookup"><span data-stu-id="bc102-131">Parameter 'Queue' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="bc102-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc102-132">OUTPUTS</span></span>

### <span data-ttu-id="bc102-133">System. String</span><span class="sxs-lookup"><span data-stu-id="bc102-133">System.String</span></span>

## <span data-ttu-id="bc102-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="bc102-134">NOTES</span></span>

## <span data-ttu-id="bc102-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bc102-135">RELATED LINKS</span></span>

[<span data-ttu-id="bc102-136">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bc102-136">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="bc102-137">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="bc102-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="bc102-138">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bc102-138">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="bc102-139">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bc102-139">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)


