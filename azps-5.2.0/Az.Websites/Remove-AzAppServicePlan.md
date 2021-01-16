---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServicePlan.md
ms.openlocfilehash: dfd2cfd20ab11e2e70e03dc3e166c83729ef344a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414812"
---
# <span data-ttu-id="3ec9d-101">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3ec9d-101">Remove-AzAppServicePlan</span></span>

## <span data-ttu-id="3ec9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ec9d-102">SYNOPSIS</span></span>
<span data-ttu-id="3ec9d-103">Удаляет план службы приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="3ec9d-103">Removes an Azure App Service plan.</span></span>

## <span data-ttu-id="3ec9d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3ec9d-104">SYNTAX</span></span>

### <span data-ttu-id="3ec9d-105">S1</span><span class="sxs-lookup"><span data-stu-id="3ec9d-105">S1</span></span>
```
Remove-AzAppServicePlan [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ec9d-106">S2</span><span class="sxs-lookup"><span data-stu-id="3ec9d-106">S2</span></span>
```
Remove-AzAppServicePlan [-Force] [-AsJob] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ec9d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ec9d-107">DESCRIPTION</span></span>
<span data-ttu-id="3ec9d-108">С **помощью cmdlet Remove-AzAppServicePlan** удаляется план службы приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="3ec9d-108">The **Remove-AzAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="3ec9d-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3ec9d-109">EXAMPLES</span></span>

### <span data-ttu-id="3ec9d-110">Пример 1. Удаление плана службы приложений</span><span class="sxs-lookup"><span data-stu-id="3ec9d-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="3ec9d-111">Эта команда удаляет план службы приложений Azure ContosoASP, принадлежащий группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="3ec9d-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="3ec9d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ec9d-112">PARAMETERS</span></span>

### <span data-ttu-id="3ec9d-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3ec9d-113">-AppServicePlan</span></span>
<span data-ttu-id="3ec9d-114">Объект плана обслуживания приложения</span><span class="sxs-lookup"><span data-stu-id="3ec9d-114">App Service Plan Object</span></span>

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

### <span data-ttu-id="3ec9d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ec9d-115">-AsJob</span></span>
<span data-ttu-id="3ec9d-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3ec9d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3ec9d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ec9d-117">-DefaultProfile</span></span>
<span data-ttu-id="3ec9d-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3ec9d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ec9d-119">-Force</span><span class="sxs-lookup"><span data-stu-id="3ec9d-119">-Force</span></span>
<span data-ttu-id="3ec9d-120">Параметр "Принудительно удалить"</span><span class="sxs-lookup"><span data-stu-id="3ec9d-120">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="3ec9d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3ec9d-121">-Name</span></span>
<span data-ttu-id="3ec9d-122">Название плана службы приложений</span><span class="sxs-lookup"><span data-stu-id="3ec9d-122">App Service Plan Name</span></span>

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

### <span data-ttu-id="3ec9d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ec9d-123">-ResourceGroupName</span></span>
<span data-ttu-id="3ec9d-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3ec9d-124">Resource Group Name</span></span>

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

### <span data-ttu-id="3ec9d-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ec9d-125">-Confirm</span></span>
<span data-ttu-id="3ec9d-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ec9d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ec9d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ec9d-127">-WhatIf</span></span>
<span data-ttu-id="3ec9d-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ec9d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ec9d-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3ec9d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ec9d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ec9d-130">CommonParameters</span></span>
<span data-ttu-id="3ec9d-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ec9d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ec9d-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ec9d-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ec9d-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3ec9d-133">INPUTS</span></span>

### <span data-ttu-id="3ec9d-134">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3ec9d-134">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="3ec9d-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3ec9d-135">OUTPUTS</span></span>

### <span data-ttu-id="3ec9d-136">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3ec9d-136">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="3ec9d-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3ec9d-137">NOTES</span></span>

## <span data-ttu-id="3ec9d-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3ec9d-138">RELATED LINKS</span></span>

[<span data-ttu-id="3ec9d-139">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3ec9d-139">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="3ec9d-140">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3ec9d-140">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="3ec9d-141">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3ec9d-141">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


