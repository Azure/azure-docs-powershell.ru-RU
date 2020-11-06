---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageQueueStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 69ec2307dfdf8525f892720281079c58c1e1bd55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568374"
---
# <span data-ttu-id="c8d7d-101">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c8d7d-101">Set-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="c8d7d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c8d7d-102">SYNOPSIS</span></span>
<span data-ttu-id="c8d7d-103">Задает политику сохранения для доступа для очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c8d7d-103">Sets a stored access policy for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8d7d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c8d7d-104">SYNTAX</span></span>

```
Set-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8d7d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8d7d-105">DESCRIPTION</span></span>
<span data-ttu-id="c8d7d-106">Командлет **Set-AzureStorageQueueStoredAccessPolicy** задает политику сохраненного доступа для очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c8d7d-106">The **Set-AzureStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="c8d7d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c8d7d-107">EXAMPLES</span></span>

### <span data-ttu-id="c8d7d-108">Пример 1: Настройка политики доступа в очереди с полным разрешением</span><span class="sxs-lookup"><span data-stu-id="c8d7d-108">Example 1: Set a stored access policy in the queue with full permission</span></span>
```
PS C:\> Set-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07" -Permission arup
```

<span data-ttu-id="c8d7d-109">Эта команда задает политику доступа с именем Policy07 для очереди хранения с именем MyQueue.</span><span class="sxs-lookup"><span data-stu-id="c8d7d-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="c8d7d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c8d7d-110">PARAMETERS</span></span>

### <span data-ttu-id="c8d7d-111">-Context</span><span class="sxs-lookup"><span data-stu-id="c8d7d-111">-Context</span></span>
<span data-ttu-id="c8d7d-112">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c8d7d-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c8d7d-113">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="c8d7d-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c8d7d-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="c8d7d-114">-ExpiryTime</span></span>
<span data-ttu-id="c8d7d-115">Указывает время, в течение которого политика хранения сохраненных прав становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="c8d7d-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="c8d7d-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="c8d7d-116">-NoExpiryTime</span></span>
<span data-ttu-id="c8d7d-117">Указывает на то, что политика доступа не содержит дату окончания срока действия.</span><span class="sxs-lookup"><span data-stu-id="c8d7d-117">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="c8d7d-118">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="c8d7d-118">-NoStartTime</span></span>
<span data-ttu-id="c8d7d-119">Указывает на то, что этот командлет задает время запуска, которое должно быть $Null.</span><span class="sxs-lookup"><span data-stu-id="c8d7d-119">Indicates that this cmdlet sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="c8d7d-120">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="c8d7d-120">-Permission</span></span>
<span data-ttu-id="c8d7d-121">Определяет разрешения в политике сохранения доступа для доступа к очереди хранилища.</span><span class="sxs-lookup"><span data-stu-id="c8d7d-121">Specifies permissions in the stored access policy to access the storage queue.</span></span>

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

### <span data-ttu-id="c8d7d-122">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="c8d7d-122">-Policy</span></span>
<span data-ttu-id="c8d7d-123">Задает имя для политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="c8d7d-123">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="c8d7d-124">-Очередь</span><span class="sxs-lookup"><span data-stu-id="c8d7d-124">-Queue</span></span>
<span data-ttu-id="c8d7d-125">Указывает имя очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c8d7d-125">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="c8d7d-126">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c8d7d-126">-StartTime</span></span>
<span data-ttu-id="c8d7d-127">Указывает время вступления в силу политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="c8d7d-127">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="c8d7d-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c8d7d-128">-Confirm</span></span>
<span data-ttu-id="c8d7d-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c8d7d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8d7d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8d7d-130">-WhatIf</span></span>
<span data-ttu-id="c8d7d-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c8d7d-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c8d7d-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c8d7d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8d7d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8d7d-133">CommonParameters</span></span>
<span data-ttu-id="c8d7d-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c8d7d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8d7d-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8d7d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8d7d-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c8d7d-136">INPUTS</span></span>

### <span data-ttu-id="c8d7d-137">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c8d7d-137">IStorageContext</span></span>

<span data-ttu-id="c8d7d-138">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="c8d7d-138">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="c8d7d-139">Подстрок</span><span class="sxs-lookup"><span data-stu-id="c8d7d-139">String</span></span>

<span data-ttu-id="c8d7d-140">Параметр "Queue" принимает значение типа String из конвейера</span><span class="sxs-lookup"><span data-stu-id="c8d7d-140">Parameter 'Queue' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="c8d7d-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8d7d-141">OUTPUTS</span></span>

### <span data-ttu-id="c8d7d-142">System. String</span><span class="sxs-lookup"><span data-stu-id="c8d7d-142">System.String</span></span>

## <span data-ttu-id="c8d7d-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="c8d7d-143">NOTES</span></span>

## <span data-ttu-id="c8d7d-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c8d7d-144">RELATED LINKS</span></span>

[<span data-ttu-id="c8d7d-145">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c8d7d-145">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="c8d7d-146">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c8d7d-146">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="c8d7d-147">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c8d7d-147">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)
