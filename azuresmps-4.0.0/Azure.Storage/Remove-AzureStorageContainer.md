---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6A46DA60-2ACF-4842-B5B3-58944264854A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ccaa0ef1ce2a29851d6e90235e4564df3bde876
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555248"
---
# <span data-ttu-id="ed67e-101">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ed67e-101">Remove-AzureStorageContainer</span></span>

## <span data-ttu-id="ed67e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ed67e-102">SYNOPSIS</span></span>
<span data-ttu-id="ed67e-103">Удаляет указанный контейнер хранилища.</span><span class="sxs-lookup"><span data-stu-id="ed67e-103">Removes the specified storage container.</span></span>

## <span data-ttu-id="ed67e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ed67e-104">SYNTAX</span></span>

```
Remove-AzureStorageContainer [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed67e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed67e-105">DESCRIPTION</span></span>
<span data-ttu-id="ed67e-106">Командлет **Remove-AzureStorageContainer** удаляет указанный контейнер хранилища в Azure.</span><span class="sxs-lookup"><span data-stu-id="ed67e-106">The **Remove-AzureStorageContainer** cmdlet removes the specified storage container in Azure.</span></span>

## <span data-ttu-id="ed67e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ed67e-107">EXAMPLES</span></span>

### <span data-ttu-id="ed67e-108">Пример 1: удаление контейнера</span><span class="sxs-lookup"><span data-stu-id="ed67e-108">Example 1: Remove a container</span></span>
```
PS C:\>Remove-AzureStorageContainer -Name "MyTestContainer"
```

<span data-ttu-id="ed67e-109">В этом примере удаляется контейнер с именем MyTestContainer.</span><span class="sxs-lookup"><span data-stu-id="ed67e-109">This example removes a container named MyTestContainer.</span></span>

## <span data-ttu-id="ed67e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ed67e-110">PARAMETERS</span></span>

### <span data-ttu-id="ed67e-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ed67e-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ed67e-112">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="ed67e-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ed67e-113">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="ed67e-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ed67e-114">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="ed67e-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ed67e-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ed67e-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ed67e-116">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="ed67e-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ed67e-117">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="ed67e-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ed67e-118">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="ed67e-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ed67e-119">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="ed67e-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ed67e-120">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="ed67e-120">The default value is 10.</span></span>

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

### <span data-ttu-id="ed67e-121">-Context</span><span class="sxs-lookup"><span data-stu-id="ed67e-121">-Context</span></span>
<span data-ttu-id="ed67e-122">Задает контекст для контейнера, который вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="ed67e-122">Specifies a context for the container you want to remove.</span></span>
<span data-ttu-id="ed67e-123">Вы можете создать его с помощью командлета New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="ed67e-123">You can use the New-AzureStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="ed67e-124">-Force</span><span class="sxs-lookup"><span data-stu-id="ed67e-124">-Force</span></span>
<span data-ttu-id="ed67e-125">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="ed67e-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ed67e-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ed67e-126">-Name</span></span>
<span data-ttu-id="ed67e-127">Указывает имя контейнера, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="ed67e-127">Specifies the name of the container to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed67e-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed67e-128">-PassThru</span></span>
<span data-ttu-id="ed67e-129">Указывает на то, что этот командлет возвращает **логическое значение** , отражающее успешное выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="ed67e-129">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="ed67e-130">По умолчанию этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ed67e-130">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="ed67e-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ed67e-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ed67e-132">Указывает интервал времени ожидания службы (в секундах) для запроса.</span><span class="sxs-lookup"><span data-stu-id="ed67e-132">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="ed67e-133">Если заданный интервал проходит до обработки запроса службой, служба хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="ed67e-133">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="ed67e-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed67e-134">-Confirm</span></span>
<span data-ttu-id="ed67e-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ed67e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed67e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed67e-136">-WhatIf</span></span>
<span data-ttu-id="ed67e-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ed67e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed67e-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ed67e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed67e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed67e-139">CommonParameters</span></span>
<span data-ttu-id="ed67e-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ed67e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed67e-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed67e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed67e-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ed67e-142">INPUTS</span></span>

## <span data-ttu-id="ed67e-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed67e-143">OUTPUTS</span></span>

## <span data-ttu-id="ed67e-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="ed67e-144">NOTES</span></span>

## <span data-ttu-id="ed67e-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ed67e-145">RELATED LINKS</span></span>

[<span data-ttu-id="ed67e-146">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ed67e-146">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="ed67e-147">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ed67e-147">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)
