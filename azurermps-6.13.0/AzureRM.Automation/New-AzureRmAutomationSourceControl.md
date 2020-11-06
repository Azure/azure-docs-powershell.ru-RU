---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationSourceControl.md
ms.openlocfilehash: d81d62e6ba391fb601817544d977f56e75522ba5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565949"
---
# <span data-ttu-id="5fe5b-101">New-AzureRmAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="5fe5b-101">New-AzureRmAutomationSourceControl</span></span>

## <span data-ttu-id="5fe5b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5fe5b-102">SYNOPSIS</span></span>
<span data-ttu-id="5fe5b-103">Создает элемент управления источником автоматизации.</span><span class="sxs-lookup"><span data-stu-id="5fe5b-103">Creates an A Automation source control.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fe5b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5fe5b-104">SYNTAX</span></span>

```
New-AzureRmAutomationSourceControl -Name <String> -RepoUrl <Uri> -SourceType <String>
 -AccessToken <SecureString> -FolderPath <String> [-Branch <String>] [-Description <String>] [-EnableAutoSync]
 [-DoNotPublishRunbook] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fe5b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5fe5b-105">DESCRIPTION</span></span>
<span data-ttu-id="5fe5b-106">Командлет New-AzureRmAutomationSourceControl создает конфигурацию для связывания моей учетной записи службы автоматизации Azure с приложением VSTS TFVC, VSTS Git или GitHub.</span><span class="sxs-lookup"><span data-stu-id="5fe5b-106">The New-AzureRmAutomationSourceControl cmdlet creates a configuration to link my Azure Automation account with my VSTS TFVC, VSTS Git or GitHub.</span></span>

## <span data-ttu-id="5fe5b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5fe5b-107">EXAMPLES</span></span>

### <span data-ttu-id="5fe5b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5fe5b-108">Example 1</span></span>
<span data-ttu-id="5fe5b-109">Создайте конфигурацию системы управления версиями, чтобы связать мою учетную запись службы автоматизации Azure с приложением "VSTS TFVC Project".</span><span class="sxs-lookup"><span data-stu-id="5fe5b-109">Create a source control configuration to link my Azure Automation account with my VSTS TFVC project.</span></span> <span data-ttu-id="5fe5b-110">В проектах TFVC отсутствуют ветви, поэтому параметр Branch не указан.</span><span class="sxs-lookup"><span data-stu-id="5fe5b-110">TFVC projects do not have branches, and therefore, the Branch parameter is not specified.</span></span>

```powershell
PS C:\> # VSTS Personal access token
PS C:\> $token = "vppmrabbs65axamofglyo66rjg6reddaa7xxgvaddd5555aaaaddxzbmma"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzureRmAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "VSTSNative" `
                                           -RepoUrl "https://contoso.visualstudio.com/ContosoProduction/_versionControl" `
                                           -SourceType "VsoTfvc" `
                                           -FolderPath "/Runbooks" `
                                           -AccessToken $accessToken

Name        SourceType Branch FolderPath AutoSync PublishRunbook RepoUrl
----        ---------- ------ ---------- -------- -------------- -------
VSTSNative  VsoTfvc            /Runbooks True     True           https://contoso.visualstudio.com/ContosoProduc...
```

### <span data-ttu-id="5fe5b-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5fe5b-111">Example 2</span></span>
<span data-ttu-id="5fe5b-112">Создайте конфигурацию системы управления версиями, чтобы связать мою учетную запись службы автоматизации Azure с проектом Git из VSTS.</span><span class="sxs-lookup"><span data-stu-id="5fe5b-112">Create a source control configuration to link my Azure Automation account with my VSTS Git project.</span></span>


```powershell
PS C:\> # VSTS Personal access token
PS C:\> $token = "vppmrabbs65axamofglyo66rjg6reddaa7xxgvaddd5555aaaaddxzbmma"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzureRmAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "VSTSGit" `
                                           -RepoUrl "https://contoso.visualstudio.com/_git/Finance" `
                                           -SourceType "VsoGit" `
                                           -Branch "Development" `
                                           -FolderPath "/" `
                                           -AccessToken $accessToken

Name    SourceType Branch      FolderPath AutoSync PublishRunbook RepoUrl
----    ---------- ------      ---------- -------- -------------- -------
VSTSGit VsoGit     Development /          True     True           https://contoso.visualstudio.com/_git/Finan...
```

### <span data-ttu-id="5fe5b-113">Пример 3</span><span class="sxs-lookup"><span data-stu-id="5fe5b-113">Example 3</span></span>
<span data-ttu-id="5fe5b-114">Создайте конфигурацию системы управления версиями, чтобы связать мою учетную запись службы автоматизации Azure с проектом GitHub.</span><span class="sxs-lookup"><span data-stu-id="5fe5b-114">Create a source control configuration to link my Azure Automation account with my GitHub project.</span></span>


```powershell
PS C:\> # GitHub access token
PS C:\> $token = "68b08011223aac8bdd3388913a44rrsaa84fdf"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzureRmAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "GitHub1" `
                                           -RepoUrl "https://github.com/Contoso/TestSourceControl.git" `
                                           -SourceType "GitHub" `
                                           -Branch "master" `
                                           -FolderPath "/Runbooks" `
                                           -AccessToken $accessToken

