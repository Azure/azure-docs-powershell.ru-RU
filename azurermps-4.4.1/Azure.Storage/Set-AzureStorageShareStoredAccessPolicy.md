---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C21CC2FA-017E-492E-96E7-B37829917FAF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageShareStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 43e9ccca185a68d3c7b0e6cca118bb2cd63247bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568365"
---
# <span data-ttu-id="bf018-101">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bf018-101">Set-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="bf018-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bf018-102">SYNOPSIS</span></span>
<span data-ttu-id="bf018-103">Обновляет политику доступа на общем хранилище.</span><span class="sxs-lookup"><span data-stu-id="bf018-103">Updates a stored access policy on a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf018-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bf018-104">SYNTAX</span></span>

```
Set-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf018-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf018-105">DESCRIPTION</span></span>
<span data-ttu-id="bf018-106">Командлет **Set-AzureStorageShareStoredAccessPolicy** обновляет политику сохраненного доступа в общем доступе к хранилищу Azure.</span><span class="sxs-lookup"><span data-stu-id="bf018-106">The **Set-AzureStorageShareStoredAccessPolicy** cmdlet updates stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="bf018-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bf018-107">EXAMPLES</span></span>

### <span data-ttu-id="bf018-108">Пример 1: обновление политики доступа в общей папке хранилища</span><span class="sxs-lookup"><span data-stu-id="bf018-108">Example 1: Update a stored access policy in Storage share</span></span>
```
PS C:\>Set-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="bf018-109">Эта команда обновляет политику доступа с полным разрешением в общем доступе.</span><span class="sxs-lookup"><span data-stu-id="bf018-109">This command updates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="bf018-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bf018-110">PARAMETERS</span></span>

### <span data-ttu-id="bf018-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bf018-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="bf018-112">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="bf018-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="bf018-113">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="bf018-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="bf018-114">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="bf018-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="bf018-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="bf018-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="bf018-116">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="bf018-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="bf018-117">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="bf018-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="bf018-118">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="bf018-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="bf018-119">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="bf018-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="bf018-120">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="bf018-120">The default value is 10.</span></span>

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

### <span data-ttu-id="bf018-121">-Context</span><span class="sxs-lookup"><span data-stu-id="bf018-121">-Context</span></span>
<span data-ttu-id="bf018-122">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="bf018-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="bf018-123">Чтобы получить контекст хранения, используйте командлет [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="bf018-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="bf018-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="bf018-124">-ExpiryTime</span></span>
<span data-ttu-id="bf018-125">Указывает время, в течение которого политика хранения сохраненных прав становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="bf018-125">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf018-126">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="bf018-126">-NoExpiryTime</span></span>
<span data-ttu-id="bf018-127">Указывает на то, что этот командлет очищает свойство **ExpiryTime** в политике сохраненного доступа.</span><span class="sxs-lookup"><span data-stu-id="bf018-127">Indicates that this cmdlet clears the **ExpiryTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="bf018-128">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="bf018-128">-NoStartTime</span></span>
<span data-ttu-id="bf018-129">Указывает на то, что этот командлет очищает свойство **StartTime** в политике сохраненного доступа.</span><span class="sxs-lookup"><span data-stu-id="bf018-129">Indicates that this cmdlet clears the **StartTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="bf018-130">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="bf018-130">-Permission</span></span>
<span data-ttu-id="bf018-131">Определяет разрешения в политике сохранения доступа, чтобы получить доступ к общему доступу и файлам.</span><span class="sxs-lookup"><span data-stu-id="bf018-131">Specifies permissions in the stored access policy to access the share or files under it.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf018-132">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="bf018-132">-Policy</span></span>
<span data-ttu-id="bf018-133">Задает имя для политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="bf018-133">Specifies a name for the stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf018-134">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bf018-134">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="bf018-135">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="bf018-135">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="bf018-136">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="bf018-136">-ShareName</span></span>
<span data-ttu-id="bf018-137">Указывает имя общего доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="bf018-137">Specifies the name of the Storage share.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf018-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="bf018-138">-StartTime</span></span>
<span data-ttu-id="bf018-139">Указывает время вступления в силу политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="bf018-139">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf018-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bf018-140">-Confirm</span></span>
<span data-ttu-id="bf018-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bf018-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf018-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf018-142">-WhatIf</span></span>
<span data-ttu-id="bf018-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bf018-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bf018-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bf018-144">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf018-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf018-145">CommonParameters</span></span>
<span data-ttu-id="bf018-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bf018-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf018-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf018-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf018-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bf018-148">INPUTS</span></span>

### <span data-ttu-id="bf018-149">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="bf018-149">IStorageContext</span></span>

<span data-ttu-id="bf018-150">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="bf018-150">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="bf018-151">Подстрок</span><span class="sxs-lookup"><span data-stu-id="bf018-151">String</span></span>

<span data-ttu-id="bf018-152">Параметр ShareName принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="bf018-152">Parameter 'ShareName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="bf018-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf018-153">OUTPUTS</span></span>

### <span data-ttu-id="bf018-154">System. String</span><span class="sxs-lookup"><span data-stu-id="bf018-154">System.String</span></span>

## <span data-ttu-id="bf018-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="bf018-155">NOTES</span></span>

## <span data-ttu-id="bf018-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bf018-156">RELATED LINKS</span></span>

[<span data-ttu-id="bf018-157">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bf018-157">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="bf018-158">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="bf018-158">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="bf018-159">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bf018-159">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="bf018-160">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bf018-160">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)
