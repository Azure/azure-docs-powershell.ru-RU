---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppContainerPSSession.md
ms.openlocfilehash: 2244eb06257d69005d64cc640d0ecd783bd30572
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505763"
---
# <span data-ttu-id="ed8f7-101">New-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="ed8f7-101">New-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="ed8f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed8f7-102">SYNOPSIS</span></span>
<span data-ttu-id="ed8f7-103">New-AzWebAppContainerPSSession создает новый удаленный сеанс PowerShell в контейнере Windows, указанном на определенном сайте или в слоте и заданной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="ed8f7-103">New-AzWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="ed8f7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ed8f7-104">SYNTAX</span></span>

### <span data-ttu-id="ed8f7-105">S1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ed8f7-105">S1 (Default)</span></span>
```
New-AzWebAppContainerPSSession [[-SlotName] <String>] [-Force] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed8f7-106">S2</span><span class="sxs-lookup"><span data-stu-id="ed8f7-106">S2</span></span>
```
New-AzWebAppContainerPSSession [-Force] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed8f7-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed8f7-107">DESCRIPTION</span></span>
<span data-ttu-id="ed8f7-108">New-AzWebAppContainerPSSession создает удаленный сеанс PowerShell в контейнере Windows, указанном на сайте или в слоте и группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="ed8f7-108">New-AzWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="ed8f7-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ed8f7-109">EXAMPLES</span></span>

### <span data-ttu-id="ed8f7-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ed8f7-110">Example 1</span></span>
```
PS C:\> $s = New-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
PS C:\> Invoke-Command -Session $s -ScriptBlock{Get-Process}
```

<span data-ttu-id="ed8f7-111">Будет создаваться новый удаленный сеанс PowerShell в приложении контейнера Windows ContosoASP и процессы, запущенные в контейнере ContosoASP.</span><span class="sxs-lookup"><span data-stu-id="ed8f7-111">This will create a new remote PowerShell Session into the windows container app ContosoASP and show the processes that are running on the container ContosoASP</span></span>

## <span data-ttu-id="ed8f7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed8f7-112">PARAMETERS</span></span>

### <span data-ttu-id="ed8f7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed8f7-113">-DefaultProfile</span></span>
<span data-ttu-id="ed8f7-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ed8f7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed8f7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ed8f7-115">-Force</span></span>
<span data-ttu-id="ed8f7-116">Создайте сеанс PowerShell без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="ed8f7-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ed8f7-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ed8f7-117">-Name</span></span>
<span data-ttu-id="ed8f7-118">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="ed8f7-118">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed8f7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed8f7-119">-ResourceGroupName</span></span>
<span data-ttu-id="ed8f7-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ed8f7-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed8f7-121">-SlotName</span><span class="sxs-lookup"><span data-stu-id="ed8f7-121">-SlotName</span></span>
<span data-ttu-id="ed8f7-122">Название слота веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="ed8f7-122">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed8f7-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ed8f7-123">-WebApp</span></span>
<span data-ttu-id="ed8f7-124">Объект веб-приложения</span><span class="sxs-lookup"><span data-stu-id="ed8f7-124">The web app object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed8f7-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed8f7-125">-Confirm</span></span>
<span data-ttu-id="ed8f7-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed8f7-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed8f7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed8f7-127">-WhatIf</span></span>
<span data-ttu-id="ed8f7-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed8f7-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ed8f7-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ed8f7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed8f7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed8f7-130">CommonParameters</span></span>
<span data-ttu-id="ed8f7-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed8f7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed8f7-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed8f7-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed8f7-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ed8f7-133">INPUTS</span></span>

### <span data-ttu-id="ed8f7-134">System.String</span><span class="sxs-lookup"><span data-stu-id="ed8f7-134">System.String</span></span>

### <span data-ttu-id="ed8f7-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="ed8f7-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ed8f7-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ed8f7-136">OUTPUTS</span></span>

### <span data-ttu-id="ed8f7-137">System.Management.Automation.Runspaces.PSSession</span><span class="sxs-lookup"><span data-stu-id="ed8f7-137">System.Management.Automation.Runspaces.PSSession</span></span>

## <span data-ttu-id="ed8f7-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ed8f7-138">NOTES</span></span>

## <span data-ttu-id="ed8f7-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ed8f7-139">RELATED LINKS</span></span>
