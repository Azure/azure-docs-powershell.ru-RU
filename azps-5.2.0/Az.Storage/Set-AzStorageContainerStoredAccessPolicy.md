---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 730ECC60-72DE-46DA-A177-D5749F540710
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 577dd6cb3ca12daee1cbc4c87d5d1f619c13eea0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403308"
---
# <span data-ttu-id="b50c8-101">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b50c8-101">Set-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="b50c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b50c8-102">SYNOPSIS</span></span>
<span data-ttu-id="b50c8-103">Задает политику хранимого доступа для контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="b50c8-103">Sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="b50c8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b50c8-104">SYNTAX</span></span>

```
Set-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b50c8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b50c8-105">DESCRIPTION</span></span>
<span data-ttu-id="b50c8-106">**Cmdlet Set-AzStorageContainerStoredAccessPolicy** задает политику доступа для контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="b50c8-106">The **Set-AzStorageContainerStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="b50c8-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b50c8-107">EXAMPLES</span></span>

### <span data-ttu-id="b50c8-108">Пример 1. Настройка политики хранимого доступа в контейнере хранилища с полными разрешениями</span><span class="sxs-lookup"><span data-stu-id="b50c8-108">Example 1: Set a stored access policy in a storage container with full permission</span></span>
```
PS C:\>Set-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy06" -Permission rwdl
```

<span data-ttu-id="b50c8-109">Эта команда задает политику доступа с именем Policy06 для контейнера хранилища MyContainer.</span><span class="sxs-lookup"><span data-stu-id="b50c8-109">This command sets an access policy named Policy06 for storage container named MyContainer.</span></span>

## <span data-ttu-id="b50c8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b50c8-110">PARAMETERS</span></span>

### <span data-ttu-id="b50c8-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b50c8-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b50c8-112">Указывает интервал времени и времени, в секундах, для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="b50c8-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b50c8-113">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="b50c8-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b50c8-114">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="b50c8-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b50c8-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b50c8-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b50c8-116">Указывает максимальное число сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="b50c8-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b50c8-117">С помощью этого параметра можно ограничить одновременное использование локального ЦП и пропускной способности, указав максимальное количество сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="b50c8-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b50c8-118">Указанное значение является абсолютным и не умножается на основное.</span><span class="sxs-lookup"><span data-stu-id="b50c8-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b50c8-119">Этот параметр помогает уменьшить количество проблем с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.</span><span class="sxs-lookup"><span data-stu-id="b50c8-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b50c8-120">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="b50c8-120">The default value is 10.</span></span>

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

### <span data-ttu-id="b50c8-121">-Container</span><span class="sxs-lookup"><span data-stu-id="b50c8-121">-Container</span></span>
<span data-ttu-id="b50c8-122">Имя контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="b50c8-122">Specifies the Azure storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b50c8-123">-Контекст</span><span class="sxs-lookup"><span data-stu-id="b50c8-123">-Context</span></span>
<span data-ttu-id="b50c8-124">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="b50c8-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b50c8-125">Для получения контекста хранилища используйте New-AzStorageContext управления.</span><span class="sxs-lookup"><span data-stu-id="b50c8-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b50c8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b50c8-126">-DefaultProfile</span></span>
<span data-ttu-id="b50c8-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b50c8-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b50c8-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="b50c8-128">-ExpiryTime</span></span>
<span data-ttu-id="b50c8-129">Время, в течение которого хранимая политика доступа становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="b50c8-129">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b50c8-130">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="b50c8-130">-NoExpiryTime</span></span>
<span data-ttu-id="b50c8-131">Указывает на то, что срок действия политики доступа не истек.</span><span class="sxs-lookup"><span data-stu-id="b50c8-131">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="b50c8-132">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="b50c8-132">-NoStartTime</span></span>
<span data-ttu-id="b50c8-133">Время начала должно быть $Null.</span><span class="sxs-lookup"><span data-stu-id="b50c8-133">Sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="b50c8-134">-Permission</span><span class="sxs-lookup"><span data-stu-id="b50c8-134">-Permission</span></span>
<span data-ttu-id="b50c8-135">Определяет разрешения в хранимой политике доступа на доступ к контейнеру хранилища.</span><span class="sxs-lookup"><span data-stu-id="b50c8-135">Specifies permissions in the stored access policy to access the storage container.</span></span>
<span data-ttu-id="b50c8-136">Важно отметить, что это строка (для `rwd` чтения, записи и удаления).</span><span class="sxs-lookup"><span data-stu-id="b50c8-136">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b50c8-137">-Политика</span><span class="sxs-lookup"><span data-stu-id="b50c8-137">-Policy</span></span>
<span data-ttu-id="b50c8-138">Указывает имя хранимой политики доступа.</span><span class="sxs-lookup"><span data-stu-id="b50c8-138">Specifies the name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b50c8-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b50c8-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b50c8-140">Указывает интервал времени и времени, в секундах, для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="b50c8-140">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b50c8-141">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="b50c8-141">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b50c8-142">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="b50c8-142">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b50c8-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b50c8-143">-StartTime</span></span>
<span data-ttu-id="b50c8-144">Время, в течение которого хранимая политика доступа становится допустимой.</span><span class="sxs-lookup"><span data-stu-id="b50c8-144">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b50c8-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b50c8-145">-Confirm</span></span>
<span data-ttu-id="b50c8-146">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b50c8-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b50c8-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b50c8-147">-WhatIf</span></span>
<span data-ttu-id="b50c8-148">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b50c8-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b50c8-149">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b50c8-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b50c8-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b50c8-150">CommonParameters</span></span>
<span data-ttu-id="b50c8-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b50c8-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b50c8-152">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b50c8-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b50c8-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b50c8-153">INPUTS</span></span>

### <span data-ttu-id="b50c8-154">System.String</span><span class="sxs-lookup"><span data-stu-id="b50c8-154">System.String</span></span>

### <span data-ttu-id="b50c8-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b50c8-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b50c8-156">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b50c8-156">OUTPUTS</span></span>

### <span data-ttu-id="b50c8-157">System.String</span><span class="sxs-lookup"><span data-stu-id="b50c8-157">System.String</span></span>

## <span data-ttu-id="b50c8-158">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b50c8-158">NOTES</span></span>

## <span data-ttu-id="b50c8-159">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b50c8-159">RELATED LINKS</span></span>

[<span data-ttu-id="b50c8-160">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b50c8-160">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="b50c8-161">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="b50c8-161">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="b50c8-162">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b50c8-162">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="b50c8-163">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b50c8-163">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)
