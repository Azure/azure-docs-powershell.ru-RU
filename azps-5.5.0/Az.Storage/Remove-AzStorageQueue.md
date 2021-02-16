---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueue.md
ms.openlocfilehash: 2cc10a1b72dc369aef08b84e7b8fe2128ff0ac33
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232481"
---
# <span data-ttu-id="7a165-101">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="7a165-101">Remove-AzStorageQueue</span></span>

## <span data-ttu-id="7a165-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a165-102">SYNOPSIS</span></span>
<span data-ttu-id="7a165-103">Удаляет очередь хранилища.</span><span class="sxs-lookup"><span data-stu-id="7a165-103">Removes a storage queue.</span></span>

## <span data-ttu-id="7a165-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7a165-104">SYNTAX</span></span>

```
Remove-AzStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a165-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a165-105">DESCRIPTION</span></span>
<span data-ttu-id="7a165-106">Для удаления очереди хранилища **удаляется cmdlet Remove-AzStorageQueue.**</span><span class="sxs-lookup"><span data-stu-id="7a165-106">The **Remove-AzStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="7a165-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7a165-107">EXAMPLES</span></span>

### <span data-ttu-id="7a165-108">Пример 1. Удаление очереди хранилища по имени</span><span class="sxs-lookup"><span data-stu-id="7a165-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzStorageQueue "ContosoQueue01"
```

<span data-ttu-id="7a165-109">Эта команда удаляет очередь с именем ContosoQueue01.</span><span class="sxs-lookup"><span data-stu-id="7a165-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="7a165-110">Пример 2. Удаление нескольких очередей хранилища</span><span class="sxs-lookup"><span data-stu-id="7a165-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzStorageQueue "Contoso*" | Remove-AzStorageQueue
```

<span data-ttu-id="7a165-111">Эта команда удаляет все очереди с именами, имена которых начинаются с Contoso.</span><span class="sxs-lookup"><span data-stu-id="7a165-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="7a165-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a165-112">PARAMETERS</span></span>

### <span data-ttu-id="7a165-113">-Контекст</span><span class="sxs-lookup"><span data-stu-id="7a165-113">-Context</span></span>
<span data-ttu-id="7a165-114">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7a165-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="7a165-115">Чтобы получить контекст хранилища, New-AzStorageContext его.</span><span class="sxs-lookup"><span data-stu-id="7a165-115">To obtain the storage context, the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="7a165-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a165-116">-DefaultProfile</span></span>
<span data-ttu-id="7a165-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7a165-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a165-118">-Force</span><span class="sxs-lookup"><span data-stu-id="7a165-118">-Force</span></span>
<span data-ttu-id="7a165-119">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="7a165-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7a165-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7a165-120">-Name</span></span>
<span data-ttu-id="7a165-121">Указывает имя очереди, которая будет удаляться.</span><span class="sxs-lookup"><span data-stu-id="7a165-121">Specifies the name of the queue to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a165-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a165-122">-PassThru</span></span>
<span data-ttu-id="7a165-123">Указывает на то, что этот cmdlet возвращает **boolean,** который отражает успешность операции.</span><span class="sxs-lookup"><span data-stu-id="7a165-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="7a165-124">По умолчанию этот cmdlet не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7a165-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="7a165-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a165-125">-Confirm</span></span>
<span data-ttu-id="7a165-126">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="7a165-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a165-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a165-127">-WhatIf</span></span>
<span data-ttu-id="7a165-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a165-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a165-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7a165-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a165-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a165-130">CommonParameters</span></span>
<span data-ttu-id="7a165-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a165-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a165-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a165-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a165-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7a165-133">INPUTS</span></span>

### <span data-ttu-id="7a165-134">System.String</span><span class="sxs-lookup"><span data-stu-id="7a165-134">System.String</span></span>

### <span data-ttu-id="7a165-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7a165-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7a165-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7a165-136">OUTPUTS</span></span>

### <span data-ttu-id="7a165-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7a165-137">System.Boolean</span></span>

## <span data-ttu-id="7a165-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7a165-138">NOTES</span></span>

## <span data-ttu-id="7a165-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7a165-139">RELATED LINKS</span></span>

[<span data-ttu-id="7a165-140">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="7a165-140">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="7a165-141">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="7a165-141">New-AzStorageQueue</span></span>](./New-AzStorageQueue.md)
