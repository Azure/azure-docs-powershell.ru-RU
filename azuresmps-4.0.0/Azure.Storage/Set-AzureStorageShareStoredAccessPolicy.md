---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C21CC2FA-017E-492E-96E7-B37829917FAF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 86ce98b1ec4d77ffc82ba923b5709321f3b3b546
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556355"
---
# <span data-ttu-id="90599-101">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="90599-101">Set-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="90599-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="90599-102">SYNOPSIS</span></span>
<span data-ttu-id="90599-103">Обновляет политику доступа на общем хранилище.</span><span class="sxs-lookup"><span data-stu-id="90599-103">Updates a stored access policy on a Storage share.</span></span>

## <span data-ttu-id="90599-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="90599-104">SYNTAX</span></span>

```
Set-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90599-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="90599-105">DESCRIPTION</span></span>
<span data-ttu-id="90599-106">Командлет **Set-AzureStorageShareStoredAccessPolicy** обновляет политику сохраненного доступа в общем доступе к хранилищу Azure.</span><span class="sxs-lookup"><span data-stu-id="90599-106">The **Set-AzureStorageShareStoredAccessPolicy** cmdlet updates stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="90599-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="90599-107">EXAMPLES</span></span>

### <span data-ttu-id="90599-108">Пример 1: обновление политики доступа в общей папке хранилища</span><span class="sxs-lookup"><span data-stu-id="90599-108">Example 1: Update a stored access policy in Storage share</span></span>
```
PS C:\>Set-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="90599-109">Эта команда обновляет политику доступа с полным разрешением в общем доступе.</span><span class="sxs-lookup"><span data-stu-id="90599-109">This command updates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="90599-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="90599-110">PARAMETERS</span></span>

### <span data-ttu-id="90599-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="90599-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="90599-112">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="90599-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="90599-113">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="90599-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="90599-114">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="90599-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="90599-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="90599-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="90599-116">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="90599-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="90599-117">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="90599-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="90599-118">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="90599-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="90599-119">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="90599-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="90599-120">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="90599-120">The default value is 10.</span></span>

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

### <span data-ttu-id="90599-121">-Context</span><span class="sxs-lookup"><span data-stu-id="90599-121">-Context</span></span>
<span data-ttu-id="90599-122">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="90599-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="90599-123">Чтобы получить контекст хранения, используйте командлет [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="90599-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="90599-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="90599-124">-ExpiryTime</span></span>
<span data-ttu-id="90599-125">Указывает время, в течение которого политика хранения сохраненных прав становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="90599-125">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="90599-126">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="90599-126">-NoExpiryTime</span></span>
<span data-ttu-id="90599-127">Указывает на то, что этот командлет очищает свойство **ExpiryTime** в политике сохраненного доступа.</span><span class="sxs-lookup"><span data-stu-id="90599-127">Indicates that this cmdlet clears the **ExpiryTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="90599-128">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="90599-128">-NoStartTime</span></span>
<span data-ttu-id="90599-129">Указывает на то, что этот командлет очищает свойство **StartTime** в политике сохраненного доступа.</span><span class="sxs-lookup"><span data-stu-id="90599-129">Indicates that this cmdlet clears the **StartTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="90599-130">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="90599-130">-Permission</span></span>
<span data-ttu-id="90599-131">Определяет разрешения в политике сохранения доступа, чтобы получить доступ к общему доступу и файлам.</span><span class="sxs-lookup"><span data-stu-id="90599-131">Specifies permissions in the stored access policy to access the share or files under it.</span></span>

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

### <span data-ttu-id="90599-132">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="90599-132">-Policy</span></span>
<span data-ttu-id="90599-133">Задает имя для политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="90599-133">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="90599-134">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="90599-134">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="90599-135">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="90599-135">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="90599-136">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="90599-136">-ShareName</span></span>
<span data-ttu-id="90599-137">Указывает имя общего доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="90599-137">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="90599-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="90599-138">-StartTime</span></span>
<span data-ttu-id="90599-139">Указывает время вступления в силу политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="90599-139">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="90599-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="90599-140">-Confirm</span></span>
<span data-ttu-id="90599-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="90599-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90599-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90599-142">-WhatIf</span></span>
<span data-ttu-id="90599-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="90599-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90599-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="90599-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90599-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90599-145">CommonParameters</span></span>
<span data-ttu-id="90599-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="90599-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90599-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90599-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90599-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="90599-148">INPUTS</span></span>

## <span data-ttu-id="90599-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="90599-149">OUTPUTS</span></span>

## <span data-ttu-id="90599-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="90599-150">NOTES</span></span>

## <span data-ttu-id="90599-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="90599-151">RELATED LINKS</span></span>

[<span data-ttu-id="90599-152">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="90599-152">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="90599-153">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="90599-153">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="90599-154">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="90599-154">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="90599-155">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="90599-155">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)
