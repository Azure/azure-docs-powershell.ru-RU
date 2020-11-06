---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
ms.openlocfilehash: b97506b8f104859c54c55ee1a937916623f4201d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558116"
---
# <span data-ttu-id="9b1cc-101">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9b1cc-101">Remove-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="9b1cc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9b1cc-102">SYNOPSIS</span></span>
<span data-ttu-id="9b1cc-103">Удаляет план служб приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="9b1cc-103">Removes an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b1cc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9b1cc-104">SYNTAX</span></span>

### <span data-ttu-id="9b1cc-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="9b1cc-105">S1</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b1cc-106">S2</span><span class="sxs-lookup"><span data-stu-id="9b1cc-106">S2</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-AsJob] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b1cc-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b1cc-107">DESCRIPTION</span></span>
<span data-ttu-id="9b1cc-108">Командлет **Remove-AzureRmAppServicePlan** удаляет план служб приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="9b1cc-108">The **Remove-AzureRmAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="9b1cc-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9b1cc-109">EXAMPLES</span></span>

### <span data-ttu-id="9b1cc-110">Пример 1: Удаление плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="9b1cc-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="9b1cc-111">Эта команда удаляет план служб приложений для Azure с именем ContosoASP, который входит в группу ресурсов с именем Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="9b1cc-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="9b1cc-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9b1cc-112">PARAMETERS</span></span>

### <span data-ttu-id="9b1cc-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9b1cc-113">-AppServicePlan</span></span>
<span data-ttu-id="9b1cc-114">Объект плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="9b1cc-114">App Service Plan Object</span></span>

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

### <span data-ttu-id="9b1cc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b1cc-115">-AsJob</span></span>
<span data-ttu-id="9b1cc-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9b1cc-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9b1cc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b1cc-117">-DefaultProfile</span></span>
<span data-ttu-id="9b1cc-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9b1cc-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b1cc-119">-Force</span><span class="sxs-lookup"><span data-stu-id="9b1cc-119">-Force</span></span>
<span data-ttu-id="9b1cc-120">Параметр принудительного удаления</span><span class="sxs-lookup"><span data-stu-id="9b1cc-120">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="9b1cc-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9b1cc-121">-Name</span></span>
<span data-ttu-id="9b1cc-122">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="9b1cc-122">App Service Plan Name</span></span>

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

### <span data-ttu-id="9b1cc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b1cc-123">-ResourceGroupName</span></span>
<span data-ttu-id="9b1cc-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="9b1cc-124">Resource Group Name</span></span>

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

### <span data-ttu-id="9b1cc-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b1cc-125">-Confirm</span></span>
<span data-ttu-id="9b1cc-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9b1cc-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b1cc-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b1cc-127">-WhatIf</span></span>
<span data-ttu-id="9b1cc-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9b1cc-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b1cc-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9b1cc-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b1cc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b1cc-130">CommonParameters</span></span>
<span data-ttu-id="9b1cc-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9b1cc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b1cc-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b1cc-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b1cc-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9b1cc-133">INPUTS</span></span>

### <span data-ttu-id="9b1cc-134">Microsoft. Azure. Management. website. Models. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9b1cc-134">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>
<span data-ttu-id="9b1cc-135">Параметры: AppServicePlan (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9b1cc-135">Parameters: AppServicePlan (ByValue)</span></span>

## <span data-ttu-id="9b1cc-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b1cc-136">OUTPUTS</span></span>

### <span data-ttu-id="9b1cc-137">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9b1cc-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="9b1cc-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="9b1cc-138">NOTES</span></span>

## <span data-ttu-id="9b1cc-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9b1cc-139">RELATED LINKS</span></span>

[<span data-ttu-id="9b1cc-140">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9b1cc-140">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="9b1cc-141">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9b1cc-141">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="9b1cc-142">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9b1cc-142">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


