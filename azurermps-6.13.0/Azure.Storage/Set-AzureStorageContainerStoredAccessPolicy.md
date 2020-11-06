---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 730ECC60-72DE-46DA-A177-D5749F540710
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 6502183d97c92dba864e68942fae214591398f91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558659"
---
# <span data-ttu-id="f2593-101">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f2593-101">Set-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="f2593-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f2593-102">SYNOPSIS</span></span>
<span data-ttu-id="f2593-103">Задает политику сохранения для доступа для контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="f2593-103">Sets a stored access policy for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2593-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f2593-104">SYNTAX</span></span>

```
Set-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f2593-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2593-105">DESCRIPTION</span></span>
<span data-ttu-id="f2593-106">Командлет **Set-AzureStorageContainerStoredAccessPolicy** устанавливает политику доступа для контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="f2593-106">The **Set-AzureStorageContainerStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="f2593-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f2593-107">EXAMPLES</span></span>

### <span data-ttu-id="f2593-108">Пример 1: Настройка политики для сохраненного доступа в контейнере хранилища с полным разрешением</span><span class="sxs-lookup"><span data-stu-id="f2593-108">Example 1: Set a stored access policy in a storage container with full permission</span></span>
```
PS C:\>Set-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy06" -Permission rwdl
```

<span data-ttu-id="f2593-109">Эта команда задает политику доступа с именем Policy06 для контейнера хранилища с именем MyContainer.</span><span class="sxs-lookup"><span data-stu-id="f2593-109">This command sets an access policy named Policy06 for storage container named MyContainer.</span></span>

## <span data-ttu-id="f2593-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f2593-110">PARAMETERS</span></span>

### <span data-ttu-id="f2593-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f2593-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f2593-112">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="f2593-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f2593-113">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="f2593-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f2593-114">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="f2593-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f2593-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f2593-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f2593-116">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="f2593-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="f2593-117">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="f2593-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="f2593-118">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="f2593-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="f2593-119">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="f2593-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="f2593-120">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="f2593-120">The default value is 10.</span></span>

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

### <span data-ttu-id="f2593-121">-Container</span><span class="sxs-lookup"><span data-stu-id="f2593-121">-Container</span></span>
<span data-ttu-id="f2593-122">Указывает имя контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="f2593-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="f2593-123">-Context</span><span class="sxs-lookup"><span data-stu-id="f2593-123">-Context</span></span>
<span data-ttu-id="f2593-124">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="f2593-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f2593-125">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="f2593-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f2593-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2593-126">-DefaultProfile</span></span>
<span data-ttu-id="f2593-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f2593-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2593-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="f2593-128">-ExpiryTime</span></span>
<span data-ttu-id="f2593-129">Указывает время, в течение которого политика хранения сохраненных прав становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="f2593-129">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="f2593-130">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="f2593-130">-NoExpiryTime</span></span>
<span data-ttu-id="f2593-131">Указывает на то, что политика доступа не содержит дату окончания срока действия.</span><span class="sxs-lookup"><span data-stu-id="f2593-131">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="f2593-132">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="f2593-132">-NoStartTime</span></span>
<span data-ttu-id="f2593-133">Задает время начала, которое должно быть $Null.</span><span class="sxs-lookup"><span data-stu-id="f2593-133">Sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="f2593-134">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="f2593-134">-Permission</span></span>
<span data-ttu-id="f2593-135">Определяет разрешения в политике сохранения доступа для доступа к контейнеру хранилища.</span><span class="sxs-lookup"><span data-stu-id="f2593-135">Specifies permissions in the stored access policy to access the storage container.</span></span>
<span data-ttu-id="f2593-136">Важно отметить, что это строка, например `rwd` (для чтения, записи и удаления).</span><span class="sxs-lookup"><span data-stu-id="f2593-136">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="f2593-137">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="f2593-137">-Policy</span></span>
<span data-ttu-id="f2593-138">Задает имя для политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="f2593-138">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="f2593-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f2593-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f2593-140">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="f2593-140">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f2593-141">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="f2593-141">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f2593-142">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="f2593-142">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f2593-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f2593-143">-StartTime</span></span>
<span data-ttu-id="f2593-144">Указывает время вступления в силу политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="f2593-144">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="f2593-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2593-145">-Confirm</span></span>
<span data-ttu-id="f2593-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f2593-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2593-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2593-147">-WhatIf</span></span>
<span data-ttu-id="f2593-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f2593-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f2593-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f2593-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2593-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2593-150">CommonParameters</span></span>
<span data-ttu-id="f2593-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f2593-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2593-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2593-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2593-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f2593-153">INPUTS</span></span>

### <span data-ttu-id="f2593-154">System. String</span><span class="sxs-lookup"><span data-stu-id="f2593-154">System.String</span></span>

### <span data-ttu-id="f2593-155">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f2593-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f2593-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2593-156">OUTPUTS</span></span>

### <span data-ttu-id="f2593-157">System. String</span><span class="sxs-lookup"><span data-stu-id="f2593-157">System.String</span></span>

## <span data-ttu-id="f2593-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="f2593-158">NOTES</span></span>

## <span data-ttu-id="f2593-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f2593-159">RELATED LINKS</span></span>

[<span data-ttu-id="f2593-160">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f2593-160">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="f2593-161">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="f2593-161">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="f2593-162">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f2593-162">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="f2593-163">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f2593-163">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)
