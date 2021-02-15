---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E2CCDA8F-2D45-4F25-B297-337B7AB021E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: d8c9e0e49ba7a5caa9cb93290ef5e96b60fd4430
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100224820"
---
# <span data-ttu-id="d40dc-101">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d40dc-101">Remove-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="d40dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d40dc-102">SYNOPSIS</span></span>
<span data-ttu-id="d40dc-103">Удаляет хранимую политику доступа из хранилища.</span><span class="sxs-lookup"><span data-stu-id="d40dc-103">Removes a stored access policy from a Storage share.</span></span>

## <span data-ttu-id="d40dc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d40dc-104">SYNTAX</span></span>

```
Remove-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d40dc-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d40dc-105">DESCRIPTION</span></span>
<span data-ttu-id="d40dc-106">С **его использованием** из хранилища Azure удаляется политика доступа, хранимая в хранилище Azure.</span><span class="sxs-lookup"><span data-stu-id="d40dc-106">The **Remove-AzStorageShareStoredAccessPolicy** cmdlet removes a stored access policy from an Azure Storage share.</span></span>

## <span data-ttu-id="d40dc-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d40dc-107">EXAMPLES</span></span>

### <span data-ttu-id="d40dc-108">Пример 1. Удаление хранимой политики доступа из хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="d40dc-108">Example 1: Remove a stored access policy from an Azure Storage share</span></span>
```
PS C:\>Remove-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="d40dc-109">Эта команда удаляет из ContosoShare хранимую политику доступа с именем GeneralPolicy.</span><span class="sxs-lookup"><span data-stu-id="d40dc-109">This command removes a stored access policy named GeneralPolicy from ContosoShare.</span></span>

## <span data-ttu-id="d40dc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d40dc-110">PARAMETERS</span></span>

### <span data-ttu-id="d40dc-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d40dc-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d40dc-112">Указывает интервал времени и времени, в секундах, для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="d40dc-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d40dc-113">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="d40dc-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d40dc-114">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="d40dc-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d40dc-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d40dc-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d40dc-116">Указывает максимальное число сетевых звонков.</span><span class="sxs-lookup"><span data-stu-id="d40dc-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d40dc-117">С помощью этого параметра можно ограничить одновременное использование локального ЦП и пропускной способности, указав максимальное количество сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="d40dc-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d40dc-118">Указанное значение является абсолютным и не умножается на основное.</span><span class="sxs-lookup"><span data-stu-id="d40dc-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d40dc-119">Этот параметр помогает уменьшить количество проблем с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.</span><span class="sxs-lookup"><span data-stu-id="d40dc-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d40dc-120">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="d40dc-120">The default value is 10.</span></span>

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

### <span data-ttu-id="d40dc-121">-Контекст</span><span class="sxs-lookup"><span data-stu-id="d40dc-121">-Context</span></span>
<span data-ttu-id="d40dc-122">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="d40dc-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d40dc-123">Чтобы получить контекст хранилища, воспользуйтесь [cmdlet New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="d40dc-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="d40dc-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d40dc-124">-DefaultProfile</span></span>
<span data-ttu-id="d40dc-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d40dc-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d40dc-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d40dc-126">-PassThru</span></span>
<span data-ttu-id="d40dc-127">Указывает на то, что этот cmdlet возвращает **boolean,** который отражает успешность операции.</span><span class="sxs-lookup"><span data-stu-id="d40dc-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="d40dc-128">По умолчанию этот cmdlet не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d40dc-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="d40dc-129">-Политика</span><span class="sxs-lookup"><span data-stu-id="d40dc-129">-Policy</span></span>
<span data-ttu-id="d40dc-130">Указывает имя хранимой политики доступа, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d40dc-130">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d40dc-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d40dc-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d40dc-132">Определяет продолжительность периода времени ожидания для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="d40dc-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="d40dc-133">-ShareName</span><span class="sxs-lookup"><span data-stu-id="d40dc-133">-ShareName</span></span>
<span data-ttu-id="d40dc-134">Имя хранилища, для которого этот cmdlet удаляет политику.</span><span class="sxs-lookup"><span data-stu-id="d40dc-134">Specifies the Storage share name for which this cmdlet removes a policy.</span></span>

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

### <span data-ttu-id="d40dc-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d40dc-135">-Confirm</span></span>
<span data-ttu-id="d40dc-136">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d40dc-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d40dc-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d40dc-137">-WhatIf</span></span>
<span data-ttu-id="d40dc-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d40dc-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d40dc-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d40dc-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d40dc-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d40dc-140">CommonParameters</span></span>
<span data-ttu-id="d40dc-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d40dc-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d40dc-142">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d40dc-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d40dc-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d40dc-143">INPUTS</span></span>

### <span data-ttu-id="d40dc-144">System.String</span><span class="sxs-lookup"><span data-stu-id="d40dc-144">System.String</span></span>

### <span data-ttu-id="d40dc-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d40dc-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d40dc-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d40dc-146">OUTPUTS</span></span>

### <span data-ttu-id="d40dc-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d40dc-147">System.Boolean</span></span>

## <span data-ttu-id="d40dc-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d40dc-148">NOTES</span></span>

## <span data-ttu-id="d40dc-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d40dc-149">RELATED LINKS</span></span>

[<span data-ttu-id="d40dc-150">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d40dc-150">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="d40dc-151">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d40dc-151">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="d40dc-152">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d40dc-152">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="d40dc-153">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d40dc-153">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)
