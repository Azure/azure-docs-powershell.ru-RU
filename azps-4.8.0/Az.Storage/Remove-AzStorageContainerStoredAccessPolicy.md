---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3E79EE05-7E52-4C54-B985-441BC2599925
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 1b8667d08e02c9294a18f4cbf84cb27085cbc118
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078586"
---
# <span data-ttu-id="5a70d-101">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5a70d-101">Remove-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="5a70d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5a70d-102">SYNOPSIS</span></span>
<span data-ttu-id="5a70d-103">Удаляет политику сохраненного доступа из контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="5a70d-103">Removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="5a70d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5a70d-104">SYNTAX</span></span>

```
Remove-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5a70d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a70d-105">DESCRIPTION</span></span>
<span data-ttu-id="5a70d-106">Командлет **Remove-AzStorageContainerStoredAccessPolicy** удаляет политику сохраненного доступа из контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="5a70d-106">The **Remove-AzStorageContainerStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="5a70d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5a70d-107">EXAMPLES</span></span>

### <span data-ttu-id="5a70d-108">Пример 1: Удаление политики сохраненного доступа из контейнера хранилища</span><span class="sxs-lookup"><span data-stu-id="5a70d-108">Example 1: Remove a stored access policy from a storage container</span></span>
```
PS C:\>Remove-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy03"
```

<span data-ttu-id="5a70d-109">Эта команда удаляет политику доступа с именем Policy03 из хранимого контейнера с именем MyContainer.</span><span class="sxs-lookup"><span data-stu-id="5a70d-109">This command removes an access policy named Policy03 from the stored container named MyContainer.</span></span>

## <span data-ttu-id="5a70d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5a70d-110">PARAMETERS</span></span>

### <span data-ttu-id="5a70d-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5a70d-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="5a70d-112">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="5a70d-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="5a70d-113">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="5a70d-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="5a70d-114">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="5a70d-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="5a70d-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="5a70d-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="5a70d-116">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="5a70d-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="5a70d-117">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="5a70d-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="5a70d-118">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="5a70d-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="5a70d-119">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="5a70d-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="5a70d-120">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="5a70d-120">The default value is 10.</span></span>

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

### <span data-ttu-id="5a70d-121">-Container</span><span class="sxs-lookup"><span data-stu-id="5a70d-121">-Container</span></span>
<span data-ttu-id="5a70d-122">Указывает имя контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="5a70d-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="5a70d-123">-Context</span><span class="sxs-lookup"><span data-stu-id="5a70d-123">-Context</span></span>
<span data-ttu-id="5a70d-124">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="5a70d-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="5a70d-125">Чтобы получить контекст хранилища, используйте командлет New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="5a70d-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="5a70d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a70d-126">-DefaultProfile</span></span>
<span data-ttu-id="5a70d-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5a70d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a70d-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a70d-128">-PassThru</span></span>
<span data-ttu-id="5a70d-129">Указывает на то, что этот командлет возвращает **логическое значение** , отражающее успешное выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="5a70d-129">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="5a70d-130">По умолчанию этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="5a70d-130">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="5a70d-131">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="5a70d-131">-Policy</span></span>
<span data-ttu-id="5a70d-132">Указывает имя политики хранения, которая удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="5a70d-132">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5a70d-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5a70d-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="5a70d-134">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="5a70d-134">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="5a70d-135">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="5a70d-135">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="5a70d-136">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="5a70d-136">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="5a70d-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a70d-137">-Confirm</span></span>
<span data-ttu-id="5a70d-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5a70d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a70d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a70d-139">-WhatIf</span></span>
<span data-ttu-id="5a70d-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5a70d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a70d-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5a70d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a70d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a70d-142">CommonParameters</span></span>
<span data-ttu-id="5a70d-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5a70d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a70d-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a70d-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a70d-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5a70d-145">INPUTS</span></span>

### <span data-ttu-id="5a70d-146">System. String</span><span class="sxs-lookup"><span data-stu-id="5a70d-146">System.String</span></span>

### <span data-ttu-id="5a70d-147">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5a70d-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="5a70d-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a70d-148">OUTPUTS</span></span>

### <span data-ttu-id="5a70d-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5a70d-149">System.Boolean</span></span>

## <span data-ttu-id="5a70d-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="5a70d-150">NOTES</span></span>

## <span data-ttu-id="5a70d-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5a70d-151">RELATED LINKS</span></span>

[<span data-ttu-id="5a70d-152">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5a70d-152">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="5a70d-153">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5a70d-153">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="5a70d-154">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="5a70d-154">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="5a70d-155">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5a70d-155">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)