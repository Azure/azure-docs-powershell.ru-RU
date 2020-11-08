---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServicePlan.md
ms.openlocfilehash: dfd2cfd20ab11e2e70e03dc3e166c83729ef344a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236477"
---
# <span data-ttu-id="990ee-101">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="990ee-101">Remove-AzAppServicePlan</span></span>

## <span data-ttu-id="990ee-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="990ee-102">SYNOPSIS</span></span>
<span data-ttu-id="990ee-103">Удаляет план служб приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="990ee-103">Removes an Azure App Service plan.</span></span>

## <span data-ttu-id="990ee-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="990ee-104">SYNTAX</span></span>

### <span data-ttu-id="990ee-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="990ee-105">S1</span></span>
```
Remove-AzAppServicePlan [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="990ee-106">S2</span><span class="sxs-lookup"><span data-stu-id="990ee-106">S2</span></span>
```
Remove-AzAppServicePlan [-Force] [-AsJob] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="990ee-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="990ee-107">DESCRIPTION</span></span>
<span data-ttu-id="990ee-108">Командлет **Remove-AzAppServicePlan** удаляет план служб приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="990ee-108">The **Remove-AzAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="990ee-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="990ee-109">EXAMPLES</span></span>

### <span data-ttu-id="990ee-110">Пример 1: Удаление плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="990ee-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="990ee-111">Эта команда удаляет план служб приложений для Azure с именем ContosoASP, который входит в группу ресурсов с именем Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="990ee-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="990ee-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="990ee-112">PARAMETERS</span></span>

### <span data-ttu-id="990ee-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="990ee-113">-AppServicePlan</span></span>
<span data-ttu-id="990ee-114">Объект плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="990ee-114">App Service Plan Object</span></span>

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

### <span data-ttu-id="990ee-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="990ee-115">-AsJob</span></span>
<span data-ttu-id="990ee-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="990ee-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="990ee-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="990ee-117">-DefaultProfile</span></span>
<span data-ttu-id="990ee-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="990ee-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="990ee-119">-Force</span><span class="sxs-lookup"><span data-stu-id="990ee-119">-Force</span></span>
<span data-ttu-id="990ee-120">Параметр принудительного удаления</span><span class="sxs-lookup"><span data-stu-id="990ee-120">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="990ee-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="990ee-121">-Name</span></span>
<span data-ttu-id="990ee-122">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="990ee-122">App Service Plan Name</span></span>

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

### <span data-ttu-id="990ee-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="990ee-123">-ResourceGroupName</span></span>
<span data-ttu-id="990ee-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="990ee-124">Resource Group Name</span></span>

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

### <span data-ttu-id="990ee-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="990ee-125">-Confirm</span></span>
<span data-ttu-id="990ee-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="990ee-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="990ee-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="990ee-127">-WhatIf</span></span>
<span data-ttu-id="990ee-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="990ee-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="990ee-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="990ee-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="990ee-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="990ee-130">CommonParameters</span></span>
<span data-ttu-id="990ee-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="990ee-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="990ee-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="990ee-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="990ee-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="990ee-133">INPUTS</span></span>

### <span data-ttu-id="990ee-134">Microsoft. Azure. Commands. Apps. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="990ee-134">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="990ee-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="990ee-135">OUTPUTS</span></span>

### <span data-ttu-id="990ee-136">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="990ee-136">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="990ee-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="990ee-137">NOTES</span></span>

## <span data-ttu-id="990ee-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="990ee-138">RELATED LINKS</span></span>

[<span data-ttu-id="990ee-139">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="990ee-139">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="990ee-140">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="990ee-140">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="990ee-141">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="990ee-141">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)

