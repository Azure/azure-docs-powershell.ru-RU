---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 578eef176903576778325eb8610870040a515751
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731766"
---
# <span data-ttu-id="61102-101">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="61102-101">New-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="61102-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="61102-102">SYNOPSIS</span></span>
<span data-ttu-id="61102-103">Создание политики сохраненного доступа для очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="61102-103">Creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="61102-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="61102-104">SYNTAX</span></span>

```
New-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="61102-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61102-105">DESCRIPTION</span></span>
<span data-ttu-id="61102-106">Командлет **New-AzureStorageQueueStoredAccessPolicy** создает политику сохраненного доступа для очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="61102-106">The **New-AzureStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="61102-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="61102-107">EXAMPLES</span></span>

### <span data-ttu-id="61102-108">Пример 1: Создание политики сохраненных прав в очереди хранилища</span><span class="sxs-lookup"><span data-stu-id="61102-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="61102-109">Эта команда создает политику доступа с именем Policy01 в очереди хранения с именем MyQueue.</span><span class="sxs-lookup"><span data-stu-id="61102-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="61102-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="61102-110">PARAMETERS</span></span>

### <span data-ttu-id="61102-111">-Context</span><span class="sxs-lookup"><span data-stu-id="61102-111">-Context</span></span>
<span data-ttu-id="61102-112">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="61102-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="61102-113">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="61102-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="61102-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="61102-114">-ExpiryTime</span></span>
<span data-ttu-id="61102-115">Указывает время, в течение которого политика хранения сохраненных прав становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="61102-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="61102-116">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="61102-116">-Permission</span></span>
<span data-ttu-id="61102-117">Задает уровень публичного доступа к этой очереди хранилища.</span><span class="sxs-lookup"><span data-stu-id="61102-117">Specifies the level of public access to this storage queue.</span></span>

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

### <span data-ttu-id="61102-118">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="61102-118">-Policy</span></span>
<span data-ttu-id="61102-119">Указывает политику сохраненного доступа, которая включает разрешения для этого маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="61102-119">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="61102-120">-Очередь</span><span class="sxs-lookup"><span data-stu-id="61102-120">-Queue</span></span>
<span data-ttu-id="61102-121">Указывает имя очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="61102-121">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="61102-122">-StartTime</span><span class="sxs-lookup"><span data-stu-id="61102-122">-StartTime</span></span>
<span data-ttu-id="61102-123">Указывает время вступления в силу политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="61102-123">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="61102-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61102-124">CommonParameters</span></span>
<span data-ttu-id="61102-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="61102-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61102-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61102-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61102-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="61102-127">INPUTS</span></span>

## <span data-ttu-id="61102-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="61102-128">OUTPUTS</span></span>

## <span data-ttu-id="61102-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="61102-129">NOTES</span></span>

## <span data-ttu-id="61102-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61102-130">RELATED LINKS</span></span>

[<span data-ttu-id="61102-131">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="61102-131">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="61102-132">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="61102-132">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="61102-133">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="61102-133">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="61102-134">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="61102-134">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)


