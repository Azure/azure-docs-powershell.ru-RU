---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/update-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Update-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Update-AzAutomationSourceControl.md
ms.openlocfilehash: 7786431232f9570557593d2fbdde65a21e34f9bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731478"
---
# <span data-ttu-id="bcea5-101">Update-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="bcea5-101">Update-AzAutomationSourceControl</span></span>

## <span data-ttu-id="bcea5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bcea5-102">SYNOPSIS</span></span>
<span data-ttu-id="bcea5-103">Обновляет элемент управления источником автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="bcea5-103">Updates an Azure Automation source control.</span></span>

## <span data-ttu-id="bcea5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bcea5-104">SYNTAX</span></span>

```
Update-AzAutomationSourceControl -Name <String> [-AccessToken <SecureString>] [-FolderPath <String>]
 [-Branch <String>] [-Description <String>] [-AutoSync <Boolean>] [-PublishRunbook <Boolean>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcea5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bcea5-105">DESCRIPTION</span></span>
<span data-ttu-id="bcea5-106">Командлет Update-AzAutomationSourceControl изменяет значение поля в системе управления версиями в Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="bcea5-106">The Update-AzAutomationSourceControl cmdlet modifies the value of a field in a source control in Azure Automation.</span></span>

## <span data-ttu-id="bcea5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bcea5-107">EXAMPLES</span></span>

### <span data-ttu-id="bcea5-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bcea5-108">Example 1</span></span>
<span data-ttu-id="bcea5-109">Эти команды устанавливают в поле PublishRunbook значение false для элемента управления источником автоматизации Azure с именем VSTSNative в учетной записи с именем devAccount.</span><span class="sxs-lookup"><span data-stu-id="bcea5-109">This commands sets the PublishRunbook field to false for the Azure Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
Update-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                      -AutomationAccountName "devAccount" `
                                      -Name "VSTSNative" `
                                      -PublishRunbook $false 

Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    False          https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="bcea5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bcea5-110">PARAMETERS</span></span>

### <span data-ttu-id="bcea5-111">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="bcea5-111">-AccessToken</span></span>
<span data-ttu-id="bcea5-112">Маркер доступа к системе управления версиями.</span><span class="sxs-lookup"><span data-stu-id="bcea5-112">The source control access token.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcea5-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bcea5-113">-AutomationAccountName</span></span>
<span data-ttu-id="bcea5-114">Имя учетной записи службы автоматизации.</span><span class="sxs-lookup"><span data-stu-id="bcea5-114">The automation account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcea5-115">-Синхронизация</span><span class="sxs-lookup"><span data-stu-id="bcea5-115">-AutoSync</span></span>
<span data-ttu-id="bcea5-116">Свойство "Автосинхронизация" для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="bcea5-116">The autoSync property for the source control.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcea5-117">-Branch</span><span class="sxs-lookup"><span data-stu-id="bcea5-117">-Branch</span></span>
<span data-ttu-id="bcea5-118">Ветвь системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="bcea5-118">The source control branch.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcea5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcea5-119">-DefaultProfile</span></span>
<span data-ttu-id="bcea5-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bcea5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcea5-121">-Описание</span><span class="sxs-lookup"><span data-stu-id="bcea5-121">-Description</span></span>
<span data-ttu-id="bcea5-122">Описание элемента управления исходным кодом.</span><span class="sxs-lookup"><span data-stu-id="bcea5-122">The source control description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcea5-123">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="bcea5-123">-FolderPath</span></span>
<span data-ttu-id="bcea5-124">Путь к папке системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="bcea5-124">The source control folder path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcea5-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bcea5-125">-Name</span></span>
<span data-ttu-id="bcea5-126">Имя исходного элемента управления.</span><span class="sxs-lookup"><span data-stu-id="bcea5-126">The source control name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcea5-127">-PublishRunbook</span><span class="sxs-lookup"><span data-stu-id="bcea5-127">-PublishRunbook</span></span>
<span data-ttu-id="bcea5-128">Свойство publishRunbook исходного элемента управления.</span><span class="sxs-lookup"><span data-stu-id="bcea5-128">The publishRunbook property of the source control.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcea5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcea5-129">-ResourceGroupName</span></span>
<span data-ttu-id="bcea5-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bcea5-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcea5-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bcea5-131">-Confirm</span></span>
<span data-ttu-id="bcea5-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bcea5-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcea5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcea5-133">-WhatIf</span></span>
<span data-ttu-id="bcea5-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bcea5-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bcea5-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bcea5-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcea5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcea5-136">CommonParameters</span></span>
<span data-ttu-id="bcea5-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bcea5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcea5-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcea5-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcea5-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bcea5-139">INPUTS</span></span>

### <span data-ttu-id="bcea5-140">System. String</span><span class="sxs-lookup"><span data-stu-id="bcea5-140">System.String</span></span>

## <span data-ttu-id="bcea5-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bcea5-141">OUTPUTS</span></span>

### <span data-ttu-id="bcea5-142">Microsoft. Azure. Commands. Automation. Model. SourceControl</span><span class="sxs-lookup"><span data-stu-id="bcea5-142">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="bcea5-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="bcea5-143">NOTES</span></span>

## <span data-ttu-id="bcea5-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bcea5-144">RELATED LINKS</span></span>
