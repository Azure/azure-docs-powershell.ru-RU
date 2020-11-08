---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 37E76360-B683-407C-9AEF-7138374562D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 52f1e3ce96133d0dc2e389f8eabcb18c6c7790c1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249345"
---
# <span data-ttu-id="3d4e4-101">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3d4e4-101">New-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="3d4e4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3d4e4-102">SYNOPSIS</span></span>
<span data-ttu-id="3d4e4-103">Создание политики сохранения для доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="3d4e4-103">Creates a stored access policy on a Storage share.</span></span>

## <span data-ttu-id="3d4e4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3d4e4-104">SYNTAX</span></span>

```
New-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="3d4e4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d4e4-105">DESCRIPTION</span></span>
<span data-ttu-id="3d4e4-106">Командлет **New-AzStorageShareStoredAccessPolicy** создает политику сохранения для доступа к хранилищу Azure.</span><span class="sxs-lookup"><span data-stu-id="3d4e4-106">The **New-AzStorageShareStoredAccessPolicy** cmdlet creates a stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="3d4e4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3d4e4-107">EXAMPLES</span></span>

### <span data-ttu-id="3d4e4-108">Пример 1: Создание политики сохраненных прав доступа в общем доступе</span><span class="sxs-lookup"><span data-stu-id="3d4e4-108">Example 1: Create a stored access policy in a share</span></span>
```
PS C:\>New-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="3d4e4-109">Эта команда создает политику доступа с уровнем "полный доступ" в общем доступе.</span><span class="sxs-lookup"><span data-stu-id="3d4e4-109">This command creates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="3d4e4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3d4e4-110">PARAMETERS</span></span>

### <span data-ttu-id="3d4e4-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3d4e4-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3d4e4-112">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="3d4e4-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3d4e4-113">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="3d4e4-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3d4e4-114">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="3d4e4-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="3d4e4-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3d4e4-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3d4e4-116">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="3d4e4-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="3d4e4-117">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="3d4e4-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="3d4e4-118">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="3d4e4-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="3d4e4-119">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="3d4e4-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="3d4e4-120">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="3d4e4-120">The default value is 10.</span></span>

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

### <span data-ttu-id="3d4e4-121">-Context</span><span class="sxs-lookup"><span data-stu-id="3d4e4-121">-Context</span></span>
<span data-ttu-id="3d4e4-122">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="3d4e4-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3d4e4-123">Чтобы получить контекст хранения, используйте командлет [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="3d4e4-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="3d4e4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d4e4-124">-DefaultProfile</span></span>
<span data-ttu-id="3d4e4-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3d4e4-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d4e4-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="3d4e4-126">-ExpiryTime</span></span>
<span data-ttu-id="3d4e4-127">Указывает время, в течение которого политика хранения сохраненных прав становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="3d4e4-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="3d4e4-128">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="3d4e4-128">-Permission</span></span>
<span data-ttu-id="3d4e4-129">Определяет разрешения в политике сохранения доступа для доступа к общей папке хранилища или файлам.</span><span class="sxs-lookup"><span data-stu-id="3d4e4-129">Specifies permissions in the stored access policy to access the Storage share or files under it.</span></span>
<span data-ttu-id="3d4e4-130">Важно отметить, что это строка, например `rwd` (для чтения, записи и удаления).</span><span class="sxs-lookup"><span data-stu-id="3d4e4-130">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="3d4e4-131">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="3d4e4-131">-Policy</span></span>
<span data-ttu-id="3d4e4-132">Задает имя для политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="3d4e4-132">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="3d4e4-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3d4e4-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3d4e4-134">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="3d4e4-134">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="3d4e4-135">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="3d4e4-135">-ShareName</span></span>
<span data-ttu-id="3d4e4-136">Указывает имя общего доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="3d4e4-136">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="3d4e4-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3d4e4-137">-StartTime</span></span>
<span data-ttu-id="3d4e4-138">Указывает время вступления в силу политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="3d4e4-138">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="3d4e4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d4e4-139">CommonParameters</span></span>
<span data-ttu-id="3d4e4-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3d4e4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d4e4-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d4e4-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d4e4-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3d4e4-142">INPUTS</span></span>

### <span data-ttu-id="3d4e4-143">System. String</span><span class="sxs-lookup"><span data-stu-id="3d4e4-143">System.String</span></span>

### <span data-ttu-id="3d4e4-144">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3d4e4-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3d4e4-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d4e4-145">OUTPUTS</span></span>

### <span data-ttu-id="3d4e4-146">System. String</span><span class="sxs-lookup"><span data-stu-id="3d4e4-146">System.String</span></span>

## <span data-ttu-id="3d4e4-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="3d4e4-147">NOTES</span></span>

## <span data-ttu-id="3d4e4-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3d4e4-148">RELATED LINKS</span></span>

[<span data-ttu-id="3d4e4-149">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3d4e4-149">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="3d4e4-150">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="3d4e4-150">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="3d4e4-151">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3d4e4-151">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="3d4e4-152">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3d4e4-152">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)
