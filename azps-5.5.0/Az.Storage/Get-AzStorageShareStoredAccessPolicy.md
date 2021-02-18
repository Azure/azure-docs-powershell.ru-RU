---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 73BB521B-20F2-4F2B-AA88-2B128F36A9EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 2e444fba12f0ffebfd3d6679293cac31fc574e93
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100224956"
---
# <span data-ttu-id="588bc-101">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="588bc-101">Get-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="588bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="588bc-102">SYNOPSIS</span></span>
<span data-ttu-id="588bc-103">Сохраняет политики доступа для хранилища.</span><span class="sxs-lookup"><span data-stu-id="588bc-103">Gets stored access policies for a Storage share.</span></span>

## <span data-ttu-id="588bc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="588bc-104">SYNTAX</span></span>

```
Get-AzStorageShareStoredAccessPolicy [-ShareName] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="588bc-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="588bc-105">DESCRIPTION</span></span>
<span data-ttu-id="588bc-106">Для share Storage Share Azure сохраняются политики доступа для **cmdlet Get-AzStorageShareStoredAccessPolicy.**</span><span class="sxs-lookup"><span data-stu-id="588bc-106">The **Get-AzStorageShareStoredAccessPolicy** cmdlet gets stored access policies for an Azure Storage share.</span></span>
<span data-ttu-id="588bc-107">Чтобы получить определенную политику, укажите ее по имени.</span><span class="sxs-lookup"><span data-stu-id="588bc-107">To get a particular policy, specify it by name.</span></span>

## <span data-ttu-id="588bc-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="588bc-108">EXAMPLES</span></span>

### <span data-ttu-id="588bc-109">Пример 1. Получить хранимую политику доступа в обет</span><span class="sxs-lookup"><span data-stu-id="588bc-109">Example 1: Get a stored access policy in a share</span></span>
```
PS C:\>Get-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="588bc-110">Эта команда получает хранимую политику доступа с именем GeneralPolicy в ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="588bc-110">This command gets a stored access policy named GeneralPolicy in ContosoShare.</span></span>

### <span data-ttu-id="588bc-111">Пример 2. Все хранимые политики доступа</span><span class="sxs-lookup"><span data-stu-id="588bc-111">Example 2: Get all the stored access policies in share</span></span>
```
PS C:\>Get-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare"
```

<span data-ttu-id="588bc-112">Эта команда получает все хранимые политики доступа в ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="588bc-112">This command gets all stored access policies in ContosoShare.</span></span>

## <span data-ttu-id="588bc-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="588bc-113">PARAMETERS</span></span>

### <span data-ttu-id="588bc-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="588bc-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="588bc-115">Указывает интервал времени и времени, в секундах, для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="588bc-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="588bc-116">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="588bc-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="588bc-117">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="588bc-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="588bc-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="588bc-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="588bc-119">Указывает максимальное число сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="588bc-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="588bc-120">С помощью этого параметра можно ограничить одновременное использование локального ЦП и пропускной способности, указав максимальное количество сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="588bc-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="588bc-121">Указанное значение является абсолютным и не умножается на основное.</span><span class="sxs-lookup"><span data-stu-id="588bc-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="588bc-122">Этот параметр помогает уменьшить количество проблем с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.</span><span class="sxs-lookup"><span data-stu-id="588bc-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="588bc-123">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="588bc-123">The default value is 10.</span></span>

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

### <span data-ttu-id="588bc-124">-Контекст</span><span class="sxs-lookup"><span data-stu-id="588bc-124">-Context</span></span>
<span data-ttu-id="588bc-125">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="588bc-125">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="588bc-126">Для получения контекста используйте [cmdlet New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="588bc-126">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="588bc-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="588bc-127">-DefaultProfile</span></span>
<span data-ttu-id="588bc-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="588bc-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="588bc-129">-Политика</span><span class="sxs-lookup"><span data-stu-id="588bc-129">-Policy</span></span>
<span data-ttu-id="588bc-130">Указывает имя хранимой политики доступа, которая получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="588bc-130">Specifies the name of the stored access policy that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="588bc-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="588bc-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="588bc-132">Определяет продолжительность периода времени ожидания для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="588bc-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="588bc-133">-ShareName</span><span class="sxs-lookup"><span data-stu-id="588bc-133">-ShareName</span></span>
<span data-ttu-id="588bc-134">Указывает имя хранилища, для которого этот cmdlet получает политики.</span><span class="sxs-lookup"><span data-stu-id="588bc-134">Specifies the Storage share name for which this cmdlet gets policies.</span></span>

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

### <span data-ttu-id="588bc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="588bc-135">CommonParameters</span></span>
<span data-ttu-id="588bc-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="588bc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="588bc-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="588bc-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="588bc-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="588bc-138">INPUTS</span></span>

### <span data-ttu-id="588bc-139">System.String</span><span class="sxs-lookup"><span data-stu-id="588bc-139">System.String</span></span>

### <span data-ttu-id="588bc-140">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="588bc-140">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="588bc-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="588bc-141">OUTPUTS</span></span>

### <span data-ttu-id="588bc-142">Microsoft.Azure.Storage.File.SharedAccessFilePolicy</span><span class="sxs-lookup"><span data-stu-id="588bc-142">Microsoft.Azure.Storage.File.SharedAccessFilePolicy</span></span>

## <span data-ttu-id="588bc-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="588bc-143">NOTES</span></span>

## <span data-ttu-id="588bc-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="588bc-144">RELATED LINKS</span></span>

[<span data-ttu-id="588bc-145">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="588bc-145">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="588bc-146">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="588bc-146">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="588bc-147">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="588bc-147">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="588bc-148">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="588bc-148">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)
