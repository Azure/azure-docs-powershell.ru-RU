---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTable.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 013d53649cc579ae305ab738e6d2bd1138646a88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560599"
---
# <span data-ttu-id="aa8f3-101">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="aa8f3-101">Remove-AzureStorageTable</span></span>

## <span data-ttu-id="aa8f3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aa8f3-102">SYNOPSIS</span></span>
<span data-ttu-id="aa8f3-103">Удаляет таблицу хранилища.</span><span class="sxs-lookup"><span data-stu-id="aa8f3-103">Removes a storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa8f3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aa8f3-104">SYNTAX</span></span>

```
Remove-AzureStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa8f3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa8f3-105">DESCRIPTION</span></span>
<span data-ttu-id="aa8f3-106">Командлет **Remove-AzureStorageTable** удаляет одну или несколько таблиц хранилища из учетной записи хранения в Azure.</span><span class="sxs-lookup"><span data-stu-id="aa8f3-106">The **Remove-AzureStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="aa8f3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aa8f3-107">EXAMPLES</span></span>

### <span data-ttu-id="aa8f3-108">Пример 1: удаление таблицы</span><span class="sxs-lookup"><span data-stu-id="aa8f3-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzureStorageTable -Name "TableABC"
```

<span data-ttu-id="aa8f3-109">Эта команда удаляет таблицу.</span><span class="sxs-lookup"><span data-stu-id="aa8f3-109">This command removes a table.</span></span>

### <span data-ttu-id="aa8f3-110">Пример 2: удаление нескольких таблиц</span><span class="sxs-lookup"><span data-stu-id="aa8f3-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzureStorageTable table* | Remove-AzureStorageTable
```

<span data-ttu-id="aa8f3-111">В этом примере используется подстановочный знак с параметром *Name* для получения всех таблиц, соответствующих таблице шаблона, а затем передача результатов в конвейере для удаления таблиц.</span><span class="sxs-lookup"><span data-stu-id="aa8f3-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="aa8f3-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aa8f3-112">PARAMETERS</span></span>

### <span data-ttu-id="aa8f3-113">-Context</span><span class="sxs-lookup"><span data-stu-id="aa8f3-113">-Context</span></span>
<span data-ttu-id="aa8f3-114">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="aa8f3-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="aa8f3-115">Вы можете создать его с помощью командлета New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="aa8f3-115">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="aa8f3-116">-Force</span><span class="sxs-lookup"><span data-stu-id="aa8f3-116">-Force</span></span>
<span data-ttu-id="aa8f3-117">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="aa8f3-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="aa8f3-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="aa8f3-118">-Name</span></span>
<span data-ttu-id="aa8f3-119">Указывает имя таблицы, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="aa8f3-119">Specifies the name of the table to remove.</span></span>

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

### <span data-ttu-id="aa8f3-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa8f3-120">-PassThru</span></span>
<span data-ttu-id="aa8f3-121">Указывает на то, что этот командлет возвращает **логическое значение** , отражающее успешное выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="aa8f3-121">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="aa8f3-122">По умолчанию этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="aa8f3-122">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="aa8f3-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa8f3-123">-Confirm</span></span>
<span data-ttu-id="aa8f3-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="aa8f3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa8f3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa8f3-125">-WhatIf</span></span>
<span data-ttu-id="aa8f3-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="aa8f3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa8f3-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="aa8f3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa8f3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa8f3-128">CommonParameters</span></span>
<span data-ttu-id="aa8f3-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aa8f3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa8f3-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa8f3-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa8f3-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aa8f3-131">INPUTS</span></span>

### <span data-ttu-id="aa8f3-132">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="aa8f3-132">IStorageContext</span></span>

<span data-ttu-id="aa8f3-133">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="aa8f3-133">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="aa8f3-134">Подстрок</span><span class="sxs-lookup"><span data-stu-id="aa8f3-134">String</span></span>

<span data-ttu-id="aa8f3-135">Параметр Name принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="aa8f3-135">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="aa8f3-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa8f3-136">OUTPUTS</span></span>

### <span data-ttu-id="aa8f3-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="aa8f3-137">System.Boolean</span></span>

## <span data-ttu-id="aa8f3-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="aa8f3-138">NOTES</span></span>

## <span data-ttu-id="aa8f3-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aa8f3-139">RELATED LINKS</span></span>

[<span data-ttu-id="aa8f3-140">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="aa8f3-140">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)
