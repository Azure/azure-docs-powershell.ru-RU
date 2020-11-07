---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueue.md
ms.openlocfilehash: b98b0ef6e8c4d47c32cab4ee891041e0820ea3ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733300"
---
# <span data-ttu-id="9931c-101">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="9931c-101">Remove-AzureStorageQueue</span></span>

## <span data-ttu-id="9931c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9931c-102">SYNOPSIS</span></span>
<span data-ttu-id="9931c-103">Удаляет очередь хранилища.</span><span class="sxs-lookup"><span data-stu-id="9931c-103">Removes a storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9931c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9931c-104">SYNTAX</span></span>

```
Remove-AzureStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9931c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9931c-105">DESCRIPTION</span></span>
<span data-ttu-id="9931c-106">Командлет **Remove-AzureStorageQueue** Удаляет очередь хранилища.</span><span class="sxs-lookup"><span data-stu-id="9931c-106">The **Remove-AzureStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="9931c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9931c-107">EXAMPLES</span></span>

### <span data-ttu-id="9931c-108">Пример 1: удаление очереди хранилища по имени</span><span class="sxs-lookup"><span data-stu-id="9931c-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzureStorageQueue "ContosoQueue01"
```

<span data-ttu-id="9931c-109">Эта команда удаляет очередь с именем ContosoQueue01.</span><span class="sxs-lookup"><span data-stu-id="9931c-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="9931c-110">Пример 2: удаление нескольких очередей хранилища</span><span class="sxs-lookup"><span data-stu-id="9931c-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue "Contoso*" | Remove-AzureStorageQueue
```

<span data-ttu-id="9931c-111">Эта команда удаляет все очереди с именами, которые начинаются с contoso.</span><span class="sxs-lookup"><span data-stu-id="9931c-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="9931c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9931c-112">PARAMETERS</span></span>

### <span data-ttu-id="9931c-113">-Context</span><span class="sxs-lookup"><span data-stu-id="9931c-113">-Context</span></span>
<span data-ttu-id="9931c-114">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="9931c-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="9931c-115">Чтобы получить контекст хранилища, New-AzureStorageContext командлет.</span><span class="sxs-lookup"><span data-stu-id="9931c-115">To obtain the storage context, the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9931c-116">-Force</span><span class="sxs-lookup"><span data-stu-id="9931c-116">-Force</span></span>
<span data-ttu-id="9931c-117">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="9931c-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9931c-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9931c-118">-Name</span></span>
<span data-ttu-id="9931c-119">Указывает имя очереди, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="9931c-119">Specifies the name of the queue to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9931c-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9931c-120">-PassThru</span></span>
<span data-ttu-id="9931c-121">Указывает на то, что этот командлет возвращает **логическое значение** , отражающее успешное выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="9931c-121">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="9931c-122">По умолчанию этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="9931c-122">By default, this cmdlet does not return a value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9931c-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9931c-123">-Confirm</span></span>
<span data-ttu-id="9931c-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9931c-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9931c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9931c-125">-WhatIf</span></span>
<span data-ttu-id="9931c-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9931c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9931c-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9931c-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9931c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9931c-128">CommonParameters</span></span>
<span data-ttu-id="9931c-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9931c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9931c-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9931c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9931c-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9931c-131">INPUTS</span></span>

### <span data-ttu-id="9931c-132">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9931c-132">IStorageContext</span></span>

<span data-ttu-id="9931c-133">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="9931c-133">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="9931c-134">Подстрок</span><span class="sxs-lookup"><span data-stu-id="9931c-134">String</span></span>

<span data-ttu-id="9931c-135">Параметр Name принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="9931c-135">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="9931c-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9931c-136">OUTPUTS</span></span>

### <span data-ttu-id="9931c-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9931c-137">System.Boolean</span></span>

## <span data-ttu-id="9931c-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="9931c-138">NOTES</span></span>

## <span data-ttu-id="9931c-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9931c-139">RELATED LINKS</span></span>

[<span data-ttu-id="9931c-140">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="9931c-140">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="9931c-141">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="9931c-141">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)
