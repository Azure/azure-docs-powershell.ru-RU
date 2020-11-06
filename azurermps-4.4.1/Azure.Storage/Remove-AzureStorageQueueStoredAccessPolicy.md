---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueueStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 94c5bc28ae381227366b5461b51a2da7fd6feccd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565763"
---
# <span data-ttu-id="20bee-101">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="20bee-101">Remove-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="20bee-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="20bee-102">SYNOPSIS</span></span>
<span data-ttu-id="20bee-103">Удаляет политику сохраненного доступа из очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="20bee-103">Removes a stored access policy from an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20bee-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="20bee-104">SYNTAX</span></span>

```
Remove-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20bee-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="20bee-105">DESCRIPTION</span></span>
<span data-ttu-id="20bee-106">Командлет **Remove-AzureStorageQueueStoredAccessPolicy** удаляет политику сохраненного доступа из очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="20bee-106">The **Remove-AzureStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="20bee-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="20bee-107">EXAMPLES</span></span>

### <span data-ttu-id="20bee-108">Пример 1: Удаление политики сохраненного доступа из очереди хранилища</span><span class="sxs-lookup"><span data-stu-id="20bee-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="20bee-109">Эта команда удаляет политику доступа с именем Policy04 из очереди хранения с именем MyQueue.</span><span class="sxs-lookup"><span data-stu-id="20bee-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="20bee-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="20bee-110">PARAMETERS</span></span>

### <span data-ttu-id="20bee-111">-Context</span><span class="sxs-lookup"><span data-stu-id="20bee-111">-Context</span></span>
<span data-ttu-id="20bee-112">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="20bee-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="20bee-113">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="20bee-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="20bee-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20bee-114">-PassThru</span></span>
<span data-ttu-id="20bee-115">Указывает на то, что этот командлет возвращает **логическое значение** , отражающее успешное выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="20bee-115">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="20bee-116">По умолчанию этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="20bee-116">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="20bee-117">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="20bee-117">-Policy</span></span>
<span data-ttu-id="20bee-118">Указывает имя политики хранения, которая удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="20bee-118">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20bee-119">-Очередь</span><span class="sxs-lookup"><span data-stu-id="20bee-119">-Queue</span></span>
<span data-ttu-id="20bee-120">Указывает имя очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="20bee-120">Specifies the Azure storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20bee-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="20bee-121">-Confirm</span></span>
<span data-ttu-id="20bee-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="20bee-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20bee-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20bee-123">-WhatIf</span></span>
<span data-ttu-id="20bee-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="20bee-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20bee-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="20bee-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20bee-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20bee-126">CommonParameters</span></span>
<span data-ttu-id="20bee-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="20bee-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20bee-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20bee-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20bee-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="20bee-129">INPUTS</span></span>

### <span data-ttu-id="20bee-130">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="20bee-130">IStorageContext</span></span>

<span data-ttu-id="20bee-131">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="20bee-131">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="20bee-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="20bee-132">OUTPUTS</span></span>

### <span data-ttu-id="20bee-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="20bee-133">System.Boolean</span></span>

## <span data-ttu-id="20bee-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="20bee-134">NOTES</span></span>

## <span data-ttu-id="20bee-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="20bee-135">RELATED LINKS</span></span>

[<span data-ttu-id="20bee-136">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="20bee-136">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="20bee-137">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="20bee-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="20bee-138">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="20bee-138">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="20bee-139">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="20bee-139">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)
