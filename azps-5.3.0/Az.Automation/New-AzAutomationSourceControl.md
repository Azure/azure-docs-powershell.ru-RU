---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSourceControl.md
ms.openlocfilehash: 17d1c7c94726543aa30a032423576c8a7dcb6fcc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509962"
---
# <span data-ttu-id="6a247-101">New-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="6a247-101">New-AzAutomationSourceControl</span></span>

## <span data-ttu-id="6a247-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a247-102">SYNOPSIS</span></span>
<span data-ttu-id="6a247-103">Создает исходный контроль автоматизации.</span><span class="sxs-lookup"><span data-stu-id="6a247-103">Creates an A Automation source control.</span></span>

## <span data-ttu-id="6a247-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6a247-104">SYNTAX</span></span>

```
New-AzAutomationSourceControl -Name <String> -RepoUrl <Uri> -SourceType <String> -AccessToken <SecureString>
 -FolderPath <String> [-Branch <String>] [-Description <String>] [-EnableAutoSync] [-DoNotPublishRunbook]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a247-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a247-105">DESCRIPTION</span></span>
<span data-ttu-id="6a247-106">С New-AzAutomationSourceControl создается конфигурация для связываия учетной записи автоматизации Azure с TFVC VSTS, VSTS Git или GitHub.</span><span class="sxs-lookup"><span data-stu-id="6a247-106">The New-AzAutomationSourceControl cmdlet creates a configuration to link my Azure Automation account with my VSTS TFVC, VSTS Git or GitHub.</span></span>

## <span data-ttu-id="6a247-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6a247-107">EXAMPLES</span></span>

### <span data-ttu-id="6a247-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6a247-108">Example 1</span></span>
<span data-ttu-id="6a247-109">Создайте конфигурацию управления источником, чтобы связать учетную запись автоматизации Azure с проектом TFVC VSTS.</span><span class="sxs-lookup"><span data-stu-id="6a247-109">Create a source control configuration to link my Azure Automation account with my VSTS TFVC project.</span></span> <span data-ttu-id="6a247-110">В проектах TFVC нет ветвей, поэтому параметр Branch не указан.</span><span class="sxs-lookup"><span data-stu-id="6a247-110">TFVC projects do not have branches, and therefore, the Branch parameter is not specified.</span></span>

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

### <span data-ttu-id="6a247-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6a247-111">Example 2</span></span>
<span data-ttu-id="6a247-112">Создайте конфигурацию управления источником, чтобы связать учетную запись автоматизации Azure с проектом VSTS GIT.</span><span class="sxs-lookup"><span data-stu-id="6a247-112">Create a source control configuration to link my Azure Automation account with my VSTS Git project.</span></span>


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

### <span data-ttu-id="6a247-113">Пример 3</span><span class="sxs-lookup"><span data-stu-id="6a247-113">Example 3</span></span>
<span data-ttu-id="6a247-114">Создайте конфигурацию управления источником, чтобы связать учетную запись автоматизации Azure с проектом GitHub.</span><span class="sxs-lookup"><span data-stu-id="6a247-114">Create a source control configuration to link my Azure Automation account with my GitHub project.</span></span>


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

## <span data-ttu-id="6a247-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a247-115">PARAMETERS</span></span>

### <span data-ttu-id="6a247-116">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="6a247-116">-AccessToken</span></span>
<span data-ttu-id="6a247-117">Маркер доступа к источнику управления.</span><span class="sxs-lookup"><span data-stu-id="6a247-117">The source control access token.</span></span>

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

### <span data-ttu-id="6a247-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6a247-118">-AutomationAccountName</span></span>
<span data-ttu-id="6a247-119">Имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="6a247-119">The automation account name.</span></span>

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

### <span data-ttu-id="6a247-120">-Branch</span><span class="sxs-lookup"><span data-stu-id="6a247-120">-Branch</span></span>
<span data-ttu-id="6a247-121">Ветвь управления "Источник".</span><span class="sxs-lookup"><span data-stu-id="6a247-121">The source control branch.</span></span>

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

### <span data-ttu-id="6a247-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a247-122">-DefaultProfile</span></span>
<span data-ttu-id="6a247-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6a247-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a247-124">-Description</span><span class="sxs-lookup"><span data-stu-id="6a247-124">-Description</span></span>
<span data-ttu-id="6a247-125">Описание источника.</span><span class="sxs-lookup"><span data-stu-id="6a247-125">The source control description.</span></span>

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

### <span data-ttu-id="6a247-126">-DoNotPublishRunbook</span><span class="sxs-lookup"><span data-stu-id="6a247-126">-DoNotPublishRunbook</span></span>
<span data-ttu-id="6a247-127">Свойство publishRunbook (Книга публикации) для source control.</span><span class="sxs-lookup"><span data-stu-id="6a247-127">The publishRunbook property of the source control.</span></span>
<span data-ttu-id="6a247-128">Если настроена книга DoNotPublishRunbook, это означает, что пользовательские книги будут импортироваться как черновики.</span><span class="sxs-lookup"><span data-stu-id="6a247-128">If DoNotPublishRunbook is set, this means that user runbooks will be imported as 'Draft'.</span></span>

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

### <span data-ttu-id="6a247-129">-EnableAutoSync</span><span class="sxs-lookup"><span data-stu-id="6a247-129">-EnableAutoSync</span></span>
<span data-ttu-id="6a247-130">Свойство autoSync для источника.</span><span class="sxs-lookup"><span data-stu-id="6a247-130">The autoSync property for the source control.</span></span>

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

### <span data-ttu-id="6a247-131">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="6a247-131">-FolderPath</span></span>
<span data-ttu-id="6a247-132">Путь к папке для управления источником.</span><span class="sxs-lookup"><span data-stu-id="6a247-132">The source control folder path.</span></span>

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

### <span data-ttu-id="6a247-133">-Name</span><span class="sxs-lookup"><span data-stu-id="6a247-133">-Name</span></span>
<span data-ttu-id="6a247-134">Имя источника.</span><span class="sxs-lookup"><span data-stu-id="6a247-134">The source control name.</span></span>

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

### <span data-ttu-id="6a247-135">-RepoUrl</span><span class="sxs-lookup"><span data-stu-id="6a247-135">-RepoUrl</span></span>
<span data-ttu-id="6a247-136">URL-адрес повторного url-адреса для управления источником.</span><span class="sxs-lookup"><span data-stu-id="6a247-136">The source control repo url.</span></span>

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

### <span data-ttu-id="6a247-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a247-137">-ResourceGroupName</span></span>
<span data-ttu-id="6a247-138">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6a247-138">The resource group name.</span></span>

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

### <span data-ttu-id="6a247-139">-SourceType</span><span class="sxs-lookup"><span data-stu-id="6a247-139">-SourceType</span></span>
<span data-ttu-id="6a247-140">Тип управления "Источник".</span><span class="sxs-lookup"><span data-stu-id="6a247-140">The source control type.</span></span>

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

### <span data-ttu-id="6a247-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a247-141">-Confirm</span></span>
<span data-ttu-id="6a247-142">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a247-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a247-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a247-143">-WhatIf</span></span>
<span data-ttu-id="6a247-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a247-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a247-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6a247-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a247-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a247-146">CommonParameters</span></span>
<span data-ttu-id="6a247-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a247-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a247-148">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a247-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a247-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6a247-149">INPUTS</span></span>

### <span data-ttu-id="6a247-150">System.String</span><span class="sxs-lookup"><span data-stu-id="6a247-150">System.String</span></span>

## <span data-ttu-id="6a247-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6a247-151">OUTPUTS</span></span>

### <span data-ttu-id="6a247-152">Microsoft.Azure.Commands.Automation.Model.SourceControl</span><span class="sxs-lookup"><span data-stu-id="6a247-152">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="6a247-153">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6a247-153">NOTES</span></span>

## <span data-ttu-id="6a247-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6a247-154">RELATED LINKS</span></span>
