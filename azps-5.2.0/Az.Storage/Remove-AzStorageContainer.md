---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6A46DA60-2ACF-4842-B5B3-58944264854A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainer.md
ms.openlocfilehash: a6ea7a2686d084b241e1ba3ff5c513c0d03128c7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403476"
---
# <span data-ttu-id="0c6d8-101">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0c6d8-101">Remove-AzStorageContainer</span></span>

## <span data-ttu-id="0c6d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c6d8-102">SYNOPSIS</span></span>
<span data-ttu-id="0c6d8-103">Удаляет указанный контейнер хранилища.</span><span class="sxs-lookup"><span data-stu-id="0c6d8-103">Removes the specified storage container.</span></span>

## <span data-ttu-id="0c6d8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0c6d8-104">SYNTAX</span></span>

```
Remove-AzStorageContainer [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0c6d8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c6d8-105">DESCRIPTION</span></span>
<span data-ttu-id="0c6d8-106">С **его использованием** удаляется указанный контейнер хранилища в Azure.</span><span class="sxs-lookup"><span data-stu-id="0c6d8-106">The **Remove-AzStorageContainer** cmdlet removes the specified storage container in Azure.</span></span>

## <span data-ttu-id="0c6d8-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0c6d8-107">EXAMPLES</span></span>

### <span data-ttu-id="0c6d8-108">Пример 1. Удаление контейнера</span><span class="sxs-lookup"><span data-stu-id="0c6d8-108">Example 1: Remove a container</span></span>
```
PS C:\>Remove-AzStorageContainer -Name "MyTestContainer"
```

<span data-ttu-id="0c6d8-109">В этом примере удаляется контейнер с именем MyTestContainer.</span><span class="sxs-lookup"><span data-stu-id="0c6d8-109">This example removes a container named MyTestContainer.</span></span>

## <span data-ttu-id="0c6d8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c6d8-110">PARAMETERS</span></span>

### <span data-ttu-id="0c6d8-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0c6d8-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="0c6d8-112">Указывает интервал времени и времени, в секундах, для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="0c6d8-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="0c6d8-113">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="0c6d8-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="0c6d8-114">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="0c6d8-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="0c6d8-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0c6d8-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0c6d8-116">Указывает максимальное число сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="0c6d8-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="0c6d8-117">С помощью этого параметра можно ограничить одновременное использование локального ЦП и пропускной способности, указав максимальное количество сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="0c6d8-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="0c6d8-118">Указанное значение является абсолютным и не умножается на основное.</span><span class="sxs-lookup"><span data-stu-id="0c6d8-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="0c6d8-119">Этот параметр помогает уменьшить количество проблем с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.</span><span class="sxs-lookup"><span data-stu-id="0c6d8-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="0c6d8-120">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="0c6d8-120">The default value is 10.</span></span>

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

### <span data-ttu-id="0c6d8-121">-Контекст</span><span class="sxs-lookup"><span data-stu-id="0c6d8-121">-Context</span></span>
<span data-ttu-id="0c6d8-122">Определяет контекст для контейнера, который вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="0c6d8-122">Specifies a context for the container you want to remove.</span></span>
<span data-ttu-id="0c6d8-123">Для создания New-AzStorageContext можно использовать новый New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="0c6d8-123">You can use the New-AzStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="0c6d8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c6d8-124">-DefaultProfile</span></span>
<span data-ttu-id="0c6d8-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0c6d8-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c6d8-126">-Force</span><span class="sxs-lookup"><span data-stu-id="0c6d8-126">-Force</span></span>
<span data-ttu-id="0c6d8-127">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="0c6d8-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0c6d8-128">-Name</span><span class="sxs-lookup"><span data-stu-id="0c6d8-128">-Name</span></span>
<span data-ttu-id="0c6d8-129">Имя контейнера, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="0c6d8-129">Specifies the name of the container to remove.</span></span>

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

### <span data-ttu-id="0c6d8-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0c6d8-130">-PassThru</span></span>
<span data-ttu-id="0c6d8-131">Указывает на то, что этот cmdlet возвращает **boolean,** который отражает успешность операции.</span><span class="sxs-lookup"><span data-stu-id="0c6d8-131">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="0c6d8-132">По умолчанию этот cmdlet не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="0c6d8-132">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="0c6d8-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0c6d8-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="0c6d8-134">Указывает для запроса интервал времени отрезка времени для стороны обслуживания (в секундах).</span><span class="sxs-lookup"><span data-stu-id="0c6d8-134">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="0c6d8-135">Если заданный интервал задан до обработки запроса службой службы хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="0c6d8-135">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="0c6d8-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0c6d8-136">-Confirm</span></span>
<span data-ttu-id="0c6d8-137">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c6d8-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c6d8-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c6d8-138">-WhatIf</span></span>
<span data-ttu-id="0c6d8-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c6d8-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c6d8-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0c6d8-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c6d8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c6d8-141">CommonParameters</span></span>
<span data-ttu-id="0c6d8-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c6d8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c6d8-143">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c6d8-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c6d8-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0c6d8-144">INPUTS</span></span>

### <span data-ttu-id="0c6d8-145">System.String</span><span class="sxs-lookup"><span data-stu-id="0c6d8-145">System.String</span></span>

### <span data-ttu-id="0c6d8-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0c6d8-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0c6d8-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0c6d8-147">OUTPUTS</span></span>

### <span data-ttu-id="0c6d8-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0c6d8-148">System.Boolean</span></span>

## <span data-ttu-id="0c6d8-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0c6d8-149">NOTES</span></span>

## <span data-ttu-id="0c6d8-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0c6d8-150">RELATED LINKS</span></span>

[<span data-ttu-id="0c6d8-151">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0c6d8-151">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="0c6d8-152">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0c6d8-152">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)
