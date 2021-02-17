---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FCDCEF0B-6E2C-480E-9841-EF4E64D61D54
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShare.md
ms.openlocfilehash: 4fa89a13f9b4124232d9459d7d3eff54a6f55a5c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217252"
---
# <span data-ttu-id="8bb6e-101">New-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="8bb6e-101">New-AzStorageShare</span></span>

## <span data-ttu-id="8bb6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bb6e-102">SYNOPSIS</span></span>
<span data-ttu-id="8bb6e-103">Создается файловая папка.</span><span class="sxs-lookup"><span data-stu-id="8bb6e-103">Creates a file share.</span></span>

## <span data-ttu-id="8bb6e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8bb6e-104">SYNTAX</span></span>

```
New-AzStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="8bb6e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8bb6e-105">DESCRIPTION</span></span>
<span data-ttu-id="8bb6e-106">Для этого создается файлообъединет **New-AzStorageShare.**</span><span class="sxs-lookup"><span data-stu-id="8bb6e-106">The **New-AzStorageShare** cmdlet creates a file share.</span></span>

## <span data-ttu-id="8bb6e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8bb6e-107">EXAMPLES</span></span>

### <span data-ttu-id="8bb6e-108">Пример 1. Создание файловой папки</span><span class="sxs-lookup"><span data-stu-id="8bb6e-108">Example 1: Create a file share</span></span>
```
PS C:\>New-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="8bb6e-109">Эта команда создает папку с именем ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="8bb6e-109">This command creates a file share named ContosoShare06.</span></span>

## <span data-ttu-id="8bb6e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8bb6e-110">PARAMETERS</span></span>

### <span data-ttu-id="8bb6e-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8bb6e-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="8bb6e-112">Указывает интервал времени и времени, в секундах, для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="8bb6e-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="8bb6e-113">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="8bb6e-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="8bb6e-114">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="8bb6e-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="8bb6e-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="8bb6e-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="8bb6e-116">Указывает максимальное число сетевых звонков.</span><span class="sxs-lookup"><span data-stu-id="8bb6e-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="8bb6e-117">С помощью этого параметра можно ограничить одновременное использование локального ЦП и пропускной способности, указав максимальное количество сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="8bb6e-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="8bb6e-118">Указанное значение является абсолютным и не умножается на основное.</span><span class="sxs-lookup"><span data-stu-id="8bb6e-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="8bb6e-119">Этот параметр помогает уменьшить количество проблем с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.</span><span class="sxs-lookup"><span data-stu-id="8bb6e-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="8bb6e-120">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="8bb6e-120">The default value is 10.</span></span>

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

### <span data-ttu-id="8bb6e-121">-Контекст</span><span class="sxs-lookup"><span data-stu-id="8bb6e-121">-Context</span></span>
<span data-ttu-id="8bb6e-122">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="8bb6e-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8bb6e-123">Чтобы получить контекст хранилища, воспользуйтесь [cmdlet New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="8bb6e-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="8bb6e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bb6e-124">-DefaultProfile</span></span>
<span data-ttu-id="8bb6e-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8bb6e-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bb6e-126">-Name</span><span class="sxs-lookup"><span data-stu-id="8bb6e-126">-Name</span></span>
<span data-ttu-id="8bb6e-127">Имя файловой папки.</span><span class="sxs-lookup"><span data-stu-id="8bb6e-127">Specifies the name of a file share.</span></span>
<span data-ttu-id="8bb6e-128">Этот cmdlet создает папку с именем, указанным этим параметром.</span><span class="sxs-lookup"><span data-stu-id="8bb6e-128">This cmdlet creates a file share that has the name that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8bb6e-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8bb6e-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="8bb6e-130">Определяет продолжительность периода времени ожидания для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="8bb6e-130">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="8bb6e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bb6e-131">CommonParameters</span></span>
<span data-ttu-id="8bb6e-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bb6e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bb6e-133">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bb6e-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bb6e-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8bb6e-134">INPUTS</span></span>

### <span data-ttu-id="8bb6e-135">System.String</span><span class="sxs-lookup"><span data-stu-id="8bb6e-135">System.String</span></span>

### <span data-ttu-id="8bb6e-136">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8bb6e-136">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8bb6e-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8bb6e-137">OUTPUTS</span></span>

### <span data-ttu-id="8bb6e-138">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span><span class="sxs-lookup"><span data-stu-id="8bb6e-138">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="8bb6e-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8bb6e-139">NOTES</span></span>

## <span data-ttu-id="8bb6e-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8bb6e-140">RELATED LINKS</span></span>

[<span data-ttu-id="8bb6e-141">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="8bb6e-141">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="8bb6e-142">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="8bb6e-142">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="8bb6e-143">Remove-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="8bb6e-143">Remove-AzStorageShare</span></span>](./Remove-AzStorageShare.md)
