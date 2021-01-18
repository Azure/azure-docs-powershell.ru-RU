---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTable.md
ms.openlocfilehash: 98ffbfe7153ba0592563b21695e1a4d1c227f99a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517025"
---
# <span data-ttu-id="67861-101">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="67861-101">Remove-AzStorageTable</span></span>

## <span data-ttu-id="67861-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67861-102">SYNOPSIS</span></span>
<span data-ttu-id="67861-103">Удаляет таблицу хранилища.</span><span class="sxs-lookup"><span data-stu-id="67861-103">Removes a storage table.</span></span>

## <span data-ttu-id="67861-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="67861-104">SYNTAX</span></span>

```
Remove-AzStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67861-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="67861-105">DESCRIPTION</span></span>
<span data-ttu-id="67861-106">С **его учетной записью** в Azure удаляется одна или несколько таблиц хранилища.</span><span class="sxs-lookup"><span data-stu-id="67861-106">The **Remove-AzStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="67861-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="67861-107">EXAMPLES</span></span>

### <span data-ttu-id="67861-108">Пример 1. Удаление таблицы</span><span class="sxs-lookup"><span data-stu-id="67861-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzStorageTable -Name "TableABC"
```

<span data-ttu-id="67861-109">Эта команда удаляет таблицу.</span><span class="sxs-lookup"><span data-stu-id="67861-109">This command removes a table.</span></span>

### <span data-ttu-id="67861-110">Пример 2. Удаление нескольких таблиц</span><span class="sxs-lookup"><span data-stu-id="67861-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzStorageTable table* | Remove-AzStorageTable
```

<span data-ttu-id="67861-111">В этом примере используется поддиавка с параметром *Name* для получения всех таблиц, которые соответствуют шаблонной таблице, а затем передает результат в конвейере для их удаления.</span><span class="sxs-lookup"><span data-stu-id="67861-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="67861-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67861-112">PARAMETERS</span></span>

### <span data-ttu-id="67861-113">-Контекст</span><span class="sxs-lookup"><span data-stu-id="67861-113">-Context</span></span>
<span data-ttu-id="67861-114">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="67861-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="67861-115">Его можно создать с помощью New-AzStorageContext-управления.</span><span class="sxs-lookup"><span data-stu-id="67861-115">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="67861-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67861-116">-DefaultProfile</span></span>
<span data-ttu-id="67861-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="67861-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67861-118">-Force</span><span class="sxs-lookup"><span data-stu-id="67861-118">-Force</span></span>
<span data-ttu-id="67861-119">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="67861-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="67861-120">-Name</span><span class="sxs-lookup"><span data-stu-id="67861-120">-Name</span></span>
<span data-ttu-id="67861-121">Указывает имя таблицы, которая будет удаляться.</span><span class="sxs-lookup"><span data-stu-id="67861-121">Specifies the name of the table to remove.</span></span>

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

### <span data-ttu-id="67861-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67861-122">-PassThru</span></span>
<span data-ttu-id="67861-123">Указывает на то, что этот cmdlet возвращает **boolean,** который отражает успешность операции.</span><span class="sxs-lookup"><span data-stu-id="67861-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="67861-124">По умолчанию этот cmdlet не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="67861-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="67861-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67861-125">-Confirm</span></span>
<span data-ttu-id="67861-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67861-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67861-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67861-127">-WhatIf</span></span>
<span data-ttu-id="67861-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67861-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67861-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="67861-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67861-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67861-130">CommonParameters</span></span>
<span data-ttu-id="67861-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67861-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67861-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67861-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67861-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="67861-133">INPUTS</span></span>

### <span data-ttu-id="67861-134">System.String</span><span class="sxs-lookup"><span data-stu-id="67861-134">System.String</span></span>

### <span data-ttu-id="67861-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="67861-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="67861-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="67861-136">OUTPUTS</span></span>

### <span data-ttu-id="67861-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="67861-137">System.Boolean</span></span>

## <span data-ttu-id="67861-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="67861-138">NOTES</span></span>

## <span data-ttu-id="67861-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="67861-139">RELATED LINKS</span></span>

[<span data-ttu-id="67861-140">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="67861-140">Get-AzStorageTable</span></span>](./Get-AzStorageTable.md)
