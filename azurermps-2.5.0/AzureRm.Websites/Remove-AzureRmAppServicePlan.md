---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermappserviceplan
schema: 2.0.0
ms.openlocfilehash: e8ce0397a59a72e2960a8e0af978c1b5484c53af
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913258"
---
# <span data-ttu-id="b70cc-101">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b70cc-101">Remove-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="b70cc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b70cc-102">SYNOPSIS</span></span>
<span data-ttu-id="b70cc-103">Удаляет план служб приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="b70cc-103">Removes an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b70cc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b70cc-104">SYNTAX</span></span>

### <span data-ttu-id="b70cc-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="b70cc-105">S1</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b70cc-106">S2</span><span class="sxs-lookup"><span data-stu-id="b70cc-106">S2</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-AppServicePlan] <AppServicePlan> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b70cc-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b70cc-107">DESCRIPTION</span></span>
<span data-ttu-id="b70cc-108">Командлет **Remove-AzureRmAppServicePlan** удаляет план служб приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="b70cc-108">The **Remove-AzureRmAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="b70cc-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b70cc-109">EXAMPLES</span></span>

### <span data-ttu-id="b70cc-110">Пример 1: Удаление плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="b70cc-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="b70cc-111">Эта команда удаляет план служб приложений для Azure с именем ContosoASP, который входит в группу ресурсов с именем Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="b70cc-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="b70cc-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b70cc-112">PARAMETERS</span></span>

### <span data-ttu-id="b70cc-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b70cc-113">-AppServicePlan</span></span>
<span data-ttu-id="b70cc-114">Объект плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="b70cc-114">App Service Plan Object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b70cc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b70cc-115">-DefaultProfile</span></span>
<span data-ttu-id="b70cc-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b70cc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b70cc-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b70cc-117">-Force</span></span>
<span data-ttu-id="b70cc-118">Параметр принудительного удаления</span><span class="sxs-lookup"><span data-stu-id="b70cc-118">Forcefully Remove Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b70cc-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b70cc-119">-Name</span></span>
<span data-ttu-id="b70cc-120">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="b70cc-120">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b70cc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b70cc-121">-ResourceGroupName</span></span>
<span data-ttu-id="b70cc-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="b70cc-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b70cc-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b70cc-123">-Confirm</span></span>
<span data-ttu-id="b70cc-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b70cc-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b70cc-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b70cc-125">-WhatIf</span></span>
<span data-ttu-id="b70cc-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b70cc-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b70cc-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b70cc-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b70cc-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b70cc-128">-AsJob</span></span>
<span data-ttu-id="b70cc-129">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b70cc-129">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b70cc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b70cc-130">CommonParameters</span></span>
<span data-ttu-id="b70cc-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b70cc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b70cc-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b70cc-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b70cc-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b70cc-133">INPUTS</span></span>

### <span data-ttu-id="b70cc-134">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="b70cc-134">ServerFarmWithRichSku</span></span>
<span data-ttu-id="b70cc-135">Параметр "AppServicePlan" принимает значение типа "ServerFarmWithRichSku" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="b70cc-135">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="b70cc-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b70cc-136">OUTPUTS</span></span>

### <span data-ttu-id="b70cc-137">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b70cc-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="b70cc-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="b70cc-138">NOTES</span></span>

## <span data-ttu-id="b70cc-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b70cc-139">RELATED LINKS</span></span>

[<span data-ttu-id="b70cc-140">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b70cc-140">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="b70cc-141">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b70cc-141">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="b70cc-142">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b70cc-142">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


