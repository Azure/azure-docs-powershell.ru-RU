---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSourceControl.md
ms.openlocfilehash: 17d1c7c94726543aa30a032423576c8a7dcb6fcc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315290"
---
# <span data-ttu-id="d947c-101">New-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="d947c-101">New-AzAutomationSourceControl</span></span>

## <span data-ttu-id="d947c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d947c-102">SYNOPSIS</span></span>
<span data-ttu-id="d947c-103">Создает элемент управления источником автоматизации.</span><span class="sxs-lookup"><span data-stu-id="d947c-103">Creates an A Automation source control.</span></span>

## <span data-ttu-id="d947c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d947c-104">SYNTAX</span></span>

```
New-AzAutomationSourceControl -Name <String> -RepoUrl <Uri> -SourceType <String> -AccessToken <SecureString>
 -FolderPath <String> [-Branch <String>] [-Description <String>] [-EnableAutoSync] [-DoNotPublishRunbook]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d947c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d947c-105">DESCRIPTION</span></span>
<span data-ttu-id="d947c-106">Командлет New-AzAutomationSourceControl создает конфигурацию для связывания моей учетной записи службы автоматизации Azure с приложением VSTS TFVC, VSTS Git или GitHub.</span><span class="sxs-lookup"><span data-stu-id="d947c-106">The New-AzAutomationSourceControl cmdlet creates a configuration to link my Azure Automation account with my VSTS TFVC, VSTS Git or GitHub.</span></span>

## <span data-ttu-id="d947c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d947c-107">EXAMPLES</span></span>

### <span data-ttu-id="d947c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d947c-108">Example 1</span></span>
<span data-ttu-id="d947c-109">Создайте конфигурацию системы управления версиями, чтобы связать мою учетную запись службы автоматизации Azure с приложением "VSTS TFVC Project".</span><span class="sxs-lookup"><span data-stu-id="d947c-109">Create a source control configuration to link my Azure Automation account with my VSTS TFVC project.</span></span> <span data-ttu-id="d947c-110">В проектах TFVC отсутствуют ветви, поэтому параметр Branch не указан.</span><span class="sxs-lookup"><span data-stu-id="d947c-110">TFVC projects do not have branches, and therefore, the Branch parameter is not specified.</span></span>

```powershell
PS C:\> # VSTS Personal access token
PS C:\> $token = "vppmrabbs65axamofglyo66rjg6reddaa7xxgvaddd5555aaaaddxzbmma"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzAutomationSourceControl -ResourceGroupName "rg1" `
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

### <span data-ttu-id="d947c-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d947c-111">Example 2</span></span>
<span data-ttu-id="d947c-112">Создайте конфигурацию системы управления версиями, чтобы связать мою учетную запись службы автоматизации Azure с проектом Git из VSTS.</span><span class="sxs-lookup"><span data-stu-id="d947c-112">Create a source control configuration to link my Azure Automation account with my VSTS Git project.</span></span>


```powershell
PS C:\> # VSTS Personal access token
PS C:\> $token = "vppmrabbs65axamofglyo66rjg6reddaa7xxgvaddd5555aaaaddxzbmma"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzAutomationSourceControl -ResourceGroupName "rg1" `
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

### <span data-ttu-id="d947c-113">Пример 3</span><span class="sxs-lookup"><span data-stu-id="d947c-113">Example 3</span></span>
<span data-ttu-id="d947c-114">Создайте конфигурацию системы управления версиями, чтобы связать мою учетную запись службы автоматизации Azure с проектом GitHub.</span><span class="sxs-lookup"><span data-stu-id="d947c-114">Create a source control configuration to link my Azure Automation account with my GitHub project.</span></span>


```powershell
PS C:\> # GitHub access token
PS C:\> $token = "68b08011223aac8bdd3388913a44rrsaa84fdf"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzAutomationSourceControl -ResourceGroupName "rg1" `
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

## <span data-ttu-id="d947c-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d947c-115">PARAMETERS</span></span>

### <span data-ttu-id="d947c-116">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="d947c-116">-AccessToken</span></span>
<span data-ttu-id="d947c-117">Маркер доступа к системе управления версиями.</span><span class="sxs-lookup"><span data-stu-id="d947c-117">The source control access token.</span></span>

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

### <span data-ttu-id="d947c-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d947c-118">-AutomationAccountName</span></span>
<span data-ttu-id="d947c-119">Имя учетной записи службы автоматизации.</span><span class="sxs-lookup"><span data-stu-id="d947c-119">The automation account name.</span></span>

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

### <span data-ttu-id="d947c-120">-Branch</span><span class="sxs-lookup"><span data-stu-id="d947c-120">-Branch</span></span>
<span data-ttu-id="d947c-121">Ветвь системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="d947c-121">The source control branch.</span></span>

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

### <span data-ttu-id="d947c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d947c-122">-DefaultProfile</span></span>
<span data-ttu-id="d947c-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d947c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d947c-124">-Описание</span><span class="sxs-lookup"><span data-stu-id="d947c-124">-Description</span></span>
<span data-ttu-id="d947c-125">Описание элемента управления исходным кодом.</span><span class="sxs-lookup"><span data-stu-id="d947c-125">The source control description.</span></span>

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

### <span data-ttu-id="d947c-126">-DoNotPublishRunbook</span><span class="sxs-lookup"><span data-stu-id="d947c-126">-DoNotPublishRunbook</span></span>
<span data-ttu-id="d947c-127">Свойство publishRunbook исходного элемента управления.</span><span class="sxs-lookup"><span data-stu-id="d947c-127">The publishRunbook property of the source control.</span></span>
<span data-ttu-id="d947c-128">Если задано значение DoNotPublishRunbook, это означает, что пользовательские runbooks будут импортированы как "черновик".</span><span class="sxs-lookup"><span data-stu-id="d947c-128">If DoNotPublishRunbook is set, this means that user runbooks will be imported as 'Draft'.</span></span>

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

### <span data-ttu-id="d947c-129">-EnableAutoSync</span><span class="sxs-lookup"><span data-stu-id="d947c-129">-EnableAutoSync</span></span>
<span data-ttu-id="d947c-130">Свойство "Автосинхронизация" для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="d947c-130">The autoSync property for the source control.</span></span>

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

### <span data-ttu-id="d947c-131">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="d947c-131">-FolderPath</span></span>
<span data-ttu-id="d947c-132">Путь к папке системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="d947c-132">The source control folder path.</span></span>

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

### <span data-ttu-id="d947c-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d947c-133">-Name</span></span>
<span data-ttu-id="d947c-134">Имя исходного элемента управления.</span><span class="sxs-lookup"><span data-stu-id="d947c-134">The source control name.</span></span>

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

### <span data-ttu-id="d947c-135">-Перекресто</span><span class="sxs-lookup"><span data-stu-id="d947c-135">-RepoUrl</span></span>
<span data-ttu-id="d947c-136">URL-адрес репозитория системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="d947c-136">The source control repo url.</span></span>

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

### <span data-ttu-id="d947c-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d947c-137">-ResourceGroupName</span></span>
<span data-ttu-id="d947c-138">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d947c-138">The resource group name.</span></span>

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

### <span data-ttu-id="d947c-139">-SourceType</span><span class="sxs-lookup"><span data-stu-id="d947c-139">-SourceType</span></span>
<span data-ttu-id="d947c-140">Тип системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="d947c-140">The source control type.</span></span>

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

### <span data-ttu-id="d947c-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d947c-141">-Confirm</span></span>
<span data-ttu-id="d947c-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d947c-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d947c-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d947c-143">-WhatIf</span></span>
<span data-ttu-id="d947c-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d947c-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d947c-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d947c-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d947c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d947c-146">CommonParameters</span></span>
<span data-ttu-id="d947c-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d947c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d947c-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d947c-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d947c-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d947c-149">INPUTS</span></span>

### <span data-ttu-id="d947c-150">System. String</span><span class="sxs-lookup"><span data-stu-id="d947c-150">System.String</span></span>

## <span data-ttu-id="d947c-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d947c-151">OUTPUTS</span></span>

### <span data-ttu-id="d947c-152">Microsoft. Azure. Commands. Automation. Model. SourceControl</span><span class="sxs-lookup"><span data-stu-id="d947c-152">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="d947c-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="d947c-153">NOTES</span></span>

## <span data-ttu-id="d947c-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d947c-154">RELATED LINKS</span></span>
