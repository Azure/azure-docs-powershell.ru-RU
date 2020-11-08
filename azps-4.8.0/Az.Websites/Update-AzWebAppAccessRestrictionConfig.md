---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: b2d2a2eb24fce89c65561c9d86f18072d4ac4e0a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077437"
---
# <span data-ttu-id="5a463-101">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="5a463-101">Update-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="5a463-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5a463-102">SYNOPSIS</span></span>
<span data-ttu-id="5a463-103">Обновляет наследование основного сайта restiction config на сайт SCM для веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="5a463-103">Updates the inheritance of Main site Access Restiction config to SCM Site for an Azure Web App.</span></span>

## <span data-ttu-id="5a463-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5a463-104">SYNTAX</span></span>

### <span data-ttu-id="5a463-105">InputValuesParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5a463-105">InputValuesParameterSet (Default)</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String>
 [-ScmSiteUseMainSiteRestrictionConfig] [-SlotName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a463-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a463-106">InputObjectParameterSet</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-PassThru] -InputObject <PSAccessRestrictionConfig>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a463-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a463-107">DESCRIPTION</span></span>
<span data-ttu-id="5a463-108">Командлет **Update-AzWebAppAccessRestrictionConfig** обновляет конфигурацию ограничения доступа для веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="5a463-108">The **Update-AzWebAppAccessRestrictionConfig** cmdlet updates Access Restriction config for an Azure Web App.</span></span>

## <span data-ttu-id="5a463-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5a463-109">EXAMPLES</span></span>

### <span data-ttu-id="5a463-110">Пример 1: обновление сайта веб-приложения SCM на использование ограничений доступа с главного сайта</span><span class="sxs-lookup"><span data-stu-id="5a463-110">Example 1: Update a Web App SCM Site to use Access Restrictions from Main Site</span></span>

<span data-ttu-id="5a463-111">В следующем примере показано, как обновить веб-приложение IpRule, которое принадлежит группе ресурсов MyResourceGroup, чтобы использовать конфигурацию ограничения доступа для основного сайта на сайте SCM.</span><span class="sxs-lookup"><span data-stu-id="5a463-111">The following example updates a Web App named IpRule that belongs to the resource group MyResourceGroup to use access restriction config of main site on the scm site.</span></span>

```powershell <!-- Aladdin Generated Example --> 
Update-AzWebAppAccessRestrictionConfig -Name IpRule -ResourceGroupName MyResourceGroup -ScmSiteUseMainSiteRestrictionConfig
```

## <span data-ttu-id="5a463-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5a463-112">PARAMETERS</span></span>

### <span data-ttu-id="5a463-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a463-113">-DefaultProfile</span></span>
<span data-ttu-id="5a463-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5a463-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a463-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a463-115">-InputObject</span></span>
<span data-ttu-id="5a463-116">Объект конфигурации ограничения доступа</span><span class="sxs-lookup"><span data-stu-id="5a463-116">The access restriction config object</span></span>

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

### <span data-ttu-id="5a463-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5a463-117">-Name</span></span>
<span data-ttu-id="5a463-118">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="5a463-118">WebApp Name</span></span>

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

### <span data-ttu-id="5a463-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a463-119">-PassThru</span></span>
<span data-ttu-id="5a463-120">Возврат объекта конфигурации ограничения доступа.</span><span class="sxs-lookup"><span data-stu-id="5a463-120">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="5a463-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a463-121">-ResourceGroupName</span></span>
<span data-ttu-id="5a463-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="5a463-122">Resource Group Name</span></span>

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

### <span data-ttu-id="5a463-123">-ScmSiteUseMainSiteRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="5a463-123">-ScmSiteUseMainSiteRestrictionConfig</span></span>
<span data-ttu-id="5a463-124">Сайт SCM наследует правила, заданные на главном сайте.</span><span class="sxs-lookup"><span data-stu-id="5a463-124">Scm site inherits rules set on Main site.</span></span>

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

### <span data-ttu-id="5a463-125">-SlotName</span><span class="sxs-lookup"><span data-stu-id="5a463-125">-SlotName</span></span>
<span data-ttu-id="5a463-126">Имя слота развертывания.</span><span class="sxs-lookup"><span data-stu-id="5a463-126">Deployment Slot name.</span></span>

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

### <span data-ttu-id="5a463-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a463-127">-Confirm</span></span>
<span data-ttu-id="5a463-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5a463-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a463-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a463-129">-WhatIf</span></span>
<span data-ttu-id="5a463-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5a463-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5a463-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5a463-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a463-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a463-132">CommonParameters</span></span>
<span data-ttu-id="5a463-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5a463-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a463-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a463-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a463-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5a463-135">INPUTS</span></span>

### <span data-ttu-id="5a463-136">System. String</span><span class="sxs-lookup"><span data-stu-id="5a463-136">System.String</span></span>

### <span data-ttu-id="5a463-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5a463-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5a463-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a463-138">OUTPUTS</span></span>

### <span data-ttu-id="5a463-139">Microsoft. Azure. Commands. Apps. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="5a463-139">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="5a463-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="5a463-140">NOTES</span></span>

## <span data-ttu-id="5a463-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5a463-141">RELATED LINKS</span></span>

[<span data-ttu-id="5a463-142">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="5a463-142">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="5a463-143">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="5a463-143">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="5a463-144">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="5a463-144">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)