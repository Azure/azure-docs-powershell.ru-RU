---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 10D5B7E0-242B-4DC0-A527-8F6388E72E0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 5a0f976d561396bc93facfeedcbb1c89c768e5b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100212273"
---
# <span data-ttu-id="7a71c-101">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7a71c-101">Get-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="7a71c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a71c-102">SYNOPSIS</span></span>
<span data-ttu-id="7a71c-103">Возвращает хранимую политику доступа или политики для контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7a71c-103">Gets the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="7a71c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7a71c-104">SYNTAX</span></span>

```
Get-AzStorageContainerStoredAccessPolicy [-Container] <String> [[-Policy] <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="7a71c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a71c-105">DESCRIPTION</span></span>
<span data-ttu-id="7a71c-106">Для контейнера хранилища Azure с его учетом вы можете получить список политик доступа и политик **доступа Get-AzStorageContainerStoredAccessPolicy.**</span><span class="sxs-lookup"><span data-stu-id="7a71c-106">The **Get-AzStorageContainerStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="7a71c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7a71c-107">EXAMPLES</span></span>

### <span data-ttu-id="7a71c-108">Пример 1. Хранение политики доступа в контейнере хранилища</span><span class="sxs-lookup"><span data-stu-id="7a71c-108">Example 1: Get a stored access policy in a storage container</span></span>
```
PS C:\>Get-AzStorageContainerStoredAccessPolicy -Container "Container07" -Policy "Policy22"
```

<span data-ttu-id="7a71c-109">Эта команда получает политику доступа "Политика22" в контейнере хранения Container07.</span><span class="sxs-lookup"><span data-stu-id="7a71c-109">This command gets the access policy named Policy22 in the storage container named Container07.</span></span>

### <span data-ttu-id="7a71c-110">Пример 2. Все хранимые политики доступа в контейнере хранилища</span><span class="sxs-lookup"><span data-stu-id="7a71c-110">Example 2: Get all the stored access policies in a storage container</span></span>
```
PS C:\>Get-AzStorageContainerStoredAccessPolicy -Container "Container07"
```

<span data-ttu-id="7a71c-111">Эта команда получает все политики доступа в контейнере хранения Container07.</span><span class="sxs-lookup"><span data-stu-id="7a71c-111">This command gets all access policies in the storage container named Container07.</span></span>

## <span data-ttu-id="7a71c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a71c-112">PARAMETERS</span></span>

### <span data-ttu-id="7a71c-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7a71c-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7a71c-114">Указывает интервал времени и времени, в секундах, для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="7a71c-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="7a71c-115">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="7a71c-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="7a71c-116">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="7a71c-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7a71c-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7a71c-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7a71c-118">Указывает максимальное число сетевых звонков.</span><span class="sxs-lookup"><span data-stu-id="7a71c-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="7a71c-119">С помощью этого параметра можно ограничить одновременное использование локального ЦП и пропускной способности, указав максимальное количество сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="7a71c-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="7a71c-120">Указанное значение является абсолютным и не умножается на основное.</span><span class="sxs-lookup"><span data-stu-id="7a71c-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="7a71c-121">Этот параметр помогает уменьшить количество проблем с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.</span><span class="sxs-lookup"><span data-stu-id="7a71c-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="7a71c-122">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="7a71c-122">The default value is 10.</span></span>

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

### <span data-ttu-id="7a71c-123">-Container</span><span class="sxs-lookup"><span data-stu-id="7a71c-123">-Container</span></span>
<span data-ttu-id="7a71c-124">Имя контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7a71c-124">Specifies the name of your Azure storage container.</span></span>

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

### <span data-ttu-id="7a71c-125">-Контекст</span><span class="sxs-lookup"><span data-stu-id="7a71c-125">-Context</span></span>
<span data-ttu-id="7a71c-126">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7a71c-126">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="7a71c-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a71c-127">-DefaultProfile</span></span>
<span data-ttu-id="7a71c-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7a71c-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a71c-129">-Политика</span><span class="sxs-lookup"><span data-stu-id="7a71c-129">-Policy</span></span>
<span data-ttu-id="7a71c-130">Определяет политику хранимого доступа Azure.</span><span class="sxs-lookup"><span data-stu-id="7a71c-130">Specifies the Azure stored access policy.</span></span>

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

### <span data-ttu-id="7a71c-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7a71c-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7a71c-132">Для запроса указывается интервал времени, заданный для времени отрезка времени для стороны обслуживания (в секундах).</span><span class="sxs-lookup"><span data-stu-id="7a71c-132">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="7a71c-133">Если заданный интервал задан до обработки запроса службой хранилища, возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="7a71c-133">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="7a71c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a71c-134">CommonParameters</span></span>
<span data-ttu-id="7a71c-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a71c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a71c-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a71c-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a71c-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7a71c-137">INPUTS</span></span>

### <span data-ttu-id="7a71c-138">System.String</span><span class="sxs-lookup"><span data-stu-id="7a71c-138">System.String</span></span>

### <span data-ttu-id="7a71c-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7a71c-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7a71c-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7a71c-140">OUTPUTS</span></span>

### <span data-ttu-id="7a71c-141">Microsoft.Azure.Storage.Blob.SharedAccessBlobPolicy</span><span class="sxs-lookup"><span data-stu-id="7a71c-141">Microsoft.Azure.Storage.Blob.SharedAccessBlobPolicy</span></span>

## <span data-ttu-id="7a71c-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7a71c-142">NOTES</span></span>

## <span data-ttu-id="7a71c-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7a71c-143">RELATED LINKS</span></span>

[<span data-ttu-id="7a71c-144">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7a71c-144">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="7a71c-145">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7a71c-145">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="7a71c-146">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7a71c-146">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)