Name    SourceType Branch FolderPath AutoSync PublishRunbook RepoUrl
----    ---------- ------ ---------- -------- -------------- -------
GitHub1 GitHub     master /Runbooks  True     True           https://github.com/Contoso/TestSourceControl...
```

## <span data-ttu-id="5fe5b-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5fe5b-115">PARAMETERS</span></span>

### <span data-ttu-id="5fe5b-116">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="5fe5b-116">-AccessToken</span></span>
<span data-ttu-id="5fe5b-117">Маркер доступа к системе управления версиями.</span><span class="sxs-lookup"><span data-stu-id="5fe5b-117">The source control access token.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe5b-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5fe5b-118">-AutomationAccountName</span></span>
<span data-ttu-id="5fe5b-119">Имя учетной записи службы автоматизации.</span><span class="sxs-lookup"><span data-stu-id="5fe5b-119">The automation account name.</span></span>

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

### <span data-ttu-id="5fe5b-120">-Branch</span><span class="sxs-lookup"><span data-stu-id="5fe5b-120">-Branch</span></span>
<span data-ttu-id="5fe5b-121">Ветвь системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="5fe5b-121">The source control branch.</span></span>

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

### <span data-ttu-id="5fe5b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fe5b-122">-DefaultProfile</span></span>
<span data-ttu-id="5fe5b-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5fe5b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe5b-124">-Описание</span><span class="sxs-lookup"><span data-stu-id="5fe5b-124">-Description</span></span>
<span data-ttu-id="5fe5b-125">Описание элемента управления исходным кодом.</span><span class="sxs-lookup"><span data-stu-id="5fe5b-125">The source control description.</span></span>

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

### <span data-ttu-id="5fe5b-126">-DoNotPublishRunbook</span><span class="sxs-lookup"><span data-stu-id="5fe5b-126">-DoNotPublishRunbook</span></span>
<span data-ttu-id="5fe5b-127">Свойство publishRunbook исходного элемента управления.</span><span class="sxs-lookup"><span data-stu-id="5fe5b-127">The publishRunbook property of the source control.</span></span>
<span data-ttu-id="5fe5b-128">Если задано значение DoNotPublishRunbook, это означает, что пользовательские runbooks будут импортированы как "черновик".</span><span class="sxs-lookup"><span data-stu-id="5fe5b-128">If DoNotPublishRunbook is set, this means that user runbooks will be imported as 'Draft'.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe5b-129">-EnableAutoSync</span><span class="sxs-lookup"><span data-stu-id="5fe5b-129">-EnableAutoSync</span></span>
<span data-ttu-id="5fe5b-130">Свойство "Автосинхронизация" для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="5fe5b-130">The autoSync property for the source control.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe5b-131">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="5fe5b-131">-FolderPath</span></span>
<span data-ttu-id="5fe5b-132">Путь к папке системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="5fe5b-132">The source control folder path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe5b-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5fe5b-133">-Name</span></span>
<span data-ttu-id="5fe5b-134">Имя исходного элемента управления.</span><span class="sxs-lookup"><span data-stu-id="5fe5b-134">The source control name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe5b-135">-Перекресто</span><span class="sxs-lookup"><span data-stu-id="5fe5b-135">-RepoUrl</span></span>
<span data-ttu-id="5fe5b-136">URL-адрес репозитория системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="5fe5b-136">The source control repo url.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe5b-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fe5b-137">-ResourceGroupName</span></span>
<span data-ttu-id="5fe5b-138">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5fe5b-138">The resource group name.</span></span>

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

### <span data-ttu-id="5fe5b-139">-SourceType</span><span class="sxs-lookup"><span data-stu-id="5fe5b-139">-SourceType</span></span>
<span data-ttu-id="5fe5b-140">Тип системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="5fe5b-140">The source control type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GitHub, VsoGit, VsoTfvc

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe5b-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5fe5b-141">-Confirm</span></span>
<span data-ttu-id="5fe5b-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5fe5b-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fe5b-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fe5b-143">-WhatIf</span></span>
<span data-ttu-id="5fe5b-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5fe5b-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fe5b-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5fe5b-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fe5b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fe5b-146">CommonParameters</span></span>
<span data-ttu-id="5fe5b-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5fe5b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fe5b-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fe5b-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fe5b-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5fe5b-149">INPUTS</span></span>

### <span data-ttu-id="5fe5b-150">System. String</span><span class="sxs-lookup"><span data-stu-id="5fe5b-150">System.String</span></span>

## <span data-ttu-id="5fe5b-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5fe5b-151">OUTPUTS</span></span>

### <span data-ttu-id="5fe5b-152">Microsoft. Azure. Commands. Automation. Model. SourceControl</span><span class="sxs-lookup"><span data-stu-id="5fe5b-152">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="5fe5b-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="5fe5b-153">NOTES</span></span>

## <span data-ttu-id="5fe5b-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5fe5b-154">RELATED LINKS</span></span>
