---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E2CCDA8F-2D45-4F25-B297-337B7AB021E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: d8c9e0e49ba7a5caa9cb93290ef5e96b60fd4430
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245798"
---
# <span data-ttu-id="f09c1-101">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f09c1-101">Remove-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="f09c1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f09c1-102">SYNOPSIS</span></span>
<span data-ttu-id="f09c1-103">Удаление политики сохраненного доступа из общей папке хранилища.</span><span class="sxs-lookup"><span data-stu-id="f09c1-103">Removes a stored access policy from a Storage share.</span></span>

## <span data-ttu-id="f09c1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f09c1-104">SYNTAX</span></span>

```
Remove-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f09c1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f09c1-105">DESCRIPTION</span></span>
<span data-ttu-id="f09c1-106">Командлет **Remove-AzStorageShareStoredAccessPolicy** удаляет политику доступа из хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="f09c1-106">The **Remove-AzStorageShareStoredAccessPolicy** cmdlet removes a stored access policy from an Azure Storage share.</span></span>

## <span data-ttu-id="f09c1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f09c1-107">EXAMPLES</span></span>

### <span data-ttu-id="f09c1-108">Пример 1: Удаление политики сохраненного доступа из общего доступа к хранилищу Azure</span><span class="sxs-lookup"><span data-stu-id="f09c1-108">Example 1: Remove a stored access policy from an Azure Storage share</span></span>
```
PS C:\>Remove-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="f09c1-109">Эта команда удаляет политику сохраненного доступа с именем GeneralPolicy из ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="f09c1-109">This command removes a stored access policy named GeneralPolicy from ContosoShare.</span></span>

## <span data-ttu-id="f09c1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f09c1-110">PARAMETERS</span></span>

### <span data-ttu-id="f09c1-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f09c1-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f09c1-112">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="f09c1-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f09c1-113">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="f09c1-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f09c1-114">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="f09c1-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f09c1-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f09c1-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f09c1-116">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="f09c1-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="f09c1-117">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="f09c1-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="f09c1-118">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="f09c1-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="f09c1-119">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="f09c1-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="f09c1-120">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="f09c1-120">The default value is 10.</span></span>

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

### <span data-ttu-id="f09c1-121">-Context</span><span class="sxs-lookup"><span data-stu-id="f09c1-121">-Context</span></span>
<span data-ttu-id="f09c1-122">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="f09c1-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f09c1-123">Чтобы получить контекст хранения, используйте командлет [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="f09c1-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="f09c1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f09c1-124">-DefaultProfile</span></span>
<span data-ttu-id="f09c1-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f09c1-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f09c1-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f09c1-126">-PassThru</span></span>
<span data-ttu-id="f09c1-127">Указывает на то, что этот командлет возвращает **логическое значение** , отражающее успешное выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="f09c1-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="f09c1-128">По умолчанию этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f09c1-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="f09c1-129">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="f09c1-129">-Policy</span></span>
<span data-ttu-id="f09c1-130">Указывает имя политики хранения, которая удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="f09c1-130">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f09c1-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f09c1-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f09c1-132">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="f09c1-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="f09c1-133">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="f09c1-133">-ShareName</span></span>
<span data-ttu-id="f09c1-134">Указывает имя общего хранилища, для которого этот командлет удаляет политику.</span><span class="sxs-lookup"><span data-stu-id="f09c1-134">Specifies the Storage share name for which this cmdlet removes a policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f09c1-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f09c1-135">-Confirm</span></span>
<span data-ttu-id="f09c1-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f09c1-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f09c1-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f09c1-137">-WhatIf</span></span>
<span data-ttu-id="f09c1-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f09c1-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f09c1-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f09c1-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f09c1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f09c1-140">CommonParameters</span></span>
<span data-ttu-id="f09c1-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f09c1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f09c1-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f09c1-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f09c1-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f09c1-143">INPUTS</span></span>

### <span data-ttu-id="f09c1-144">System. String</span><span class="sxs-lookup"><span data-stu-id="f09c1-144">System.String</span></span>

### <span data-ttu-id="f09c1-145">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f09c1-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f09c1-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f09c1-146">OUTPUTS</span></span>

### <span data-ttu-id="f09c1-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f09c1-147">System.Boolean</span></span>

## <span data-ttu-id="f09c1-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="f09c1-148">NOTES</span></span>

## <span data-ttu-id="f09c1-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f09c1-149">RELATED LINKS</span></span>

[<span data-ttu-id="f09c1-150">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f09c1-150">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="f09c1-151">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f09c1-151">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="f09c1-152">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f09c1-152">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="f09c1-153">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f09c1-153">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)