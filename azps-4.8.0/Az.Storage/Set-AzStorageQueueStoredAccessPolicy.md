---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 0f8d9860f04112c197b91907a7622683069c3589
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235231"
---
# <span data-ttu-id="3f774-101">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3f774-101">Set-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="3f774-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3f774-102">SYNOPSIS</span></span>
<span data-ttu-id="3f774-103">Задает политику сохранения для доступа для очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="3f774-103">Sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="3f774-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3f774-104">SYNTAX</span></span>

```
Set-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f774-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f774-105">DESCRIPTION</span></span>
<span data-ttu-id="3f774-106">Командлет **Set-AzStorageQueueStoredAccessPolicy** задает политику сохраненного доступа для очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="3f774-106">The **Set-AzStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="3f774-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3f774-107">EXAMPLES</span></span>

### <span data-ttu-id="3f774-108">Пример 1: Настройка политики доступа в очереди с полным разрешением</span><span class="sxs-lookup"><span data-stu-id="3f774-108">Example 1: Set a stored access policy in the queue with full permission</span></span>
```
PS C:\> Set-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07" -Permission arup
```

<span data-ttu-id="3f774-109">Эта команда задает политику доступа с именем Policy07 для очереди хранения с именем MyQueue.</span><span class="sxs-lookup"><span data-stu-id="3f774-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="3f774-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3f774-110">PARAMETERS</span></span>

### <span data-ttu-id="3f774-111">-Context</span><span class="sxs-lookup"><span data-stu-id="3f774-111">-Context</span></span>
<span data-ttu-id="3f774-112">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="3f774-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3f774-113">Чтобы получить контекст хранилища, используйте командлет New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="3f774-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3f774-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f774-114">-DefaultProfile</span></span>
<span data-ttu-id="3f774-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3f774-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f774-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="3f774-116">-ExpiryTime</span></span>
<span data-ttu-id="3f774-117">Указывает время, в течение которого политика хранения сохраненных прав становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="3f774-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="3f774-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="3f774-118">-NoExpiryTime</span></span>
<span data-ttu-id="3f774-119">Указывает на то, что политика доступа не содержит дату окончания срока действия.</span><span class="sxs-lookup"><span data-stu-id="3f774-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="3f774-120">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="3f774-120">-NoStartTime</span></span>
<span data-ttu-id="3f774-121">Указывает на то, что этот командлет задает время запуска, которое должно быть $Null.</span><span class="sxs-lookup"><span data-stu-id="3f774-121">Indicates that this cmdlet sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="3f774-122">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="3f774-122">-Permission</span></span>
<span data-ttu-id="3f774-123">Определяет разрешения в политике сохранения доступа для доступа к очереди хранилища.</span><span class="sxs-lookup"><span data-stu-id="3f774-123">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="3f774-124">Важно отметить, что это строка, например `rwd` (для чтения, записи и удаления).</span><span class="sxs-lookup"><span data-stu-id="3f774-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="3f774-125">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="3f774-125">-Policy</span></span>
<span data-ttu-id="3f774-126">Задает имя для политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="3f774-126">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="3f774-127">-Очередь</span><span class="sxs-lookup"><span data-stu-id="3f774-127">-Queue</span></span>
<span data-ttu-id="3f774-128">Указывает имя очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="3f774-128">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="3f774-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3f774-129">-StartTime</span></span>
<span data-ttu-id="3f774-130">Указывает время вступления в силу политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="3f774-130">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="3f774-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f774-131">-Confirm</span></span>
<span data-ttu-id="3f774-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3f774-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f774-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f774-133">-WhatIf</span></span>
<span data-ttu-id="3f774-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3f774-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3f774-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3f774-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f774-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f774-136">CommonParameters</span></span>
<span data-ttu-id="3f774-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3f774-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f774-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f774-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f774-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3f774-139">INPUTS</span></span>

### <span data-ttu-id="3f774-140">System. String</span><span class="sxs-lookup"><span data-stu-id="3f774-140">System.String</span></span>

### <span data-ttu-id="3f774-141">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3f774-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3f774-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f774-142">OUTPUTS</span></span>

### <span data-ttu-id="3f774-143">System. String</span><span class="sxs-lookup"><span data-stu-id="3f774-143">System.String</span></span>

## <span data-ttu-id="3f774-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="3f774-144">NOTES</span></span>

## <span data-ttu-id="3f774-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f774-145">RELATED LINKS</span></span>

[<span data-ttu-id="3f774-146">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3f774-146">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="3f774-147">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3f774-147">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="3f774-148">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3f774-148">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)