---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 37E76360-B683-407C-9AEF-7138374562D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: a4013543cfd96a1aaae591a9f1b1ed4b6da46155
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904458"
---
# <span data-ttu-id="40d77-101">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="40d77-101">New-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="40d77-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="40d77-102">SYNOPSIS</span></span>
<span data-ttu-id="40d77-103">Создание политики сохранения для доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="40d77-103">Creates a stored access policy on a Storage share.</span></span>

## <span data-ttu-id="40d77-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="40d77-104">SYNTAX</span></span>

```
New-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="40d77-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="40d77-105">DESCRIPTION</span></span>
<span data-ttu-id="40d77-106">Командлет **New-AzStorageShareStoredAccessPolicy** создает политику сохранения для доступа к хранилищу Azure.</span><span class="sxs-lookup"><span data-stu-id="40d77-106">The **New-AzStorageShareStoredAccessPolicy** cmdlet creates a stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="40d77-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="40d77-107">EXAMPLES</span></span>

### <span data-ttu-id="40d77-108">Пример 1: Создание политики сохраненных прав доступа в общем доступе</span><span class="sxs-lookup"><span data-stu-id="40d77-108">Example 1: Create a stored access policy in a share</span></span>
```
PS C:\>New-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="40d77-109">Эта команда создает политику доступа с уровнем "полный доступ" в общем доступе.</span><span class="sxs-lookup"><span data-stu-id="40d77-109">This command creates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="40d77-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="40d77-110">PARAMETERS</span></span>

### <span data-ttu-id="40d77-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="40d77-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="40d77-112">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="40d77-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="40d77-113">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="40d77-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="40d77-114">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="40d77-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="40d77-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="40d77-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="40d77-116">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="40d77-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="40d77-117">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="40d77-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="40d77-118">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="40d77-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="40d77-119">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="40d77-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="40d77-120">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="40d77-120">The default value is 10.</span></span>

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

### <span data-ttu-id="40d77-121">-Context</span><span class="sxs-lookup"><span data-stu-id="40d77-121">-Context</span></span>
<span data-ttu-id="40d77-122">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="40d77-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="40d77-123">Чтобы получить контекст хранения, используйте командлет [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="40d77-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="40d77-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40d77-124">-DefaultProfile</span></span>
<span data-ttu-id="40d77-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="40d77-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40d77-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="40d77-126">-ExpiryTime</span></span>
<span data-ttu-id="40d77-127">Указывает время, в течение которого политика хранения сохраненных прав становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="40d77-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="40d77-128">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="40d77-128">-Permission</span></span>
<span data-ttu-id="40d77-129">Определяет разрешения в политике сохранения доступа для доступа к общей папке хранилища или файлам.</span><span class="sxs-lookup"><span data-stu-id="40d77-129">Specifies permissions in the stored access policy to access the Storage share or files under it.</span></span>
<span data-ttu-id="40d77-130">Важно отметить, что это строка, например `rwd` (для чтения, записи и удаления).</span><span class="sxs-lookup"><span data-stu-id="40d77-130">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="40d77-131">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="40d77-131">-Policy</span></span>
<span data-ttu-id="40d77-132">Задает имя для политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="40d77-132">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="40d77-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="40d77-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="40d77-134">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="40d77-134">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="40d77-135">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="40d77-135">-ShareName</span></span>
<span data-ttu-id="40d77-136">Указывает имя общего доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="40d77-136">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="40d77-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="40d77-137">-StartTime</span></span>
<span data-ttu-id="40d77-138">Указывает время вступления в силу политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="40d77-138">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="40d77-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40d77-139">CommonParameters</span></span>
<span data-ttu-id="40d77-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="40d77-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40d77-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40d77-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40d77-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="40d77-142">INPUTS</span></span>

### <span data-ttu-id="40d77-143">System. String</span><span class="sxs-lookup"><span data-stu-id="40d77-143">System.String</span></span>

### <span data-ttu-id="40d77-144">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="40d77-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="40d77-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="40d77-145">OUTPUTS</span></span>

### <span data-ttu-id="40d77-146">System. String</span><span class="sxs-lookup"><span data-stu-id="40d77-146">System.String</span></span>

## <span data-ttu-id="40d77-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="40d77-147">NOTES</span></span>

## <span data-ttu-id="40d77-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="40d77-148">RELATED LINKS</span></span>

[<span data-ttu-id="40d77-149">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="40d77-149">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="40d77-150">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="40d77-150">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="40d77-151">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="40d77-151">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="40d77-152">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="40d77-152">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)
