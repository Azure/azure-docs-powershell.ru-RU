---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: e20caedc23dcd4d06336f3dddf80fdaf4a84cbcc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566002"
---
# <span data-ttu-id="e19d1-101">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e19d1-101">Set-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="e19d1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e19d1-102">SYNOPSIS</span></span>
<span data-ttu-id="e19d1-103">Задает политику сохранения для доступа для очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="e19d1-103">Sets a stored access policy for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e19d1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e19d1-104">SYNTAX</span></span>

```
Set-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e19d1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e19d1-105">DESCRIPTION</span></span>
<span data-ttu-id="e19d1-106">Командлет **Set-AzureStorageQueueStoredAccessPolicy** задает политику сохраненного доступа для очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="e19d1-106">The **Set-AzureStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="e19d1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e19d1-107">EXAMPLES</span></span>

### <span data-ttu-id="e19d1-108">Пример 1: Настройка политики доступа в очереди с полным разрешением</span><span class="sxs-lookup"><span data-stu-id="e19d1-108">Example 1: Set a stored access policy in the queue with full permission</span></span>
```
PS C:\> Set-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07" -Permission arup
```

<span data-ttu-id="e19d1-109">Эта команда задает политику доступа с именем Policy07 для очереди хранения с именем MyQueue.</span><span class="sxs-lookup"><span data-stu-id="e19d1-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="e19d1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e19d1-110">PARAMETERS</span></span>

### <span data-ttu-id="e19d1-111">-Context</span><span class="sxs-lookup"><span data-stu-id="e19d1-111">-Context</span></span>
<span data-ttu-id="e19d1-112">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="e19d1-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e19d1-113">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="e19d1-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e19d1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e19d1-114">-DefaultProfile</span></span>
<span data-ttu-id="e19d1-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e19d1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e19d1-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="e19d1-116">-ExpiryTime</span></span>
<span data-ttu-id="e19d1-117">Указывает время, в течение которого политика хранения сохраненных прав становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="e19d1-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="e19d1-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="e19d1-118">-NoExpiryTime</span></span>
<span data-ttu-id="e19d1-119">Указывает на то, что политика доступа не содержит дату окончания срока действия.</span><span class="sxs-lookup"><span data-stu-id="e19d1-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="e19d1-120">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="e19d1-120">-NoStartTime</span></span>
<span data-ttu-id="e19d1-121">Указывает на то, что этот командлет задает время запуска, которое должно быть $Null.</span><span class="sxs-lookup"><span data-stu-id="e19d1-121">Indicates that this cmdlet sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="e19d1-122">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="e19d1-122">-Permission</span></span>
<span data-ttu-id="e19d1-123">Определяет разрешения в политике сохранения доступа для доступа к очереди хранилища.</span><span class="sxs-lookup"><span data-stu-id="e19d1-123">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="e19d1-124">Важно отметить, что это строка, например `rwd` (для чтения, записи и удаления).</span><span class="sxs-lookup"><span data-stu-id="e19d1-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="e19d1-125">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="e19d1-125">-Policy</span></span>
<span data-ttu-id="e19d1-126">Задает имя для политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="e19d1-126">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="e19d1-127">-Очередь</span><span class="sxs-lookup"><span data-stu-id="e19d1-127">-Queue</span></span>
<span data-ttu-id="e19d1-128">Указывает имя очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="e19d1-128">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="e19d1-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e19d1-129">-StartTime</span></span>
<span data-ttu-id="e19d1-130">Указывает время вступления в силу политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="e19d1-130">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="e19d1-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e19d1-131">-Confirm</span></span>
<span data-ttu-id="e19d1-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e19d1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e19d1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e19d1-133">-WhatIf</span></span>
<span data-ttu-id="e19d1-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e19d1-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e19d1-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e19d1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e19d1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e19d1-136">CommonParameters</span></span>
<span data-ttu-id="e19d1-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e19d1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e19d1-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e19d1-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e19d1-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e19d1-139">INPUTS</span></span>

### <span data-ttu-id="e19d1-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e19d1-140">System.String</span></span>

### <span data-ttu-id="e19d1-141">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e19d1-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e19d1-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e19d1-142">OUTPUTS</span></span>

### <span data-ttu-id="e19d1-143">System. String</span><span class="sxs-lookup"><span data-stu-id="e19d1-143">System.String</span></span>

## <span data-ttu-id="e19d1-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="e19d1-144">NOTES</span></span>

## <span data-ttu-id="e19d1-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e19d1-145">RELATED LINKS</span></span>

[<span data-ttu-id="e19d1-146">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e19d1-146">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="e19d1-147">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e19d1-147">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="e19d1-148">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e19d1-148">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)
