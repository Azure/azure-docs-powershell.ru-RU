---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3E79EE05-7E52-4C54-B985-441BC2599925
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 08b3ec17476e959aa7190cfb914468eb8ab73775
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732663"
---
# <span data-ttu-id="e2697-101">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e2697-101">Remove-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="e2697-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e2697-102">SYNOPSIS</span></span>
<span data-ttu-id="e2697-103">Удаляет политику сохраненного доступа из контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="e2697-103">Removes a stored access policy from an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2697-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e2697-104">SYNTAX</span></span>

```
Remove-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2697-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2697-105">DESCRIPTION</span></span>
<span data-ttu-id="e2697-106">Командлет **Remove-AzureStorageContainerStoredAccessPolicy** удаляет политику сохраненного доступа из контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="e2697-106">The **Remove-AzureStorageContainerStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="e2697-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e2697-107">EXAMPLES</span></span>

### <span data-ttu-id="e2697-108">Пример 1: Удаление политики сохраненного доступа из контейнера хранилища</span><span class="sxs-lookup"><span data-stu-id="e2697-108">Example 1: Remove a stored access policy from a storage container</span></span>
```
PS C:\>Remove-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy03"
```

<span data-ttu-id="e2697-109">Эта команда удаляет политику доступа с именем Policy03 из хранимого контейнера с именем MyContainer.</span><span class="sxs-lookup"><span data-stu-id="e2697-109">This command removes an access policy named Policy03 from the stored container named MyContainer.</span></span>

## <span data-ttu-id="e2697-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e2697-110">PARAMETERS</span></span>

### <span data-ttu-id="e2697-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e2697-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e2697-112">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="e2697-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e2697-113">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="e2697-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e2697-114">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="e2697-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e2697-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e2697-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e2697-116">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="e2697-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="e2697-117">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="e2697-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="e2697-118">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="e2697-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="e2697-119">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="e2697-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="e2697-120">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="e2697-120">The default value is 10.</span></span>

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

### <span data-ttu-id="e2697-121">-Container</span><span class="sxs-lookup"><span data-stu-id="e2697-121">-Container</span></span>
<span data-ttu-id="e2697-122">Указывает имя контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="e2697-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="e2697-123">-Context</span><span class="sxs-lookup"><span data-stu-id="e2697-123">-Context</span></span>
<span data-ttu-id="e2697-124">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="e2697-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e2697-125">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="e2697-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e2697-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2697-126">-PassThru</span></span>
<span data-ttu-id="e2697-127">Указывает на то, что этот командлет возвращает **логическое значение** , отражающее успешное выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="e2697-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="e2697-128">По умолчанию этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="e2697-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="e2697-129">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="e2697-129">-Policy</span></span>
<span data-ttu-id="e2697-130">Указывает имя политики хранения, которая удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="e2697-130">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e2697-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e2697-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e2697-132">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="e2697-132">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e2697-133">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="e2697-133">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e2697-134">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="e2697-134">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e2697-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2697-135">-Confirm</span></span>
<span data-ttu-id="e2697-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e2697-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2697-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2697-137">-WhatIf</span></span>
<span data-ttu-id="e2697-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e2697-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2697-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e2697-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2697-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2697-140">CommonParameters</span></span>
<span data-ttu-id="e2697-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e2697-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2697-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2697-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2697-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e2697-143">INPUTS</span></span>

### <span data-ttu-id="e2697-144">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e2697-144">IStorageContext</span></span>

<span data-ttu-id="e2697-145">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="e2697-145">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="e2697-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2697-146">OUTPUTS</span></span>

### <span data-ttu-id="e2697-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e2697-147">System.Boolean</span></span>

## <span data-ttu-id="e2697-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="e2697-148">NOTES</span></span>

## <span data-ttu-id="e2697-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e2697-149">RELATED LINKS</span></span>

[<span data-ttu-id="e2697-150">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e2697-150">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="e2697-151">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e2697-151">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="e2697-152">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="e2697-152">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="e2697-153">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e2697-153">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)
