---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 198d52678bceccfd1045522881dc3a62fdebf752
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214196"
---
# <span data-ttu-id="a2cad-101">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="a2cad-101">New-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="a2cad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2cad-102">SYNOPSIS</span></span>
<span data-ttu-id="a2cad-103">Создание области частных ссылок</span><span class="sxs-lookup"><span data-stu-id="a2cad-103">create private link scope</span></span>

## <span data-ttu-id="a2cad-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a2cad-104">SYNTAX</span></span>

```
New-AzInsightsPrivateLinkScope -Location <String> -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2cad-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2cad-105">DESCRIPTION</span></span>
<span data-ttu-id="a2cad-106">Создание области частных ссылок</span><span class="sxs-lookup"><span data-stu-id="a2cad-106">create private link scope</span></span>

## <span data-ttu-id="a2cad-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a2cad-107">EXAMPLES</span></span>

### <span data-ttu-id="a2cad-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a2cad-108">Example 1</span></span>
```powershell
New-AzInsightsPrivateLinkScope -Location "eastus" -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="a2cad-109">Создать частную область ссылок с именем "scope_name" в группе ресурсов "rg_name" в расположении "eastus"</span><span class="sxs-lookup"><span data-stu-id="a2cad-109">create private link scope with name "scope_name" under resource group "rg_name" in location "eastus"</span></span>

## <span data-ttu-id="a2cad-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2cad-110">PARAMETERS</span></span>

### <span data-ttu-id="a2cad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2cad-111">-DefaultProfile</span></span>
<span data-ttu-id="a2cad-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a2cad-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2cad-113">-Location</span><span class="sxs-lookup"><span data-stu-id="a2cad-113">-Location</span></span>
<span data-ttu-id="a2cad-114">Расположение</span><span class="sxs-lookup"><span data-stu-id="a2cad-114">Location</span></span>

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

### <span data-ttu-id="a2cad-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a2cad-115">-Name</span></span>
<span data-ttu-id="a2cad-116">Имя области приватных ссылок</span><span class="sxs-lookup"><span data-stu-id="a2cad-116">Private Link Scope Name</span></span>

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

### <span data-ttu-id="a2cad-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2cad-117">-ResourceGroupName</span></span>
<span data-ttu-id="a2cad-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a2cad-118">Resource Group Name</span></span>

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

### <span data-ttu-id="a2cad-119">-Теги</span><span class="sxs-lookup"><span data-stu-id="a2cad-119">-Tags</span></span>
<span data-ttu-id="a2cad-120">Теги</span><span class="sxs-lookup"><span data-stu-id="a2cad-120">Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2cad-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2cad-121">-Confirm</span></span>
<span data-ttu-id="a2cad-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a2cad-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2cad-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2cad-123">-WhatIf</span></span>
<span data-ttu-id="a2cad-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2cad-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2cad-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a2cad-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2cad-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2cad-126">CommonParameters</span></span>
<span data-ttu-id="a2cad-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2cad-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2cad-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2cad-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2cad-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a2cad-129">INPUTS</span></span>

### <span data-ttu-id="a2cad-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a2cad-130">System.String</span></span>

## <span data-ttu-id="a2cad-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a2cad-131">OUTPUTS</span></span>

### <span data-ttu-id="a2cad-132">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="a2cad-132">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="a2cad-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a2cad-133">NOTES</span></span>

## <span data-ttu-id="a2cad-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a2cad-134">RELATED LINKS</span></span>
