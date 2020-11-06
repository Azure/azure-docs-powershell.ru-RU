---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTableStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 7ee384fb26ed8e16b377800fc7e3912f33b81669
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560596"
---
# <span data-ttu-id="19dcc-101">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="19dcc-101">Remove-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="19dcc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="19dcc-102">SYNOPSIS</span></span>
<span data-ttu-id="19dcc-103">Удаляет политику сохраненного доступа из таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="19dcc-103">Removes a stored access policy from an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19dcc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="19dcc-104">SYNTAX</span></span>

```
Remove-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19dcc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19dcc-105">DESCRIPTION</span></span>
<span data-ttu-id="19dcc-106">Командлет **Remove-AzureStorageTableStoredAccessPolicy** удаляет политику сохраненного доступа из таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="19dcc-106">The **Remove-AzureStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="19dcc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="19dcc-107">EXAMPLES</span></span>

### <span data-ttu-id="19dcc-108">Пример 1: Удаление политики сохраненных прав доступа из таблицы хранилища</span><span class="sxs-lookup"><span data-stu-id="19dcc-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="19dcc-109">Эта команда удаляет политику с именем Policy05 из таблицы хранения с именем MyTable.</span><span class="sxs-lookup"><span data-stu-id="19dcc-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="19dcc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="19dcc-110">PARAMETERS</span></span>

### <span data-ttu-id="19dcc-111">-Context</span><span class="sxs-lookup"><span data-stu-id="19dcc-111">-Context</span></span>
<span data-ttu-id="19dcc-112">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="19dcc-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="19dcc-113">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="19dcc-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="19dcc-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19dcc-114">-PassThru</span></span>
<span data-ttu-id="19dcc-115">Указывает на то, что этот командлет возвращает **логическое значение** , отражающее успешное выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="19dcc-115">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="19dcc-116">По умолчанию этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="19dcc-116">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="19dcc-117">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="19dcc-117">-Policy</span></span>
<span data-ttu-id="19dcc-118">Указывает имя политики хранения, которая удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="19dcc-118">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="19dcc-119">-Таблица</span><span class="sxs-lookup"><span data-stu-id="19dcc-119">-Table</span></span>
<span data-ttu-id="19dcc-120">Указывает имя таблицы Azure.</span><span class="sxs-lookup"><span data-stu-id="19dcc-120">Specifies the Azure table name.</span></span>

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

### <span data-ttu-id="19dcc-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19dcc-121">-Confirm</span></span>
<span data-ttu-id="19dcc-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="19dcc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19dcc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19dcc-123">-WhatIf</span></span>
<span data-ttu-id="19dcc-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="19dcc-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19dcc-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="19dcc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19dcc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19dcc-126">CommonParameters</span></span>
<span data-ttu-id="19dcc-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="19dcc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19dcc-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19dcc-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19dcc-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="19dcc-129">INPUTS</span></span>

### <span data-ttu-id="19dcc-130">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="19dcc-130">IStorageContext</span></span>

<span data-ttu-id="19dcc-131">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="19dcc-131">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="19dcc-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="19dcc-132">OUTPUTS</span></span>

### <span data-ttu-id="19dcc-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="19dcc-133">System.Boolean</span></span>

## <span data-ttu-id="19dcc-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="19dcc-134">NOTES</span></span>

## <span data-ttu-id="19dcc-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19dcc-135">RELATED LINKS</span></span>

[<span data-ttu-id="19dcc-136">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="19dcc-136">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="19dcc-137">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="19dcc-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="19dcc-138">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="19dcc-138">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="19dcc-139">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="19dcc-139">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)
