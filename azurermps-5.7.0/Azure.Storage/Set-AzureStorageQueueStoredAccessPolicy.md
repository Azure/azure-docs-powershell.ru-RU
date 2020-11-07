---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 9a3a19b2e0773d1513ce57dc5fe7ca7502bb325d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735133"
---
# <span data-ttu-id="a32d2-101">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a32d2-101">Set-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="a32d2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a32d2-102">SYNOPSIS</span></span>
<span data-ttu-id="a32d2-103">Задает политику сохранения для доступа для очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="a32d2-103">Sets a stored access policy for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a32d2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a32d2-104">SYNTAX</span></span>

```
Set-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a32d2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a32d2-105">DESCRIPTION</span></span>
<span data-ttu-id="a32d2-106">Командлет **Set-AzureStorageQueueStoredAccessPolicy** задает политику сохраненного доступа для очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="a32d2-106">The **Set-AzureStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="a32d2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a32d2-107">EXAMPLES</span></span>

### <span data-ttu-id="a32d2-108">Пример 1: Настройка политики доступа в очереди с полным разрешением</span><span class="sxs-lookup"><span data-stu-id="a32d2-108">Example 1: Set a stored access policy in the queue with full permission</span></span>
```
PS C:\> Set-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07" -Permission arup
```

<span data-ttu-id="a32d2-109">Эта команда задает политику доступа с именем Policy07 для очереди хранения с именем MyQueue.</span><span class="sxs-lookup"><span data-stu-id="a32d2-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="a32d2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a32d2-110">PARAMETERS</span></span>

### <span data-ttu-id="a32d2-111">-Context</span><span class="sxs-lookup"><span data-stu-id="a32d2-111">-Context</span></span>
<span data-ttu-id="a32d2-112">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="a32d2-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a32d2-113">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="a32d2-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a32d2-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="a32d2-114">-ExpiryTime</span></span>
<span data-ttu-id="a32d2-115">Указывает время, в течение которого политика хранения сохраненных прав становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="a32d2-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="a32d2-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="a32d2-116">-NoExpiryTime</span></span>
<span data-ttu-id="a32d2-117">Указывает на то, что политика доступа не содержит дату окончания срока действия.</span><span class="sxs-lookup"><span data-stu-id="a32d2-117">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="a32d2-118">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="a32d2-118">-NoStartTime</span></span>
<span data-ttu-id="a32d2-119">Указывает на то, что этот командлет задает время запуска, которое должно быть $Null.</span><span class="sxs-lookup"><span data-stu-id="a32d2-119">Indicates that this cmdlet sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="a32d2-120">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="a32d2-120">-Permission</span></span>
<span data-ttu-id="a32d2-121">Определяет разрешения в политике сохранения доступа для доступа к очереди хранилища.</span><span class="sxs-lookup"><span data-stu-id="a32d2-121">Specifies permissions in the stored access policy to access the storage queue.</span></span>

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

### <span data-ttu-id="a32d2-122">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="a32d2-122">-Policy</span></span>
<span data-ttu-id="a32d2-123">Задает имя для политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="a32d2-123">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="a32d2-124">-Очередь</span><span class="sxs-lookup"><span data-stu-id="a32d2-124">-Queue</span></span>
<span data-ttu-id="a32d2-125">Указывает имя очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="a32d2-125">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="a32d2-126">-StartTime</span><span class="sxs-lookup"><span data-stu-id="a32d2-126">-StartTime</span></span>
<span data-ttu-id="a32d2-127">Указывает время вступления в силу политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="a32d2-127">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="a32d2-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a32d2-128">-Confirm</span></span>
<span data-ttu-id="a32d2-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a32d2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a32d2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a32d2-130">-WhatIf</span></span>
<span data-ttu-id="a32d2-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a32d2-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a32d2-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a32d2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a32d2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a32d2-133">CommonParameters</span></span>
<span data-ttu-id="a32d2-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a32d2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a32d2-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a32d2-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a32d2-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a32d2-136">INPUTS</span></span>

### <span data-ttu-id="a32d2-137">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a32d2-137">IStorageContext</span></span>

<span data-ttu-id="a32d2-138">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="a32d2-138">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="a32d2-139">Подстрок</span><span class="sxs-lookup"><span data-stu-id="a32d2-139">String</span></span>

<span data-ttu-id="a32d2-140">Параметр "Queue" принимает значение типа String из конвейера</span><span class="sxs-lookup"><span data-stu-id="a32d2-140">Parameter 'Queue' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="a32d2-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a32d2-141">OUTPUTS</span></span>

### <span data-ttu-id="a32d2-142">System. String</span><span class="sxs-lookup"><span data-stu-id="a32d2-142">System.String</span></span>

## <span data-ttu-id="a32d2-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="a32d2-143">NOTES</span></span>

## <span data-ttu-id="a32d2-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a32d2-144">RELATED LINKS</span></span>

[<span data-ttu-id="a32d2-145">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a32d2-145">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="a32d2-146">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a32d2-146">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="a32d2-147">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a32d2-147">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)
