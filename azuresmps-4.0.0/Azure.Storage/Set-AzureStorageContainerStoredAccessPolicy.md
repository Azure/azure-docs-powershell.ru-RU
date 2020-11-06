---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 730ECC60-72DE-46DA-A177-D5749F540710
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1bdded3834806e33f4605f626b78fe06bc370bf6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556367"
---
# <span data-ttu-id="d0cb0-101">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d0cb0-101">Set-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="d0cb0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d0cb0-102">SYNOPSIS</span></span>
<span data-ttu-id="d0cb0-103">Задает политику сохранения для доступа для контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="d0cb0-103">Sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="d0cb0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d0cb0-104">SYNTAX</span></span>

```
Set-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0cb0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0cb0-105">DESCRIPTION</span></span>
<span data-ttu-id="d0cb0-106">Командлет **Set-AzureStorageContainerStoredAccessPolicy** устанавливает политику доступа для контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="d0cb0-106">The **Set-AzureStorageContainerStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="d0cb0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d0cb0-107">EXAMPLES</span></span>

### <span data-ttu-id="d0cb0-108">Пример 1: Настройка политики для сохраненного доступа в контейнере хранилища</span><span class="sxs-lookup"><span data-stu-id="d0cb0-108">Example 1: Set a stored access policy in a storage container</span></span>
```
PS C:\>Set-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy06"
```

<span data-ttu-id="d0cb0-109">Эта команда задает политику доступа с именем Policy06 для контейнера хранилища с именем MyContainer.</span><span class="sxs-lookup"><span data-stu-id="d0cb0-109">This command sets an access policy named Policy06 for storage container named MyContainer.</span></span>

## <span data-ttu-id="d0cb0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d0cb0-110">PARAMETERS</span></span>

### <span data-ttu-id="d0cb0-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d0cb0-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d0cb0-112">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="d0cb0-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d0cb0-113">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="d0cb0-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d0cb0-114">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="d0cb0-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0cb0-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d0cb0-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d0cb0-116">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="d0cb0-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d0cb0-117">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="d0cb0-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d0cb0-118">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="d0cb0-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d0cb0-119">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="d0cb0-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d0cb0-120">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="d0cb0-120">The default value is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0cb0-121">-Container</span><span class="sxs-lookup"><span data-stu-id="d0cb0-121">-Container</span></span>
<span data-ttu-id="d0cb0-122">Указывает имя контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="d0cb0-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="d0cb0-123">-Context</span><span class="sxs-lookup"><span data-stu-id="d0cb0-123">-Context</span></span>
<span data-ttu-id="d0cb0-124">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="d0cb0-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d0cb0-125">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="d0cb0-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d0cb0-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="d0cb0-126">-ExpiryTime</span></span>
<span data-ttu-id="d0cb0-127">Указывает время, в течение которого политика хранения сохраненных прав становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="d0cb0-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="d0cb0-128">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="d0cb0-128">-NoExpiryTime</span></span>
<span data-ttu-id="d0cb0-129">Указывает на то, что политика доступа не содержит дату окончания срока действия.</span><span class="sxs-lookup"><span data-stu-id="d0cb0-129">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="d0cb0-130">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="d0cb0-130">-NoStartTime</span></span>
<span data-ttu-id="d0cb0-131">Задает время начала, которое должно быть $Null.</span><span class="sxs-lookup"><span data-stu-id="d0cb0-131">Sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="d0cb0-132">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="d0cb0-132">-Permission</span></span>
<span data-ttu-id="d0cb0-133">Указывает уровень общедоступного доступа к этому контейнеру.</span><span class="sxs-lookup"><span data-stu-id="d0cb0-133">Specifies the level of public access to this container.</span></span>

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

### <span data-ttu-id="d0cb0-134">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="d0cb0-134">-Policy</span></span>
<span data-ttu-id="d0cb0-135">Указывает политику сохраненного доступа, которая включает разрешения для маркера данной подписи общего доступа (SAS).</span><span class="sxs-lookup"><span data-stu-id="d0cb0-135">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="d0cb0-136">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d0cb0-136">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d0cb0-137">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="d0cb0-137">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d0cb0-138">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="d0cb0-138">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d0cb0-139">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="d0cb0-139">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0cb0-140">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d0cb0-140">-StartTime</span></span>
<span data-ttu-id="d0cb0-141">Указывает время вступления в силу политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="d0cb0-141">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="d0cb0-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0cb0-142">-Confirm</span></span>
<span data-ttu-id="d0cb0-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d0cb0-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0cb0-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0cb0-144">-WhatIf</span></span>
<span data-ttu-id="d0cb0-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d0cb0-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d0cb0-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d0cb0-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0cb0-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0cb0-147">CommonParameters</span></span>
<span data-ttu-id="d0cb0-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d0cb0-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0cb0-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0cb0-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0cb0-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d0cb0-150">INPUTS</span></span>

## <span data-ttu-id="d0cb0-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0cb0-151">OUTPUTS</span></span>

## <span data-ttu-id="d0cb0-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="d0cb0-152">NOTES</span></span>

## <span data-ttu-id="d0cb0-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d0cb0-153">RELATED LINKS</span></span>

[<span data-ttu-id="d0cb0-154">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d0cb0-154">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="d0cb0-155">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="d0cb0-155">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="d0cb0-156">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d0cb0-156">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="d0cb0-157">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d0cb0-157">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)
