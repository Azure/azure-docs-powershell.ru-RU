---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 54770fd564addf30e7c4ed058776857b823903e3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556147"
---
# <span data-ttu-id="43f52-101">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="43f52-101">Remove-AzureStorageQueue</span></span>

## <span data-ttu-id="43f52-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="43f52-102">SYNOPSIS</span></span>
<span data-ttu-id="43f52-103">Удаляет очередь хранилища.</span><span class="sxs-lookup"><span data-stu-id="43f52-103">Removes a storage queue.</span></span>

## <span data-ttu-id="43f52-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="43f52-104">SYNTAX</span></span>

```
Remove-AzureStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43f52-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="43f52-105">DESCRIPTION</span></span>
<span data-ttu-id="43f52-106">Командлет **Remove-AzureStorageQueue** Удаляет очередь хранилища.</span><span class="sxs-lookup"><span data-stu-id="43f52-106">The **Remove-AzureStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="43f52-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="43f52-107">EXAMPLES</span></span>

### <span data-ttu-id="43f52-108">Пример 1: удаление очереди хранилища по имени</span><span class="sxs-lookup"><span data-stu-id="43f52-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzureStorageQueue "ContosoQueue01"
```

<span data-ttu-id="43f52-109">Эта команда удаляет очередь с именем ContosoQueue01.</span><span class="sxs-lookup"><span data-stu-id="43f52-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="43f52-110">Пример 2: удаление нескольких очередей хранилища</span><span class="sxs-lookup"><span data-stu-id="43f52-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue "Contoso*" | Remove-AzureStorageQueue
```

<span data-ttu-id="43f52-111">Эта команда удаляет все очереди с именами, которые начинаются с contoso.</span><span class="sxs-lookup"><span data-stu-id="43f52-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="43f52-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="43f52-112">PARAMETERS</span></span>

### <span data-ttu-id="43f52-113">-Context</span><span class="sxs-lookup"><span data-stu-id="43f52-113">-Context</span></span>
<span data-ttu-id="43f52-114">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="43f52-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="43f52-115">Чтобы получить контекст хранилища, New-AzureStorageContext командлет.</span><span class="sxs-lookup"><span data-stu-id="43f52-115">To obtain the storage context, the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="43f52-116">-Force</span><span class="sxs-lookup"><span data-stu-id="43f52-116">-Force</span></span>
<span data-ttu-id="43f52-117">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="43f52-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="43f52-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="43f52-118">-Name</span></span>
<span data-ttu-id="43f52-119">Указывает имя очереди, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="43f52-119">Specifies the name of the queue to remove.</span></span>

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

### <span data-ttu-id="43f52-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43f52-120">-PassThru</span></span>
<span data-ttu-id="43f52-121">Указывает на то, что этот командлет возвращает **логическое значение** , отражающее успешное выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="43f52-121">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="43f52-122">По умолчанию этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="43f52-122">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="43f52-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43f52-123">-Confirm</span></span>
<span data-ttu-id="43f52-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="43f52-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43f52-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43f52-125">-WhatIf</span></span>
<span data-ttu-id="43f52-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="43f52-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43f52-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="43f52-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43f52-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43f52-128">CommonParameters</span></span>
<span data-ttu-id="43f52-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="43f52-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43f52-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43f52-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43f52-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="43f52-131">INPUTS</span></span>

## <span data-ttu-id="43f52-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="43f52-132">OUTPUTS</span></span>

## <span data-ttu-id="43f52-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="43f52-133">NOTES</span></span>

## <span data-ttu-id="43f52-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="43f52-134">RELATED LINKS</span></span>

[<span data-ttu-id="43f52-135">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="43f52-135">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="43f52-136">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="43f52-136">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)
