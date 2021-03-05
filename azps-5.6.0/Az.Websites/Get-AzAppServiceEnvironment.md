---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azappserviceenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServiceEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServiceEnvironment.md
ms.openlocfilehash: 9641c55dd25d8f09d1898bdda37fafa840db0a19
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983896"
---
# <span data-ttu-id="6fa33-101">Get-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="6fa33-101">Get-AzAppServiceEnvironment</span></span>

## <span data-ttu-id="6fa33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fa33-102">SYNOPSIS</span></span>
<span data-ttu-id="6fa33-103">Получает среду службы приложений.</span><span class="sxs-lookup"><span data-stu-id="6fa33-103">Gets App Service Environment.</span></span> <span data-ttu-id="6fa33-104">Если указана только группа ресурсов, она возвращает список ASE в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6fa33-104">If only Resource Group is specified, it will return a list of ASE in the Resource Group.</span></span>

## <span data-ttu-id="6fa33-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6fa33-105">SYNTAX</span></span>

```
Get-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fa33-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6fa33-106">DESCRIPTION</span></span>
<span data-ttu-id="6fa33-107">Командлет **Get-AzAppServiceEnvironment** возвращает asE, совпадающие с запросом.</span><span class="sxs-lookup"><span data-stu-id="6fa33-107">The **Get-AzAppServiceEnvironment** cmdlet return ASE(s) matching the query.</span></span>

## <span data-ttu-id="6fa33-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6fa33-108">EXAMPLES</span></span>

### <span data-ttu-id="6fa33-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6fa33-109">Example 1</span></span>
```powershell
PS C:\> Get-AzAppServiceEnvironment -ResourceGroupName MyResourceGroup -Name MyAseName
```

<span data-ttu-id="6fa33-110">Возвращает определенную среду служб приложений, которая называется <MyAseName> в <MyResourceGroup></span><span class="sxs-lookup"><span data-stu-id="6fa33-110">Returns a specific App Service Environment named <MyAseName> in <MyResourceGroup></span></span>

## <span data-ttu-id="6fa33-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6fa33-111">PARAMETERS</span></span>

### <span data-ttu-id="6fa33-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fa33-112">-DefaultProfile</span></span>
<span data-ttu-id="6fa33-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6fa33-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fa33-114">-Name</span><span class="sxs-lookup"><span data-stu-id="6fa33-114">-Name</span></span>
<span data-ttu-id="6fa33-115">Имя среды службы приложений.</span><span class="sxs-lookup"><span data-stu-id="6fa33-115">The name of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fa33-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fa33-116">-ResourceGroupName</span></span>
<span data-ttu-id="6fa33-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6fa33-117">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fa33-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6fa33-118">-Confirm</span></span>
<span data-ttu-id="6fa33-119">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6fa33-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fa33-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fa33-120">-WhatIf</span></span>
<span data-ttu-id="6fa33-121">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6fa33-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fa33-122">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6fa33-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fa33-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fa33-123">CommonParameters</span></span>
<span data-ttu-id="6fa33-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fa33-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fa33-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6fa33-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fa33-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6fa33-126">INPUTS</span></span>

### <span data-ttu-id="6fa33-127">Нет</span><span class="sxs-lookup"><span data-stu-id="6fa33-127">None</span></span>

## <span data-ttu-id="6fa33-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6fa33-128">OUTPUTS</span></span>

### <span data-ttu-id="6fa33-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="6fa33-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServiceEnvironment</span></span>

## <span data-ttu-id="6fa33-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6fa33-130">NOTES</span></span>

## <span data-ttu-id="6fa33-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6fa33-131">RELATED LINKS</span></span>

[<span data-ttu-id="6fa33-132">New-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="6fa33-132">New-AzAppServiceEnvironment</span></span>](./New-AzAppServiceEnvironment.md)

[<span data-ttu-id="6fa33-133">New-AzAppServiceEnvironmentInboundServices</span><span class="sxs-lookup"><span data-stu-id="6fa33-133">New-AzAppServiceEnvironmentInboundServices</span></span>](./New-AzAppServiceEnvironmentInboundServices.md)

[<span data-ttu-id="6fa33-134">Remove-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="6fa33-134">Remove-AzAppServiceEnvironment</span></span>](./Remove-AzAppServiceEnvironment.md)