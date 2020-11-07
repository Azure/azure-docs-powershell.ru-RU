---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTable.md
ms.openlocfilehash: 77e011275a7861f54d25339fe46aad36cffe5e34
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907446"
---
# <span data-ttu-id="d356e-101">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="d356e-101">Remove-AzStorageTable</span></span>

## <span data-ttu-id="d356e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d356e-102">SYNOPSIS</span></span>
<span data-ttu-id="d356e-103">Удаляет таблицу хранилища.</span><span class="sxs-lookup"><span data-stu-id="d356e-103">Removes a storage table.</span></span>

## <span data-ttu-id="d356e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d356e-104">SYNTAX</span></span>

```
Remove-AzStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d356e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d356e-105">DESCRIPTION</span></span>
<span data-ttu-id="d356e-106">Командлет **Remove-AzStorageTable** удаляет одну или несколько таблиц хранилища из учетной записи хранения в Azure.</span><span class="sxs-lookup"><span data-stu-id="d356e-106">The **Remove-AzStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="d356e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d356e-107">EXAMPLES</span></span>

### <span data-ttu-id="d356e-108">Пример 1: удаление таблицы</span><span class="sxs-lookup"><span data-stu-id="d356e-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzStorageTable -Name "TableABC"
```

<span data-ttu-id="d356e-109">Эта команда удаляет таблицу.</span><span class="sxs-lookup"><span data-stu-id="d356e-109">This command removes a table.</span></span>

### <span data-ttu-id="d356e-110">Пример 2: удаление нескольких таблиц</span><span class="sxs-lookup"><span data-stu-id="d356e-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzStorageTable table* | Remove-AzStorageTable
```

<span data-ttu-id="d356e-111">В этом примере используется подстановочный знак с параметром *Name* для получения всех таблиц, соответствующих таблице шаблона, а затем передача результатов в конвейере для удаления таблиц.</span><span class="sxs-lookup"><span data-stu-id="d356e-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="d356e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d356e-112">PARAMETERS</span></span>

### <span data-ttu-id="d356e-113">-Context</span><span class="sxs-lookup"><span data-stu-id="d356e-113">-Context</span></span>
<span data-ttu-id="d356e-114">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="d356e-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="d356e-115">Вы можете создать его с помощью командлета New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="d356e-115">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d356e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d356e-116">-DefaultProfile</span></span>
<span data-ttu-id="d356e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d356e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d356e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d356e-118">-Force</span></span>
<span data-ttu-id="d356e-119">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="d356e-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d356e-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d356e-120">-Name</span></span>
<span data-ttu-id="d356e-121">Указывает имя таблицы, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="d356e-121">Specifies the name of the table to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d356e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d356e-122">-PassThru</span></span>
<span data-ttu-id="d356e-123">Указывает на то, что этот командлет возвращает **логическое значение** , отражающее успешное выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="d356e-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="d356e-124">По умолчанию этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d356e-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="d356e-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d356e-125">-Confirm</span></span>
<span data-ttu-id="d356e-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d356e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d356e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d356e-127">-WhatIf</span></span>
<span data-ttu-id="d356e-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d356e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d356e-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d356e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d356e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d356e-130">CommonParameters</span></span>
<span data-ttu-id="d356e-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d356e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d356e-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d356e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d356e-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d356e-133">INPUTS</span></span>

### <span data-ttu-id="d356e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d356e-134">System.String</span></span>

### <span data-ttu-id="d356e-135">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d356e-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d356e-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d356e-136">OUTPUTS</span></span>

### <span data-ttu-id="d356e-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d356e-137">System.Boolean</span></span>

## <span data-ttu-id="d356e-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="d356e-138">NOTES</span></span>

## <span data-ttu-id="d356e-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d356e-139">RELATED LINKS</span></span>

[<span data-ttu-id="d356e-140">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="d356e-140">Get-AzStorageTable</span></span>](./Get-AzStorageTable.md)
