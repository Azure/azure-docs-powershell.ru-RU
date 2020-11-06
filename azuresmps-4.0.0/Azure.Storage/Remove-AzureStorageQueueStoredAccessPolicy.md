---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: ''
schema: 2.0.0
ms.openlocfilehash: 116dcc8967ab18d0b67cd3e4eeea91190c38930f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556140"
---
# <span data-ttu-id="ee89c-101">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ee89c-101">Remove-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="ee89c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ee89c-102">SYNOPSIS</span></span>
<span data-ttu-id="ee89c-103">Удаляет политику сохраненного доступа из очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="ee89c-103">Removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="ee89c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ee89c-104">SYNTAX</span></span>

```
Remove-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee89c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee89c-105">DESCRIPTION</span></span>
<span data-ttu-id="ee89c-106">Командлет **Remove-AzureStorageQueueStoredAccessPolicy** удаляет политику сохраненного доступа из очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="ee89c-106">The **Remove-AzureStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="ee89c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ee89c-107">EXAMPLES</span></span>

### <span data-ttu-id="ee89c-108">Пример 1: Удаление политики сохраненного доступа из очереди хранилища</span><span class="sxs-lookup"><span data-stu-id="ee89c-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="ee89c-109">Эта команда удаляет политику доступа с именем Policy04 из очереди хранения с именем MyQueue.</span><span class="sxs-lookup"><span data-stu-id="ee89c-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="ee89c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ee89c-110">PARAMETERS</span></span>

### <span data-ttu-id="ee89c-111">-Context</span><span class="sxs-lookup"><span data-stu-id="ee89c-111">-Context</span></span>
<span data-ttu-id="ee89c-112">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="ee89c-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ee89c-113">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="ee89c-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ee89c-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee89c-114">-PassThru</span></span>
<span data-ttu-id="ee89c-115">Указывает на то, что этот командлет возвращает **логическое значение** , отражающее успешное выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="ee89c-115">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="ee89c-116">По умолчанию этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ee89c-116">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="ee89c-117">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="ee89c-117">-Policy</span></span>
<span data-ttu-id="ee89c-118">Указывает политику сохраненного доступа, которая включает разрешения для маркера данной подписи общего доступа (SAS).</span><span class="sxs-lookup"><span data-stu-id="ee89c-118">Specifies the stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="ee89c-119">-Очередь</span><span class="sxs-lookup"><span data-stu-id="ee89c-119">-Queue</span></span>
<span data-ttu-id="ee89c-120">Указывает имя очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="ee89c-120">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="ee89c-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee89c-121">-Confirm</span></span>
<span data-ttu-id="ee89c-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ee89c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee89c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee89c-123">-WhatIf</span></span>
<span data-ttu-id="ee89c-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ee89c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee89c-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ee89c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee89c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee89c-126">CommonParameters</span></span>
<span data-ttu-id="ee89c-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ee89c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee89c-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee89c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee89c-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ee89c-129">INPUTS</span></span>

## <span data-ttu-id="ee89c-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee89c-130">OUTPUTS</span></span>

## <span data-ttu-id="ee89c-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="ee89c-131">NOTES</span></span>

## <span data-ttu-id="ee89c-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ee89c-132">RELATED LINKS</span></span>

[<span data-ttu-id="ee89c-133">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ee89c-133">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="ee89c-134">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="ee89c-134">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="ee89c-135">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ee89c-135">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="ee89c-136">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ee89c-136">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)
