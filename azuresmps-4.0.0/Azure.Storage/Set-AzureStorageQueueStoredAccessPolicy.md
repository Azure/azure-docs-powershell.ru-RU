---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: ''
schema: 2.0.0
ms.openlocfilehash: b273dbec3fda421574c8866a10eda0a8098513ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556363"
---
# <span data-ttu-id="4e5d4-101">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4e5d4-101">Set-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="4e5d4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e5d4-102">SYNOPSIS</span></span>
<span data-ttu-id="4e5d4-103">Задает политику сохранения для доступа для очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4e5d4-103">Sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="4e5d4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e5d4-104">SYNTAX</span></span>

```
Set-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e5d4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e5d4-105">DESCRIPTION</span></span>
<span data-ttu-id="4e5d4-106">Командлет **Set-AzureStorageQueueStoredAccessPolicy** задает политику сохраненного доступа для очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4e5d4-106">The **Set-AzureStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="4e5d4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e5d4-107">EXAMPLES</span></span>

### <span data-ttu-id="4e5d4-108">Пример 1: Настройка политики сохраненных прав доступа в очереди</span><span class="sxs-lookup"><span data-stu-id="4e5d4-108">Example 1: Set a stored access policy in the queue</span></span>
```
PS C:\> Set-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07"
```

<span data-ttu-id="4e5d4-109">Эта команда задает политику доступа с именем Policy07 для очереди хранения с именем MyQueue.</span><span class="sxs-lookup"><span data-stu-id="4e5d4-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="4e5d4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e5d4-110">PARAMETERS</span></span>

### <span data-ttu-id="4e5d4-111">-Context</span><span class="sxs-lookup"><span data-stu-id="4e5d4-111">-Context</span></span>
<span data-ttu-id="4e5d4-112">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4e5d4-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4e5d4-113">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="4e5d4-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4e5d4-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="4e5d4-114">-ExpiryTime</span></span>
<span data-ttu-id="4e5d4-115">Указывает время, в течение которого политика хранения сохраненных прав становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="4e5d4-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="4e5d4-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="4e5d4-116">-NoExpiryTime</span></span>
<span data-ttu-id="4e5d4-117">Указывает на то, что политика доступа не содержит дату окончания срока действия.</span><span class="sxs-lookup"><span data-stu-id="4e5d4-117">Indicates that the access policy has no expiration date.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e5d4-118">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="4e5d4-118">-NoStartTime</span></span>
<span data-ttu-id="4e5d4-119">Указывает на то, что этот командлет задает время запуска, которое должно быть $Null.</span><span class="sxs-lookup"><span data-stu-id="4e5d4-119">Indicates that this cmdlet sets the start time to be $Null.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e5d4-120">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="4e5d4-120">-Permission</span></span>
<span data-ttu-id="4e5d4-121">Задает уровень публичного доступа к этой очереди хранилища.</span><span class="sxs-lookup"><span data-stu-id="4e5d4-121">Specifies the level of public access to this storage queue.</span></span>

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

### <span data-ttu-id="4e5d4-122">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="4e5d4-122">-Policy</span></span>
<span data-ttu-id="4e5d4-123">Указывает политику сохраненного доступа, которая включает разрешения для этого маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="4e5d4-123">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="4e5d4-124">-Очередь</span><span class="sxs-lookup"><span data-stu-id="4e5d4-124">-Queue</span></span>
<span data-ttu-id="4e5d4-125">Указывает имя очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4e5d4-125">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="4e5d4-126">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4e5d4-126">-StartTime</span></span>
<span data-ttu-id="4e5d4-127">Указывает время вступления в силу политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="4e5d4-127">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="4e5d4-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e5d4-128">-Confirm</span></span>
<span data-ttu-id="4e5d4-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4e5d4-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e5d4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e5d4-130">-WhatIf</span></span>
<span data-ttu-id="4e5d4-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4e5d4-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4e5d4-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4e5d4-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e5d4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e5d4-133">CommonParameters</span></span>
<span data-ttu-id="4e5d4-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e5d4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e5d4-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e5d4-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e5d4-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e5d4-136">INPUTS</span></span>

## <span data-ttu-id="4e5d4-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e5d4-137">OUTPUTS</span></span>

## <span data-ttu-id="4e5d4-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e5d4-138">NOTES</span></span>

## <span data-ttu-id="4e5d4-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e5d4-139">RELATED LINKS</span></span>

[<span data-ttu-id="4e5d4-140">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4e5d4-140">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="4e5d4-141">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4e5d4-141">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="4e5d4-142">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4e5d4-142">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)
