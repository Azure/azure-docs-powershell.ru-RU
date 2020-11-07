---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: ''
schema: 2.0.0
ms.openlocfilehash: fcb08eb9e63917d072630f81a2026d961a70dd27
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731712"
---
# <span data-ttu-id="c9342-101">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="c9342-101">Remove-AzureStorageTable</span></span>

## <span data-ttu-id="c9342-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c9342-102">SYNOPSIS</span></span>
<span data-ttu-id="c9342-103">Удаляет таблицу хранилища.</span><span class="sxs-lookup"><span data-stu-id="c9342-103">Removes a storage table.</span></span>

## <span data-ttu-id="c9342-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c9342-104">SYNTAX</span></span>

```
Remove-AzureStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9342-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9342-105">DESCRIPTION</span></span>
<span data-ttu-id="c9342-106">Командлет **Remove-AzureStorageTable** удаляет одну или несколько таблиц хранилища из учетной записи хранения в Azure.</span><span class="sxs-lookup"><span data-stu-id="c9342-106">The **Remove-AzureStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="c9342-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c9342-107">EXAMPLES</span></span>

### <span data-ttu-id="c9342-108">Пример 1: удаление таблицы</span><span class="sxs-lookup"><span data-stu-id="c9342-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzureStorageTable -Name "TableABC"
```

<span data-ttu-id="c9342-109">Эта команда удаляет таблицу.</span><span class="sxs-lookup"><span data-stu-id="c9342-109">This command removes a table.</span></span>

### <span data-ttu-id="c9342-110">Пример 2: удаление нескольких таблиц</span><span class="sxs-lookup"><span data-stu-id="c9342-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzureStorageTable table* | Remove-AzureStorageTable
```

<span data-ttu-id="c9342-111">В этом примере используется подстановочный знак с параметром *Name* для получения всех таблиц, соответствующих таблице шаблона, а затем передача результатов в конвейере для удаления таблиц.</span><span class="sxs-lookup"><span data-stu-id="c9342-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="c9342-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c9342-112">PARAMETERS</span></span>

### <span data-ttu-id="c9342-113">-Context</span><span class="sxs-lookup"><span data-stu-id="c9342-113">-Context</span></span>
<span data-ttu-id="c9342-114">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c9342-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="c9342-115">Вы можете создать его с помощью командлета New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="c9342-115">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c9342-116">-Force</span><span class="sxs-lookup"><span data-stu-id="c9342-116">-Force</span></span>
<span data-ttu-id="c9342-117">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="c9342-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c9342-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c9342-118">-Name</span></span>
<span data-ttu-id="c9342-119">Указывает имя таблицы, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="c9342-119">Specifies the name of the table to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9342-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c9342-120">-PassThru</span></span>
<span data-ttu-id="c9342-121">Указывает на то, что этот командлет возвращает **логическое значение** , отражающее успешное выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="c9342-121">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="c9342-122">По умолчанию этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c9342-122">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="c9342-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9342-123">-Confirm</span></span>
<span data-ttu-id="c9342-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c9342-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9342-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9342-125">-WhatIf</span></span>
<span data-ttu-id="c9342-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c9342-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9342-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c9342-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9342-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9342-128">CommonParameters</span></span>
<span data-ttu-id="c9342-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c9342-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9342-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9342-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9342-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c9342-131">INPUTS</span></span>

## <span data-ttu-id="c9342-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9342-132">OUTPUTS</span></span>

## <span data-ttu-id="c9342-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="c9342-133">NOTES</span></span>

## <span data-ttu-id="c9342-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c9342-134">RELATED LINKS</span></span>

[<span data-ttu-id="c9342-135">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="c9342-135">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)
