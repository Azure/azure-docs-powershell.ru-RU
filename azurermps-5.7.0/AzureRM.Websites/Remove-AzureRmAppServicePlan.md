---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
ms.openlocfilehash: d5164e47dd759538fea6f0ab143ef9640055f1c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561300"
---
# <span data-ttu-id="d5114-101">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d5114-101">Remove-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="d5114-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d5114-102">SYNOPSIS</span></span>
<span data-ttu-id="d5114-103">Удаляет план служб приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="d5114-103">Removes an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5114-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d5114-104">SYNTAX</span></span>

### <span data-ttu-id="d5114-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="d5114-105">S1</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5114-106">S2</span><span class="sxs-lookup"><span data-stu-id="d5114-106">S2</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-AppServicePlan] <ServerFarmWithRichSku> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5114-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5114-107">DESCRIPTION</span></span>
<span data-ttu-id="d5114-108">Командлет **Remove-AzureRmAppServicePlan** удаляет план служб приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="d5114-108">The **Remove-AzureRmAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="d5114-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d5114-109">EXAMPLES</span></span>

### <span data-ttu-id="d5114-110">Пример 1: Удаление плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="d5114-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="d5114-111">Эта команда удаляет план служб приложений для Azure с именем ContosoASP, который входит в группу ресурсов с именем Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="d5114-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="d5114-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d5114-112">PARAMETERS</span></span>

### <span data-ttu-id="d5114-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d5114-113">-AppServicePlan</span></span>
<span data-ttu-id="d5114-114">Объект плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="d5114-114">App Service Plan Object</span></span>

```yaml
Type: ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5114-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5114-115">-DefaultProfile</span></span>
<span data-ttu-id="d5114-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d5114-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5114-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d5114-117">-Force</span></span>
<span data-ttu-id="d5114-118">Параметр принудительного удаления</span><span class="sxs-lookup"><span data-stu-id="d5114-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="d5114-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d5114-119">-Name</span></span>
<span data-ttu-id="d5114-120">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="d5114-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="d5114-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5114-121">-ResourceGroupName</span></span>
<span data-ttu-id="d5114-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d5114-122">Resource Group Name</span></span>

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

### <span data-ttu-id="d5114-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d5114-123">-Confirm</span></span>
<span data-ttu-id="d5114-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d5114-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5114-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5114-125">-WhatIf</span></span>
<span data-ttu-id="d5114-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d5114-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5114-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d5114-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5114-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d5114-128">-AsJob</span></span>
<span data-ttu-id="d5114-129">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d5114-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d5114-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5114-130">CommonParameters</span></span>
<span data-ttu-id="d5114-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d5114-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5114-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5114-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5114-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d5114-133">INPUTS</span></span>

### <span data-ttu-id="d5114-134">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="d5114-134">ServerFarmWithRichSku</span></span>
<span data-ttu-id="d5114-135">Параметр "AppServicePlan" принимает значение типа "ServerFarmWithRichSku" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="d5114-135">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="d5114-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5114-136">OUTPUTS</span></span>

### <span data-ttu-id="d5114-137">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d5114-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="d5114-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="d5114-138">NOTES</span></span>

## <span data-ttu-id="d5114-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d5114-139">RELATED LINKS</span></span>

[<span data-ttu-id="d5114-140">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d5114-140">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="d5114-141">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d5114-141">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="d5114-142">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d5114-142">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


