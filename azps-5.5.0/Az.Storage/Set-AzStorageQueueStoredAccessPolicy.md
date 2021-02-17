---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 0f8d9860f04112c197b91907a7622683069c3589
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241797"
---
# <span data-ttu-id="6e408-101">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6e408-101">Set-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="6e408-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e408-102">SYNOPSIS</span></span>
<span data-ttu-id="6e408-103">Задает политику хранимого доступа для очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="6e408-103">Sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="6e408-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6e408-104">SYNTAX</span></span>

```
Set-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e408-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e408-105">DESCRIPTION</span></span>
<span data-ttu-id="6e408-106">**Cmdlet Set-AzStorageQueueStoredAccessPolicy** задает политику хранимого доступа для очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="6e408-106">The **Set-AzStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="6e408-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6e408-107">EXAMPLES</span></span>

### <span data-ttu-id="6e408-108">Пример 1. Настройка хранимой политики доступа в очереди с полными разрешениями</span><span class="sxs-lookup"><span data-stu-id="6e408-108">Example 1: Set a stored access policy in the queue with full permission</span></span>
```
PS C:\> Set-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07" -Permission arup
```

<span data-ttu-id="6e408-109">Эта команда задает политику доступа с именем Policy07 для очереди хранения MyQueue.</span><span class="sxs-lookup"><span data-stu-id="6e408-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="6e408-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e408-110">PARAMETERS</span></span>

### <span data-ttu-id="6e408-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="6e408-111">-Context</span></span>
<span data-ttu-id="6e408-112">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="6e408-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="6e408-113">Для получения контекста хранилища используйте New-AzStorageContext управления.</span><span class="sxs-lookup"><span data-stu-id="6e408-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6e408-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e408-114">-DefaultProfile</span></span>
<span data-ttu-id="6e408-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6e408-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e408-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="6e408-116">-ExpiryTime</span></span>
<span data-ttu-id="6e408-117">Время, в течение которого хранимая политика доступа становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="6e408-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="6e408-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="6e408-118">-NoExpiryTime</span></span>
<span data-ttu-id="6e408-119">Указывает на то, что срок действия политики доступа не истек.</span><span class="sxs-lookup"><span data-stu-id="6e408-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="6e408-120">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="6e408-120">-NoStartTime</span></span>
<span data-ttu-id="6e408-121">Указывает на то, что этот cmdlet задает время начала $Null.</span><span class="sxs-lookup"><span data-stu-id="6e408-121">Indicates that this cmdlet sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="6e408-122">-Permission</span><span class="sxs-lookup"><span data-stu-id="6e408-122">-Permission</span></span>
<span data-ttu-id="6e408-123">Определяет разрешения в хранимой политике доступа на доступ к очереди хранилища.</span><span class="sxs-lookup"><span data-stu-id="6e408-123">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="6e408-124">Важно отметить, что это строка (для чтения, записи `rwd` и удаления).</span><span class="sxs-lookup"><span data-stu-id="6e408-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="6e408-125">-Политика</span><span class="sxs-lookup"><span data-stu-id="6e408-125">-Policy</span></span>
<span data-ttu-id="6e408-126">Указывает имя хранимой политики доступа.</span><span class="sxs-lookup"><span data-stu-id="6e408-126">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="6e408-127">-Queue</span><span class="sxs-lookup"><span data-stu-id="6e408-127">-Queue</span></span>
<span data-ttu-id="6e408-128">Указывает имя очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="6e408-128">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="6e408-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="6e408-129">-StartTime</span></span>
<span data-ttu-id="6e408-130">Время, в течение которого хранимая политика доступа становится допустимой.</span><span class="sxs-lookup"><span data-stu-id="6e408-130">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="6e408-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e408-131">-Confirm</span></span>
<span data-ttu-id="6e408-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6e408-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e408-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e408-133">-WhatIf</span></span>
<span data-ttu-id="6e408-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e408-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6e408-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6e408-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e408-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e408-136">CommonParameters</span></span>
<span data-ttu-id="6e408-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e408-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e408-138">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e408-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e408-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6e408-139">INPUTS</span></span>

### <span data-ttu-id="6e408-140">System.String</span><span class="sxs-lookup"><span data-stu-id="6e408-140">System.String</span></span>

### <span data-ttu-id="6e408-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6e408-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6e408-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6e408-142">OUTPUTS</span></span>

### <span data-ttu-id="6e408-143">System.String</span><span class="sxs-lookup"><span data-stu-id="6e408-143">System.String</span></span>

## <span data-ttu-id="6e408-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6e408-144">NOTES</span></span>

## <span data-ttu-id="6e408-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6e408-145">RELATED LINKS</span></span>

[<span data-ttu-id="6e408-146">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6e408-146">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="6e408-147">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6e408-147">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="6e408-148">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6e408-148">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)
