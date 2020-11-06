---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3E79EE05-7E52-4C54-B985-441BC2599925
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e2a6e00832ea57f3d5608b30791c37e5cde5be5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555247"
---
# <span data-ttu-id="f0653-101">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f0653-101">Remove-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="f0653-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f0653-102">SYNOPSIS</span></span>
<span data-ttu-id="f0653-103">Удаляет политику сохраненного доступа из контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="f0653-103">Removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="f0653-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f0653-104">SYNTAX</span></span>

```
Remove-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0653-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0653-105">DESCRIPTION</span></span>
<span data-ttu-id="f0653-106">Командлет **Remove-AzureStorageContainerStoredAccessPolicy** удаляет политику сохраненного доступа из контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="f0653-106">The **Remove-AzureStorageContainerStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="f0653-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f0653-107">EXAMPLES</span></span>

### <span data-ttu-id="f0653-108">Пример 1: Удаление политики сохраненного доступа из контейнера хранилища</span><span class="sxs-lookup"><span data-stu-id="f0653-108">Example 1: Remove a stored access policy from a storage container</span></span>
```
PS C:\>Remove-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy03"
```

<span data-ttu-id="f0653-109">Эта команда удаляет политику доступа с именем Policy03 из хранимого контейнера с именем MyContainer.</span><span class="sxs-lookup"><span data-stu-id="f0653-109">This command removes an access policy named Policy03 from the stored container named MyContainer.</span></span>

## <span data-ttu-id="f0653-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f0653-110">PARAMETERS</span></span>

### <span data-ttu-id="f0653-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f0653-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f0653-112">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="f0653-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f0653-113">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="f0653-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f0653-114">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="f0653-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f0653-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f0653-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f0653-116">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="f0653-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="f0653-117">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="f0653-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="f0653-118">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="f0653-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="f0653-119">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="f0653-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="f0653-120">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="f0653-120">The default value is 10.</span></span>

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

### <span data-ttu-id="f0653-121">-Container</span><span class="sxs-lookup"><span data-stu-id="f0653-121">-Container</span></span>
<span data-ttu-id="f0653-122">Указывает имя контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="f0653-122">Specifies the Azure storage container name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0653-123">-Context</span><span class="sxs-lookup"><span data-stu-id="f0653-123">-Context</span></span>
<span data-ttu-id="f0653-124">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="f0653-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f0653-125">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="f0653-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f0653-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0653-126">-PassThru</span></span>
<span data-ttu-id="f0653-127">Указывает на то, что этот командлет возвращает **логическое значение** , отражающее успешное выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="f0653-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="f0653-128">По умолчанию этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f0653-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="f0653-129">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="f0653-129">-Policy</span></span>
<span data-ttu-id="f0653-130">Указывает политику сохраненного доступа, которая включает разрешения для этого маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="f0653-130">Specifies the stored access policy, which includes the permissions for this SAS token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0653-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f0653-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f0653-132">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="f0653-132">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f0653-133">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="f0653-133">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f0653-134">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="f0653-134">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f0653-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0653-135">-Confirm</span></span>
<span data-ttu-id="f0653-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f0653-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0653-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0653-137">-WhatIf</span></span>
<span data-ttu-id="f0653-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f0653-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0653-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f0653-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0653-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0653-140">CommonParameters</span></span>
<span data-ttu-id="f0653-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f0653-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0653-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0653-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0653-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f0653-143">INPUTS</span></span>

## <span data-ttu-id="f0653-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0653-144">OUTPUTS</span></span>

## <span data-ttu-id="f0653-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="f0653-145">NOTES</span></span>

## <span data-ttu-id="f0653-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f0653-146">RELATED LINKS</span></span>

[<span data-ttu-id="f0653-147">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f0653-147">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="f0653-148">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f0653-148">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="f0653-149">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="f0653-149">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="f0653-150">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f0653-150">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)
