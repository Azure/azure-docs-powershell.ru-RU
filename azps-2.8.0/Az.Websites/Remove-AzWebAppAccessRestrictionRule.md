---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: 0631492bf2574fed7a9bb755088d811483504763
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907782"
---
# <span data-ttu-id="37b26-101">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="37b26-101">Remove-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="37b26-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="37b26-102">SYNOPSIS</span></span>
<span data-ttu-id="37b26-103">Удаляет правило ограничения доступа из веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="37b26-103">Removes an Access Restriction rule from an Azure Web App.</span></span>

## <span data-ttu-id="37b26-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="37b26-104">SYNTAX</span></span>

```
Remove-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> -Name <String>
 [-TargetScmSite] [-SlotName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37b26-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="37b26-105">DESCRIPTION</span></span>
<span data-ttu-id="37b26-106">Командлет **Remove-AzWebAppAccessRestrictionRule** удаляет правило ограничения доступа из веб-приложения Azure</span><span class="sxs-lookup"><span data-stu-id="37b26-106">The **Remove-AzWebAppAccessRestrictionRule** cmdlet removes an Access Restriction rule from an Azure Web App</span></span>

## <span data-ttu-id="37b26-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="37b26-107">EXAMPLES</span></span>

### <span data-ttu-id="37b26-108">Пример 1: Удаление правила ограничения доступа для веб-приложения</span><span class="sxs-lookup"><span data-stu-id="37b26-108">Example 1: Remove a Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -Name IpRule
```

<span data-ttu-id="37b26-109">Эта команда удаляет правило ограничения доступа IpRule из Azure Web App с именем ContosoSite, которое принадлежит группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="37b26-109">This command removes the IpRule access restriction rule from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="37b26-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="37b26-110">PARAMETERS</span></span>

### <span data-ttu-id="37b26-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37b26-111">-DefaultProfile</span></span>
<span data-ttu-id="37b26-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="37b26-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37b26-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="37b26-113">-Name</span></span>
<span data-ttu-id="37b26-114">Имя правила ограничения доступа</span><span class="sxs-lookup"><span data-stu-id="37b26-114">Access Restriction Rule Name</span></span>

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

### <span data-ttu-id="37b26-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37b26-115">-PassThru</span></span>
<span data-ttu-id="37b26-116">Возврат объекта конфигурации ограничения доступа.</span><span class="sxs-lookup"><span data-stu-id="37b26-116">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="37b26-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37b26-117">-ResourceGroupName</span></span>
<span data-ttu-id="37b26-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="37b26-118">Resource Group Name</span></span>

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

### <span data-ttu-id="37b26-119">-SlotName</span><span class="sxs-lookup"><span data-stu-id="37b26-119">-SlotName</span></span>
<span data-ttu-id="37b26-120">Имя слота развертывания.</span><span class="sxs-lookup"><span data-stu-id="37b26-120">Deployment Slot Name.</span></span>

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

### <span data-ttu-id="37b26-121">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="37b26-121">-TargetScmSite</span></span>
<span data-ttu-id="37b26-122">Правило предназначено для основного сайта или сайта SCM.</span><span class="sxs-lookup"><span data-stu-id="37b26-122">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="37b26-123">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="37b26-123">-WebAppName</span></span>
<span data-ttu-id="37b26-124">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="37b26-124">The name of the web app.</span></span>

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

### <span data-ttu-id="37b26-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37b26-125">-Confirm</span></span>
<span data-ttu-id="37b26-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="37b26-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37b26-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37b26-127">-WhatIf</span></span>
<span data-ttu-id="37b26-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="37b26-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="37b26-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="37b26-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37b26-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37b26-130">CommonParameters</span></span>
<span data-ttu-id="37b26-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="37b26-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37b26-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37b26-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37b26-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="37b26-133">INPUTS</span></span>

### <span data-ttu-id="37b26-134">System. String</span><span class="sxs-lookup"><span data-stu-id="37b26-134">System.String</span></span>

## <span data-ttu-id="37b26-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="37b26-135">OUTPUTS</span></span>

### <span data-ttu-id="37b26-136">Microsoft. Azure. Commands. Apps. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="37b26-136">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="37b26-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="37b26-137">NOTES</span></span>

## <span data-ttu-id="37b26-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="37b26-138">RELATED LINKS</span></span>

[<span data-ttu-id="37b26-139">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="37b26-139">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="37b26-140">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="37b26-140">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="37b26-141">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="37b26-141">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)
