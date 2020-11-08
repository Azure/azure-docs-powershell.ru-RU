---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C21CC2FA-017E-492E-96E7-B37829917FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 5159e09d4e56b45e9b7ce61bae3e9d8e5fd115c6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245757"
---
# <span data-ttu-id="a0f51-101">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a0f51-101">Set-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="a0f51-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a0f51-102">SYNOPSIS</span></span>
<span data-ttu-id="a0f51-103">Обновляет политику доступа на общем хранилище.</span><span class="sxs-lookup"><span data-stu-id="a0f51-103">Updates a stored access policy on a Storage share.</span></span>

## <span data-ttu-id="a0f51-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a0f51-104">SYNTAX</span></span>

```
Set-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a0f51-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0f51-105">DESCRIPTION</span></span>
<span data-ttu-id="a0f51-106">Командлет **Set-AzStorageShareStoredAccessPolicy** обновляет политику сохраненного доступа в общем доступе к хранилищу Azure.</span><span class="sxs-lookup"><span data-stu-id="a0f51-106">The **Set-AzStorageShareStoredAccessPolicy** cmdlet updates stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="a0f51-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a0f51-107">EXAMPLES</span></span>

### <span data-ttu-id="a0f51-108">Пример 1: обновление политики доступа в общей папке хранилища</span><span class="sxs-lookup"><span data-stu-id="a0f51-108">Example 1: Update a stored access policy in Storage share</span></span>
```
PS C:\>Set-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="a0f51-109">Эта команда обновляет политику доступа с полным разрешением в общем доступе.</span><span class="sxs-lookup"><span data-stu-id="a0f51-109">This command updates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="a0f51-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a0f51-110">PARAMETERS</span></span>

### <span data-ttu-id="a0f51-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a0f51-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a0f51-112">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="a0f51-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a0f51-113">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="a0f51-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a0f51-114">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="a0f51-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a0f51-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a0f51-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a0f51-116">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="a0f51-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a0f51-117">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="a0f51-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a0f51-118">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="a0f51-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a0f51-119">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="a0f51-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a0f51-120">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="a0f51-120">The default value is 10.</span></span>

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

### <span data-ttu-id="a0f51-121">-Context</span><span class="sxs-lookup"><span data-stu-id="a0f51-121">-Context</span></span>
<span data-ttu-id="a0f51-122">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="a0f51-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a0f51-123">Чтобы получить контекст хранения, используйте командлет [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="a0f51-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="a0f51-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0f51-124">-DefaultProfile</span></span>
<span data-ttu-id="a0f51-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a0f51-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0f51-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="a0f51-126">-ExpiryTime</span></span>
<span data-ttu-id="a0f51-127">Указывает время, в течение которого политика хранения сохраненных прав становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="a0f51-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="a0f51-128">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="a0f51-128">-NoExpiryTime</span></span>
<span data-ttu-id="a0f51-129">Указывает на то, что этот командлет очищает свойство **ExpiryTime** в политике сохраненного доступа.</span><span class="sxs-lookup"><span data-stu-id="a0f51-129">Indicates that this cmdlet clears the **ExpiryTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="a0f51-130">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="a0f51-130">-NoStartTime</span></span>
<span data-ttu-id="a0f51-131">Указывает на то, что этот командлет очищает свойство **StartTime** в политике сохраненного доступа.</span><span class="sxs-lookup"><span data-stu-id="a0f51-131">Indicates that this cmdlet clears the **StartTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="a0f51-132">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="a0f51-132">-Permission</span></span>
<span data-ttu-id="a0f51-133">Определяет разрешения в политике сохранения доступа, чтобы получить доступ к общему доступу и файлам.</span><span class="sxs-lookup"><span data-stu-id="a0f51-133">Specifies permissions in the stored access policy to access the share or files under it.</span></span>
<span data-ttu-id="a0f51-134">Важно отметить, что это строка, например `rwd` (для чтения, записи и удаления).</span><span class="sxs-lookup"><span data-stu-id="a0f51-134">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="a0f51-135">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="a0f51-135">-Policy</span></span>
<span data-ttu-id="a0f51-136">Задает имя для политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="a0f51-136">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="a0f51-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a0f51-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a0f51-138">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="a0f51-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="a0f51-139">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="a0f51-139">-ShareName</span></span>
<span data-ttu-id="a0f51-140">Указывает имя общего доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="a0f51-140">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="a0f51-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="a0f51-141">-StartTime</span></span>
<span data-ttu-id="a0f51-142">Указывает время вступления в силу политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="a0f51-142">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="a0f51-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a0f51-143">-Confirm</span></span>
<span data-ttu-id="a0f51-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a0f51-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0f51-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0f51-145">-WhatIf</span></span>
<span data-ttu-id="a0f51-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a0f51-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0f51-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a0f51-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0f51-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0f51-148">CommonParameters</span></span>
<span data-ttu-id="a0f51-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a0f51-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0f51-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0f51-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0f51-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a0f51-151">INPUTS</span></span>

### <span data-ttu-id="a0f51-152">System. String</span><span class="sxs-lookup"><span data-stu-id="a0f51-152">System.String</span></span>

### <span data-ttu-id="a0f51-153">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a0f51-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a0f51-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0f51-154">OUTPUTS</span></span>

### <span data-ttu-id="a0f51-155">System. String</span><span class="sxs-lookup"><span data-stu-id="a0f51-155">System.String</span></span>

## <span data-ttu-id="a0f51-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="a0f51-156">NOTES</span></span>

## <span data-ttu-id="a0f51-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a0f51-157">RELATED LINKS</span></span>

[<span data-ttu-id="a0f51-158">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a0f51-158">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="a0f51-159">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a0f51-159">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="a0f51-160">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a0f51-160">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="a0f51-161">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a0f51-161">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)
