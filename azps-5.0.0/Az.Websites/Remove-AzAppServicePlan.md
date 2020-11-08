---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServicePlan.md
ms.openlocfilehash: dfd2cfd20ab11e2e70e03dc3e166c83729ef344a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249261"
---
# <span data-ttu-id="501c1-101">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="501c1-101">Remove-AzAppServicePlan</span></span>

## <span data-ttu-id="501c1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="501c1-102">SYNOPSIS</span></span>
<span data-ttu-id="501c1-103">Удаляет план служб приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="501c1-103">Removes an Azure App Service plan.</span></span>

## <span data-ttu-id="501c1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="501c1-104">SYNTAX</span></span>

### <span data-ttu-id="501c1-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="501c1-105">S1</span></span>
```
Remove-AzAppServicePlan [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="501c1-106">S2</span><span class="sxs-lookup"><span data-stu-id="501c1-106">S2</span></span>
```
Remove-AzAppServicePlan [-Force] [-AsJob] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="501c1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="501c1-107">DESCRIPTION</span></span>
<span data-ttu-id="501c1-108">Командлет **Remove-AzAppServicePlan** удаляет план служб приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="501c1-108">The **Remove-AzAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="501c1-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="501c1-109">EXAMPLES</span></span>

### <span data-ttu-id="501c1-110">Пример 1: Удаление плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="501c1-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="501c1-111">Эта команда удаляет план служб приложений для Azure с именем ContosoASP, который входит в группу ресурсов с именем Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="501c1-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="501c1-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="501c1-112">PARAMETERS</span></span>

### <span data-ttu-id="501c1-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="501c1-113">-AppServicePlan</span></span>
<span data-ttu-id="501c1-114">Объект плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="501c1-114">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="501c1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="501c1-115">-AsJob</span></span>
<span data-ttu-id="501c1-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="501c1-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="501c1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="501c1-117">-DefaultProfile</span></span>
<span data-ttu-id="501c1-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="501c1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="501c1-119">-Force</span><span class="sxs-lookup"><span data-stu-id="501c1-119">-Force</span></span>
<span data-ttu-id="501c1-120">Параметр принудительного удаления</span><span class="sxs-lookup"><span data-stu-id="501c1-120">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="501c1-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="501c1-121">-Name</span></span>
<span data-ttu-id="501c1-122">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="501c1-122">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="501c1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="501c1-123">-ResourceGroupName</span></span>
<span data-ttu-id="501c1-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="501c1-124">Resource Group Name</span></span>

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

### <span data-ttu-id="501c1-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="501c1-125">-Confirm</span></span>
<span data-ttu-id="501c1-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="501c1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="501c1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="501c1-127">-WhatIf</span></span>
<span data-ttu-id="501c1-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="501c1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="501c1-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="501c1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="501c1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="501c1-130">CommonParameters</span></span>
<span data-ttu-id="501c1-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="501c1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="501c1-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="501c1-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="501c1-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="501c1-133">INPUTS</span></span>

### <span data-ttu-id="501c1-134">Microsoft. Azure. Commands. Apps. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="501c1-134">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="501c1-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="501c1-135">OUTPUTS</span></span>

### <span data-ttu-id="501c1-136">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="501c1-136">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="501c1-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="501c1-137">NOTES</span></span>

## <span data-ttu-id="501c1-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="501c1-138">RELATED LINKS</span></span>

[<span data-ttu-id="501c1-139">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="501c1-139">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="501c1-140">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="501c1-140">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="501c1-141">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="501c1-141">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


