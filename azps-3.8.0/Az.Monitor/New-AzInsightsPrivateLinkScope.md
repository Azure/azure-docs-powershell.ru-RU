---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 198d52678bceccfd1045522881dc3a62fdebf752
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912349"
---
# <span data-ttu-id="48d77-101">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="48d77-101">New-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="48d77-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="48d77-102">SYNOPSIS</span></span>
<span data-ttu-id="48d77-103">Создание области личных ссылок</span><span class="sxs-lookup"><span data-stu-id="48d77-103">create private link scope</span></span>

## <span data-ttu-id="48d77-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="48d77-104">SYNTAX</span></span>

```
New-AzInsightsPrivateLinkScope -Location <String> -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48d77-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="48d77-105">DESCRIPTION</span></span>
<span data-ttu-id="48d77-106">Создание области личных ссылок</span><span class="sxs-lookup"><span data-stu-id="48d77-106">create private link scope</span></span>

## <span data-ttu-id="48d77-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="48d77-107">EXAMPLES</span></span>

### <span data-ttu-id="48d77-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="48d77-108">Example 1</span></span>
```powershell
New-AzInsightsPrivateLinkScope -Location "eastus" -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="48d77-109">Создание области личных ссылок с именем "scope_name" в разделе "Группа ресурсов" rg_name "в расположении" eastus "</span><span class="sxs-lookup"><span data-stu-id="48d77-109">create private link scope with name "scope_name" under resource group "rg_name" in location "eastus"</span></span>

## <span data-ttu-id="48d77-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="48d77-110">PARAMETERS</span></span>

### <span data-ttu-id="48d77-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48d77-111">-DefaultProfile</span></span>
<span data-ttu-id="48d77-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="48d77-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48d77-113">-Location</span><span class="sxs-lookup"><span data-stu-id="48d77-113">-Location</span></span>
<span data-ttu-id="48d77-114">Поиска</span><span class="sxs-lookup"><span data-stu-id="48d77-114">Location</span></span>

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

### <span data-ttu-id="48d77-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="48d77-115">-Name</span></span>
<span data-ttu-id="48d77-116">Имя области личных ссылок</span><span class="sxs-lookup"><span data-stu-id="48d77-116">Private Link Scope Name</span></span>

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

### <span data-ttu-id="48d77-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48d77-117">-ResourceGroupName</span></span>
<span data-ttu-id="48d77-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="48d77-118">Resource Group Name</span></span>

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

### <span data-ttu-id="48d77-119">-Теги</span><span class="sxs-lookup"><span data-stu-id="48d77-119">-Tags</span></span>
<span data-ttu-id="48d77-120">Embed</span><span class="sxs-lookup"><span data-stu-id="48d77-120">Tags</span></span>

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

### <span data-ttu-id="48d77-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="48d77-121">-Confirm</span></span>
<span data-ttu-id="48d77-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="48d77-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48d77-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48d77-123">-WhatIf</span></span>
<span data-ttu-id="48d77-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="48d77-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48d77-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="48d77-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48d77-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48d77-126">CommonParameters</span></span>
<span data-ttu-id="48d77-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="48d77-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48d77-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48d77-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48d77-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="48d77-129">INPUTS</span></span>

### <span data-ttu-id="48d77-130">System. String</span><span class="sxs-lookup"><span data-stu-id="48d77-130">System.String</span></span>

## <span data-ttu-id="48d77-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="48d77-131">OUTPUTS</span></span>

### <span data-ttu-id="48d77-132">Microsoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="48d77-132">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="48d77-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="48d77-133">NOTES</span></span>

## <span data-ttu-id="48d77-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="48d77-134">RELATED LINKS</span></span>
