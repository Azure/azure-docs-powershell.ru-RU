---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: ''
schema: 2.0.0
ms.openlocfilehash: c3276a23869633238ebc6b84dfa01934e5ad9896
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555456"
---
# <span data-ttu-id="b52df-101">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b52df-101">Remove-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="b52df-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b52df-102">SYNOPSIS</span></span>
<span data-ttu-id="b52df-103">Удаляет политику сохраненного доступа из таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="b52df-103">Removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="b52df-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b52df-104">SYNTAX</span></span>

```
Remove-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b52df-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b52df-105">DESCRIPTION</span></span>
<span data-ttu-id="b52df-106">Командлет **Remove-AzureStorageTableStoredAccessPolicy** удаляет политику сохраненного доступа из таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="b52df-106">The **Remove-AzureStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="b52df-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b52df-107">EXAMPLES</span></span>

### <span data-ttu-id="b52df-108">Пример 1: Удаление политики сохраненных прав доступа из таблицы хранилища</span><span class="sxs-lookup"><span data-stu-id="b52df-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="b52df-109">Эта команда удаляет политику с именем Policy05 из таблицы хранения с именем MyTable.</span><span class="sxs-lookup"><span data-stu-id="b52df-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="b52df-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b52df-110">PARAMETERS</span></span>

### <span data-ttu-id="b52df-111">-Context</span><span class="sxs-lookup"><span data-stu-id="b52df-111">-Context</span></span>
<span data-ttu-id="b52df-112">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="b52df-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b52df-113">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="b52df-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b52df-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b52df-114">-PassThru</span></span>
<span data-ttu-id="b52df-115">Указывает на то, что этот командлет возвращает **логическое значение** , отражающее успешное выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="b52df-115">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="b52df-116">По умолчанию этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b52df-116">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="b52df-117">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="b52df-117">-Policy</span></span>
<span data-ttu-id="b52df-118">Указывает политику сохраненного доступа, которая включает разрешения для этого маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="b52df-118">Specifies the stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="b52df-119">-Таблица</span><span class="sxs-lookup"><span data-stu-id="b52df-119">-Table</span></span>
<span data-ttu-id="b52df-120">Указывает имя таблицы Azure.</span><span class="sxs-lookup"><span data-stu-id="b52df-120">Specifies the Azure table name.</span></span>

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

### <span data-ttu-id="b52df-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b52df-121">-Confirm</span></span>
<span data-ttu-id="b52df-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b52df-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b52df-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b52df-123">-WhatIf</span></span>
<span data-ttu-id="b52df-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b52df-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b52df-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b52df-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b52df-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b52df-126">CommonParameters</span></span>
<span data-ttu-id="b52df-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b52df-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b52df-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b52df-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b52df-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b52df-129">INPUTS</span></span>

## <span data-ttu-id="b52df-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b52df-130">OUTPUTS</span></span>

## <span data-ttu-id="b52df-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="b52df-131">NOTES</span></span>

## <span data-ttu-id="b52df-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b52df-132">RELATED LINKS</span></span>

[<span data-ttu-id="b52df-133">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b52df-133">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="b52df-134">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="b52df-134">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="b52df-135">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b52df-135">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="b52df-136">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b52df-136">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)
