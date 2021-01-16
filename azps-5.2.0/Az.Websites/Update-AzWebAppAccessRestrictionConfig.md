---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: b2d2a2eb24fce89c65561c9d86f18072d4ac4e0a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404007"
---
# <span data-ttu-id="96559-101">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="96559-101">Update-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="96559-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96559-102">SYNOPSIS</span></span>
<span data-ttu-id="96559-103">Обновляет наследование веб-сайта Restiction Access restiction для сайта SCM для Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="96559-103">Updates the inheritance of Main site Access Restiction config to SCM Site for an Azure Web App.</span></span>

## <span data-ttu-id="96559-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="96559-104">SYNTAX</span></span>

### <span data-ttu-id="96559-105">InputValuesParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="96559-105">InputValuesParameterSet (Default)</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String>
 [-ScmSiteUseMainSiteRestrictionConfig] [-SlotName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96559-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="96559-106">InputObjectParameterSet</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-PassThru] -InputObject <PSAccessRestrictionConfig>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96559-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="96559-107">DESCRIPTION</span></span>
<span data-ttu-id="96559-108">С **помощью cmdlet update-AzWebAppAccessRestrictionConfig** обновляется значение ограничения доступа для Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="96559-108">The **Update-AzWebAppAccessRestrictionConfig** cmdlet updates Access Restriction config for an Azure Web App.</span></span>

## <span data-ttu-id="96559-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="96559-109">EXAMPLES</span></span>

### <span data-ttu-id="96559-110">Пример 1. Обновление SCM-сайта веб-приложения для использования ограничений доступа с основного сайта</span><span class="sxs-lookup"><span data-stu-id="96559-110">Example 1: Update a Web App SCM Site to use Access Restrictions from Main Site</span></span>

<span data-ttu-id="96559-111">В следующем примере веб-приложение с именем IpRule, которое принадлежит к группе ресурсов MyResourceGroup, обновляется для использования ограничений доступа основного сайта на scm-сайте.</span><span class="sxs-lookup"><span data-stu-id="96559-111">The following example updates a Web App named IpRule that belongs to the resource group MyResourceGroup to use access restriction config of main site on the scm site.</span></span>

```powershell <!-- Aladdin Generated Example --> 
Update-AzWebAppAccessRestrictionConfig -Name IpRule -ResourceGroupName MyResourceGroup -ScmSiteUseMainSiteRestrictionConfig
```

## <span data-ttu-id="96559-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96559-112">PARAMETERS</span></span>

### <span data-ttu-id="96559-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96559-113">-DefaultProfile</span></span>
<span data-ttu-id="96559-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="96559-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96559-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96559-115">-InputObject</span></span>
<span data-ttu-id="96559-116">Объект config с ограничением доступа</span><span class="sxs-lookup"><span data-stu-id="96559-116">The access restriction config object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96559-117">-Name</span><span class="sxs-lookup"><span data-stu-id="96559-117">-Name</span></span>
<span data-ttu-id="96559-118">Имя веб-приложения</span><span class="sxs-lookup"><span data-stu-id="96559-118">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96559-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="96559-119">-PassThru</span></span>
<span data-ttu-id="96559-120">Возвращает объект config с ограничениями доступа.</span><span class="sxs-lookup"><span data-stu-id="96559-120">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="96559-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96559-121">-ResourceGroupName</span></span>
<span data-ttu-id="96559-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="96559-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96559-123">-ScmSiteUseMainSiteRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="96559-123">-ScmSiteUseMainSiteRestrictionConfig</span></span>
<span data-ttu-id="96559-124">SCM-сайт наследует правила, установленные на основном сайте.</span><span class="sxs-lookup"><span data-stu-id="96559-124">Scm site inherits rules set on Main site.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96559-125">-SlotName</span><span class="sxs-lookup"><span data-stu-id="96559-125">-SlotName</span></span>
<span data-ttu-id="96559-126">Название слота развертывания.</span><span class="sxs-lookup"><span data-stu-id="96559-126">Deployment Slot name.</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96559-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="96559-127">-Confirm</span></span>
<span data-ttu-id="96559-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="96559-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96559-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96559-129">-WhatIf</span></span>
<span data-ttu-id="96559-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96559-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96559-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="96559-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96559-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96559-132">CommonParameters</span></span>
<span data-ttu-id="96559-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96559-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96559-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="96559-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96559-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="96559-135">INPUTS</span></span>

### <span data-ttu-id="96559-136">System.String</span><span class="sxs-lookup"><span data-stu-id="96559-136">System.String</span></span>

### <span data-ttu-id="96559-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="96559-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="96559-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="96559-138">OUTPUTS</span></span>

### <span data-ttu-id="96559-139">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="96559-139">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="96559-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="96559-140">NOTES</span></span>

## <span data-ttu-id="96559-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="96559-141">RELATED LINKS</span></span>

[<span data-ttu-id="96559-142">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="96559-142">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="96559-143">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="96559-143">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="96559-144">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="96559-144">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
