---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueue.md
ms.openlocfilehash: 2cc10a1b72dc369aef08b84e7b8fe2128ff0ac33
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236527"
---
# <span data-ttu-id="99706-101">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="99706-101">Remove-AzStorageQueue</span></span>

## <span data-ttu-id="99706-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="99706-102">SYNOPSIS</span></span>
<span data-ttu-id="99706-103">Удаляет очередь хранилища.</span><span class="sxs-lookup"><span data-stu-id="99706-103">Removes a storage queue.</span></span>

## <span data-ttu-id="99706-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="99706-104">SYNTAX</span></span>

```
Remove-AzStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99706-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="99706-105">DESCRIPTION</span></span>
<span data-ttu-id="99706-106">Командлет **Remove-AzStorageQueue** Удаляет очередь хранилища.</span><span class="sxs-lookup"><span data-stu-id="99706-106">The **Remove-AzStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="99706-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="99706-107">EXAMPLES</span></span>

### <span data-ttu-id="99706-108">Пример 1: удаление очереди хранилища по имени</span><span class="sxs-lookup"><span data-stu-id="99706-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzStorageQueue "ContosoQueue01"
```

<span data-ttu-id="99706-109">Эта команда удаляет очередь с именем ContosoQueue01.</span><span class="sxs-lookup"><span data-stu-id="99706-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="99706-110">Пример 2: удаление нескольких очередей хранилища</span><span class="sxs-lookup"><span data-stu-id="99706-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzStorageQueue "Contoso*" | Remove-AzStorageQueue
```

<span data-ttu-id="99706-111">Эта команда удаляет все очереди с именами, которые начинаются с contoso.</span><span class="sxs-lookup"><span data-stu-id="99706-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="99706-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="99706-112">PARAMETERS</span></span>

### <span data-ttu-id="99706-113">-Context</span><span class="sxs-lookup"><span data-stu-id="99706-113">-Context</span></span>
<span data-ttu-id="99706-114">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="99706-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="99706-115">Чтобы получить контекст хранилища, New-AzStorageContext командлет.</span><span class="sxs-lookup"><span data-stu-id="99706-115">To obtain the storage context, the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="99706-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99706-116">-DefaultProfile</span></span>
<span data-ttu-id="99706-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="99706-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99706-118">-Force</span><span class="sxs-lookup"><span data-stu-id="99706-118">-Force</span></span>
<span data-ttu-id="99706-119">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="99706-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="99706-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="99706-120">-Name</span></span>
<span data-ttu-id="99706-121">Указывает имя очереди, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="99706-121">Specifies the name of the queue to remove.</span></span>

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

### <span data-ttu-id="99706-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99706-122">-PassThru</span></span>
<span data-ttu-id="99706-123">Указывает на то, что этот командлет возвращает **логическое значение** , отражающее успешное выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="99706-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="99706-124">По умолчанию этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="99706-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="99706-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="99706-125">-Confirm</span></span>
<span data-ttu-id="99706-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="99706-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99706-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99706-127">-WhatIf</span></span>
<span data-ttu-id="99706-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="99706-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99706-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="99706-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99706-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99706-130">CommonParameters</span></span>
<span data-ttu-id="99706-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="99706-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99706-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99706-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99706-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="99706-133">INPUTS</span></span>

### <span data-ttu-id="99706-134">System. String</span><span class="sxs-lookup"><span data-stu-id="99706-134">System.String</span></span>

### <span data-ttu-id="99706-135">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="99706-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="99706-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="99706-136">OUTPUTS</span></span>

### <span data-ttu-id="99706-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="99706-137">System.Boolean</span></span>

## <span data-ttu-id="99706-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="99706-138">NOTES</span></span>

## <span data-ttu-id="99706-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="99706-139">RELATED LINKS</span></span>

[<span data-ttu-id="99706-140">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="99706-140">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="99706-141">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="99706-141">New-AzStorageQueue</span></span>](./New-AzStorageQueue.md)
