---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6A46DA60-2ACF-4842-B5B3-58944264854A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainer.md
ms.openlocfilehash: a6ea7a2686d084b241e1ba3ff5c513c0d03128c7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074659"
---
# <span data-ttu-id="81bb2-101">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="81bb2-101">Remove-AzStorageContainer</span></span>

## <span data-ttu-id="81bb2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="81bb2-102">SYNOPSIS</span></span>
<span data-ttu-id="81bb2-103">Удаляет указанный контейнер хранилища.</span><span class="sxs-lookup"><span data-stu-id="81bb2-103">Removes the specified storage container.</span></span>

## <span data-ttu-id="81bb2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="81bb2-104">SYNTAX</span></span>

```
Remove-AzStorageContainer [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="81bb2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="81bb2-105">DESCRIPTION</span></span>
<span data-ttu-id="81bb2-106">Командлет **Remove-AzStorageContainer** удаляет указанный контейнер хранилища в Azure.</span><span class="sxs-lookup"><span data-stu-id="81bb2-106">The **Remove-AzStorageContainer** cmdlet removes the specified storage container in Azure.</span></span>

## <span data-ttu-id="81bb2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="81bb2-107">EXAMPLES</span></span>

### <span data-ttu-id="81bb2-108">Пример 1: удаление контейнера</span><span class="sxs-lookup"><span data-stu-id="81bb2-108">Example 1: Remove a container</span></span>
```
PS C:\>Remove-AzStorageContainer -Name "MyTestContainer"
```

<span data-ttu-id="81bb2-109">В этом примере удаляется контейнер с именем MyTestContainer.</span><span class="sxs-lookup"><span data-stu-id="81bb2-109">This example removes a container named MyTestContainer.</span></span>

## <span data-ttu-id="81bb2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="81bb2-110">PARAMETERS</span></span>

### <span data-ttu-id="81bb2-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="81bb2-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="81bb2-112">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="81bb2-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="81bb2-113">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="81bb2-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="81bb2-114">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="81bb2-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81bb2-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="81bb2-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="81bb2-116">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="81bb2-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="81bb2-117">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="81bb2-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="81bb2-118">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="81bb2-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="81bb2-119">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="81bb2-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="81bb2-120">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="81bb2-120">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81bb2-121">-Context</span><span class="sxs-lookup"><span data-stu-id="81bb2-121">-Context</span></span>
<span data-ttu-id="81bb2-122">Задает контекст для контейнера, который вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="81bb2-122">Specifies a context for the container you want to remove.</span></span>
<span data-ttu-id="81bb2-123">Вы можете создать его с помощью командлета New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="81bb2-123">You can use the New-AzStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="81bb2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81bb2-124">-DefaultProfile</span></span>
<span data-ttu-id="81bb2-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="81bb2-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81bb2-126">-Force</span><span class="sxs-lookup"><span data-stu-id="81bb2-126">-Force</span></span>
<span data-ttu-id="81bb2-127">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="81bb2-127">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81bb2-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="81bb2-128">-Name</span></span>
<span data-ttu-id="81bb2-129">Указывает имя контейнера, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="81bb2-129">Specifies the name of the container to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81bb2-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81bb2-130">-PassThru</span></span>
<span data-ttu-id="81bb2-131">Указывает на то, что этот командлет возвращает **логическое значение** , отражающее успешное выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="81bb2-131">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="81bb2-132">По умолчанию этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="81bb2-132">By default, this cmdlet does not return a value.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81bb2-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="81bb2-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="81bb2-134">Указывает интервал времени ожидания службы (в секундах) для запроса.</span><span class="sxs-lookup"><span data-stu-id="81bb2-134">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="81bb2-135">Если заданный интервал проходит до обработки запроса службой, служба хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="81bb2-135">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81bb2-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="81bb2-136">-Confirm</span></span>
<span data-ttu-id="81bb2-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="81bb2-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81bb2-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81bb2-138">-WhatIf</span></span>
<span data-ttu-id="81bb2-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="81bb2-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81bb2-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="81bb2-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81bb2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81bb2-141">CommonParameters</span></span>
<span data-ttu-id="81bb2-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="81bb2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81bb2-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81bb2-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81bb2-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="81bb2-144">INPUTS</span></span>

### <span data-ttu-id="81bb2-145">System. String</span><span class="sxs-lookup"><span data-stu-id="81bb2-145">System.String</span></span>

### <span data-ttu-id="81bb2-146">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="81bb2-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="81bb2-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="81bb2-147">OUTPUTS</span></span>

### <span data-ttu-id="81bb2-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="81bb2-148">System.Boolean</span></span>

## <span data-ttu-id="81bb2-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="81bb2-149">NOTES</span></span>

## <span data-ttu-id="81bb2-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="81bb2-150">RELATED LINKS</span></span>

[<span data-ttu-id="81bb2-151">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="81bb2-151">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="81bb2-152">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="81bb2-152">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)
