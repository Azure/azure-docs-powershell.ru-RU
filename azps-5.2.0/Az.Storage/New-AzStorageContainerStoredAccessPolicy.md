---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C324F28A-7215-4F10-A012-92B4F6544BC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: eb51b8c4e33f45d637354f85be049295626afdd6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324775"
---
# <span data-ttu-id="28679-101">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="28679-101">New-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="28679-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28679-102">SYNOPSIS</span></span>
<span data-ttu-id="28679-103">Создает политику хранимого доступа для контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="28679-103">Creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="28679-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="28679-104">SYNTAX</span></span>

```
New-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="28679-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="28679-105">DESCRIPTION</span></span>
<span data-ttu-id="28679-106">Для контейнера хранилища Azure создается политика доступа **New-AzStorageContainerStoredAccessPolicy.**</span><span class="sxs-lookup"><span data-stu-id="28679-106">The **New-AzStorageContainerStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="28679-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="28679-107">EXAMPLES</span></span>

### <span data-ttu-id="28679-108">Пример 1. Создание политики хранимого доступа в контейнере хранилища</span><span class="sxs-lookup"><span data-stu-id="28679-108">Example 1: Create a stored access policy in a storage container</span></span>
```
PS C:\>New-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy01"
```

<span data-ttu-id="28679-109">Эта команда создает политику доступа с именем Policy01 в контейнере хранилища MyContainer.</span><span class="sxs-lookup"><span data-stu-id="28679-109">This command creates an access policy named Policy01 in the storage container named MyContainer.</span></span>

## <span data-ttu-id="28679-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28679-110">PARAMETERS</span></span>

### <span data-ttu-id="28679-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="28679-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="28679-112">Указывает интервал времени и времени, в секундах, для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="28679-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="28679-113">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="28679-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="28679-114">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="28679-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="28679-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="28679-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="28679-116">Указывает максимальное число сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="28679-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="28679-117">С помощью этого параметра можно ограничить одновременное использование локального ЦП и пропускной способности, указав максимальное количество сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="28679-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="28679-118">Указанное значение является абсолютным и не умножается на основное.</span><span class="sxs-lookup"><span data-stu-id="28679-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="28679-119">Этот параметр помогает уменьшить количество проблем с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.</span><span class="sxs-lookup"><span data-stu-id="28679-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="28679-120">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="28679-120">The default value is 10.</span></span>

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

### <span data-ttu-id="28679-121">-Container</span><span class="sxs-lookup"><span data-stu-id="28679-121">-Container</span></span>
<span data-ttu-id="28679-122">Имя контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="28679-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="28679-123">-Контекст</span><span class="sxs-lookup"><span data-stu-id="28679-123">-Context</span></span>
<span data-ttu-id="28679-124">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="28679-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="28679-125">Для получения контекста хранилища используйте New-AzStorageContext управления.</span><span class="sxs-lookup"><span data-stu-id="28679-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="28679-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28679-126">-DefaultProfile</span></span>
<span data-ttu-id="28679-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="28679-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28679-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="28679-128">-ExpiryTime</span></span>
<span data-ttu-id="28679-129">Время, в течение которого хранимая политика доступа становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="28679-129">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="28679-130">-Permission</span><span class="sxs-lookup"><span data-stu-id="28679-130">-Permission</span></span>
<span data-ttu-id="28679-131">Определяет разрешения в хранимой политике доступа на доступ к контейнеру.</span><span class="sxs-lookup"><span data-stu-id="28679-131">Specifies permissions in the stored access policy to access the container.</span></span>
<span data-ttu-id="28679-132">Важно отметить, что это строка (для `rwd` чтения, записи и удаления).</span><span class="sxs-lookup"><span data-stu-id="28679-132">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="28679-133">-Политика</span><span class="sxs-lookup"><span data-stu-id="28679-133">-Policy</span></span>
<span data-ttu-id="28679-134">Определяет хранимую политику доступа, которая включает разрешения для этого токена SAS.</span><span class="sxs-lookup"><span data-stu-id="28679-134">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="28679-135">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="28679-135">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="28679-136">Указывает интервал времени и времени, в секундах, для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="28679-136">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="28679-137">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="28679-137">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="28679-138">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="28679-138">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="28679-139">-StartTime</span><span class="sxs-lookup"><span data-stu-id="28679-139">-StartTime</span></span>
<span data-ttu-id="28679-140">Время, в течение которого хранимая политика доступа становится допустимой.</span><span class="sxs-lookup"><span data-stu-id="28679-140">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="28679-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28679-141">CommonParameters</span></span>
<span data-ttu-id="28679-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28679-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28679-143">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28679-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28679-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="28679-144">INPUTS</span></span>

### <span data-ttu-id="28679-145">System.String</span><span class="sxs-lookup"><span data-stu-id="28679-145">System.String</span></span>

### <span data-ttu-id="28679-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="28679-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="28679-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="28679-147">OUTPUTS</span></span>

### <span data-ttu-id="28679-148">System.String</span><span class="sxs-lookup"><span data-stu-id="28679-148">System.String</span></span>

## <span data-ttu-id="28679-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="28679-149">NOTES</span></span>

## <span data-ttu-id="28679-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="28679-150">RELATED LINKS</span></span>

[<span data-ttu-id="28679-151">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="28679-151">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="28679-152">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="28679-152">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="28679-153">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="28679-153">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="28679-154">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="28679-154">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)


