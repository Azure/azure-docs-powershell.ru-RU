---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C21CC2FA-017E-492E-96E7-B37829917FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 5159e09d4e56b45e9b7ce61bae3e9d8e5fd115c6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419972"
---
# <span data-ttu-id="3b0a0-101">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3b0a0-101">Set-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="3b0a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b0a0-102">SYNOPSIS</span></span>
<span data-ttu-id="3b0a0-103">Обновляет хранимую политику доступа для хранилища.</span><span class="sxs-lookup"><span data-stu-id="3b0a0-103">Updates a stored access policy on a Storage share.</span></span>

## <span data-ttu-id="3b0a0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3b0a0-104">SYNTAX</span></span>

```
Set-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3b0a0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b0a0-105">DESCRIPTION</span></span>
<span data-ttu-id="3b0a0-106">При обновлении политики доступа для хранилища Azure обновляется политика доступа для **cmdlet Set-AzStorageShareStoredAccessPolicy.**</span><span class="sxs-lookup"><span data-stu-id="3b0a0-106">The **Set-AzStorageShareStoredAccessPolicy** cmdlet updates stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="3b0a0-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3b0a0-107">EXAMPLES</span></span>

### <span data-ttu-id="3b0a0-108">Пример 1. Обновление политики хранимого доступа в области хранилища</span><span class="sxs-lookup"><span data-stu-id="3b0a0-108">Example 1: Update a stored access policy in Storage share</span></span>
```
PS C:\>Set-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="3b0a0-109">Эта команда обновляет хранимую политику доступа с полными разрешениями на доступ.</span><span class="sxs-lookup"><span data-stu-id="3b0a0-109">This command updates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="3b0a0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b0a0-110">PARAMETERS</span></span>

### <span data-ttu-id="3b0a0-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3b0a0-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3b0a0-112">Указывает интервал времени и времени, в секундах, для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="3b0a0-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3b0a0-113">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="3b0a0-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3b0a0-114">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="3b0a0-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="3b0a0-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3b0a0-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3b0a0-116">Указывает максимальное число сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="3b0a0-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="3b0a0-117">С помощью этого параметра можно ограничить одновременное использование локального ЦП и пропускной способности, указав максимальное количество сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="3b0a0-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="3b0a0-118">Указанное значение является абсолютным и не умножается на основное.</span><span class="sxs-lookup"><span data-stu-id="3b0a0-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="3b0a0-119">Этот параметр помогает уменьшить количество проблем с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.</span><span class="sxs-lookup"><span data-stu-id="3b0a0-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="3b0a0-120">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="3b0a0-120">The default value is 10.</span></span>

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

### <span data-ttu-id="3b0a0-121">-Контекст</span><span class="sxs-lookup"><span data-stu-id="3b0a0-121">-Context</span></span>
<span data-ttu-id="3b0a0-122">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="3b0a0-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3b0a0-123">Чтобы получить контекст хранилища, воспользуйтесь [cmdlet New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="3b0a0-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="3b0a0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b0a0-124">-DefaultProfile</span></span>
<span data-ttu-id="3b0a0-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3b0a0-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b0a0-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="3b0a0-126">-ExpiryTime</span></span>
<span data-ttu-id="3b0a0-127">Время, в течение которого хранимая политика доступа становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="3b0a0-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="3b0a0-128">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="3b0a0-128">-NoExpiryTime</span></span>
<span data-ttu-id="3b0a0-129">Указывает на то, что этот cmdlet очищает свойство **ExpiryTime** в политике хранимого доступа.</span><span class="sxs-lookup"><span data-stu-id="3b0a0-129">Indicates that this cmdlet clears the **ExpiryTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="3b0a0-130">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="3b0a0-130">-NoStartTime</span></span>
<span data-ttu-id="3b0a0-131">Указывает на то, что этот cmdlet очищает свойство **StartTime** в политике хранимого доступа.</span><span class="sxs-lookup"><span data-stu-id="3b0a0-131">Indicates that this cmdlet clears the **StartTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="3b0a0-132">-Permission</span><span class="sxs-lookup"><span data-stu-id="3b0a0-132">-Permission</span></span>
<span data-ttu-id="3b0a0-133">Определяет разрешения в хранимой политике доступа на доступ к папке или файлам в ней.</span><span class="sxs-lookup"><span data-stu-id="3b0a0-133">Specifies permissions in the stored access policy to access the share or files under it.</span></span>
<span data-ttu-id="3b0a0-134">Важно отметить, что это строка (для `rwd` чтения, записи и удаления).</span><span class="sxs-lookup"><span data-stu-id="3b0a0-134">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="3b0a0-135">-Политика</span><span class="sxs-lookup"><span data-stu-id="3b0a0-135">-Policy</span></span>
<span data-ttu-id="3b0a0-136">Указывает имя хранимой политики доступа.</span><span class="sxs-lookup"><span data-stu-id="3b0a0-136">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="3b0a0-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3b0a0-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3b0a0-138">Определяет продолжительность периода времени ожидания для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="3b0a0-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="3b0a0-139">-ShareName</span><span class="sxs-lookup"><span data-stu-id="3b0a0-139">-ShareName</span></span>
<span data-ttu-id="3b0a0-140">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="3b0a0-140">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="3b0a0-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3b0a0-141">-StartTime</span></span>
<span data-ttu-id="3b0a0-142">Время, в течение которого хранимая политика доступа становится допустимой.</span><span class="sxs-lookup"><span data-stu-id="3b0a0-142">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="3b0a0-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b0a0-143">-Confirm</span></span>
<span data-ttu-id="3b0a0-144">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b0a0-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b0a0-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b0a0-145">-WhatIf</span></span>
<span data-ttu-id="3b0a0-146">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b0a0-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3b0a0-147">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3b0a0-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b0a0-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b0a0-148">CommonParameters</span></span>
<span data-ttu-id="3b0a0-149">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b0a0-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b0a0-150">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b0a0-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b0a0-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3b0a0-151">INPUTS</span></span>

### <span data-ttu-id="3b0a0-152">System.String</span><span class="sxs-lookup"><span data-stu-id="3b0a0-152">System.String</span></span>

### <span data-ttu-id="3b0a0-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3b0a0-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3b0a0-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3b0a0-154">OUTPUTS</span></span>

### <span data-ttu-id="3b0a0-155">System.String</span><span class="sxs-lookup"><span data-stu-id="3b0a0-155">System.String</span></span>

## <span data-ttu-id="3b0a0-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3b0a0-156">NOTES</span></span>

## <span data-ttu-id="3b0a0-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3b0a0-157">RELATED LINKS</span></span>

[<span data-ttu-id="3b0a0-158">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3b0a0-158">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="3b0a0-159">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="3b0a0-159">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="3b0a0-160">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3b0a0-160">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="3b0a0-161">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3b0a0-161">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)
