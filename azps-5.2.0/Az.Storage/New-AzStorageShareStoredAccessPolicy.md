---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 37E76360-B683-407C-9AEF-7138374562D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 52f1e3ce96133d0dc2e389f8eabcb18c6c7790c1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404079"
---
# <span data-ttu-id="188cc-101">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="188cc-101">New-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="188cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="188cc-102">SYNOPSIS</span></span>
<span data-ttu-id="188cc-103">Создает политику доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="188cc-103">Creates a stored access policy on a Storage share.</span></span>

## <span data-ttu-id="188cc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="188cc-104">SYNTAX</span></span>

```
New-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="188cc-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="188cc-105">DESCRIPTION</span></span>
<span data-ttu-id="188cc-106">С **его** использованием создается политика доступа для хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="188cc-106">The **New-AzStorageShareStoredAccessPolicy** cmdlet creates a stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="188cc-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="188cc-107">EXAMPLES</span></span>

### <span data-ttu-id="188cc-108">Пример 1. Создание политики хранимого доступа в области</span><span class="sxs-lookup"><span data-stu-id="188cc-108">Example 1: Create a stored access policy in a share</span></span>
```
PS C:\>New-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="188cc-109">Эта команда создает хранимую политику доступа с полными разрешениями на доступ.</span><span class="sxs-lookup"><span data-stu-id="188cc-109">This command creates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="188cc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="188cc-110">PARAMETERS</span></span>

### <span data-ttu-id="188cc-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="188cc-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="188cc-112">Указывает интервал времени и времени, в секундах, для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="188cc-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="188cc-113">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="188cc-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="188cc-114">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="188cc-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="188cc-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="188cc-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="188cc-116">Указывает максимальное число сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="188cc-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="188cc-117">С помощью этого параметра можно ограничить одновременное использование локального ЦП и пропускной способности, указав максимальное количество сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="188cc-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="188cc-118">Указанное значение является абсолютным и не умножается на основное.</span><span class="sxs-lookup"><span data-stu-id="188cc-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="188cc-119">Этот параметр помогает уменьшить количество проблем с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.</span><span class="sxs-lookup"><span data-stu-id="188cc-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="188cc-120">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="188cc-120">The default value is 10.</span></span>

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

### <span data-ttu-id="188cc-121">-Контекст</span><span class="sxs-lookup"><span data-stu-id="188cc-121">-Context</span></span>
<span data-ttu-id="188cc-122">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="188cc-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="188cc-123">Чтобы получить контекст хранилища, воспользуйтесь [cmdlet New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="188cc-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="188cc-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="188cc-124">-DefaultProfile</span></span>
<span data-ttu-id="188cc-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="188cc-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="188cc-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="188cc-126">-ExpiryTime</span></span>
<span data-ttu-id="188cc-127">Время, в течение которого хранимая политика доступа становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="188cc-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="188cc-128">-Permission</span><span class="sxs-lookup"><span data-stu-id="188cc-128">-Permission</span></span>
<span data-ttu-id="188cc-129">Определяет разрешения в хранимой политике доступа на доступ к папке или файлам в хранилище.</span><span class="sxs-lookup"><span data-stu-id="188cc-129">Specifies permissions in the stored access policy to access the Storage share or files under it.</span></span>
<span data-ttu-id="188cc-130">Важно отметить, что это строка (для чтения, записи `rwd` и удаления).</span><span class="sxs-lookup"><span data-stu-id="188cc-130">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="188cc-131">-Политика</span><span class="sxs-lookup"><span data-stu-id="188cc-131">-Policy</span></span>
<span data-ttu-id="188cc-132">Указывает имя хранимой политики доступа.</span><span class="sxs-lookup"><span data-stu-id="188cc-132">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="188cc-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="188cc-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="188cc-134">Определяет продолжительность периода времени ожидания для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="188cc-134">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="188cc-135">-ShareName</span><span class="sxs-lookup"><span data-stu-id="188cc-135">-ShareName</span></span>
<span data-ttu-id="188cc-136">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="188cc-136">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="188cc-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="188cc-137">-StartTime</span></span>
<span data-ttu-id="188cc-138">Время, в течение которого хранимая политика доступа становится допустимой.</span><span class="sxs-lookup"><span data-stu-id="188cc-138">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="188cc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="188cc-139">CommonParameters</span></span>
<span data-ttu-id="188cc-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="188cc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="188cc-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="188cc-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="188cc-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="188cc-142">INPUTS</span></span>

### <span data-ttu-id="188cc-143">System.String</span><span class="sxs-lookup"><span data-stu-id="188cc-143">System.String</span></span>

### <span data-ttu-id="188cc-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="188cc-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="188cc-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="188cc-145">OUTPUTS</span></span>

### <span data-ttu-id="188cc-146">System.String</span><span class="sxs-lookup"><span data-stu-id="188cc-146">System.String</span></span>

## <span data-ttu-id="188cc-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="188cc-147">NOTES</span></span>

## <span data-ttu-id="188cc-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="188cc-148">RELATED LINKS</span></span>

[<span data-ttu-id="188cc-149">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="188cc-149">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="188cc-150">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="188cc-150">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="188cc-151">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="188cc-151">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="188cc-152">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="188cc-152">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)
