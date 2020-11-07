---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/remove-Azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzAppServicePlan.md
ms.openlocfilehash: 3d0e3ad30df71700eb83938181ed86a97a77528a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910588"
---
# <span data-ttu-id="ff37c-101">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ff37c-101">Remove-AzAppServicePlan</span></span>

## <span data-ttu-id="ff37c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ff37c-102">SYNOPSIS</span></span>
<span data-ttu-id="ff37c-103">Удаляет план служб приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="ff37c-103">Removes an Azure App Service plan.</span></span>

## <span data-ttu-id="ff37c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ff37c-104">SYNTAX</span></span>

### <span data-ttu-id="ff37c-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="ff37c-105">S1</span></span>
```
Remove-AzAppServicePlan [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff37c-106">S2</span><span class="sxs-lookup"><span data-stu-id="ff37c-106">S2</span></span>
```
Remove-AzAppServicePlan [-Force] [-AppServicePlan] <AppServicePlan> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff37c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff37c-107">DESCRIPTION</span></span>
<span data-ttu-id="ff37c-108">Командлет **Remove-AzAppServicePlan** удаляет план служб приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="ff37c-108">The **Remove-AzAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="ff37c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ff37c-109">EXAMPLES</span></span>

### <span data-ttu-id="ff37c-110">Пример 1: Удаление плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="ff37c-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="ff37c-111">Эта команда удаляет план служб приложений для Azure с именем ContosoASP, который входит в группу ресурсов с именем Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="ff37c-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="ff37c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ff37c-112">PARAMETERS</span></span>

### <span data-ttu-id="ff37c-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ff37c-113">-AppServicePlan</span></span>
<span data-ttu-id="ff37c-114">Объект плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="ff37c-114">App Service Plan Object</span></span>

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

### <span data-ttu-id="ff37c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff37c-115">-DefaultProfile</span></span>
<span data-ttu-id="ff37c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ff37c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff37c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ff37c-117">-Force</span></span>
<span data-ttu-id="ff37c-118">Параметр принудительного удаления</span><span class="sxs-lookup"><span data-stu-id="ff37c-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="ff37c-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ff37c-119">-Name</span></span>
<span data-ttu-id="ff37c-120">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="ff37c-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="ff37c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff37c-121">-ResourceGroupName</span></span>
<span data-ttu-id="ff37c-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ff37c-122">Resource Group Name</span></span>

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

### <span data-ttu-id="ff37c-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ff37c-123">-Confirm</span></span>
<span data-ttu-id="ff37c-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ff37c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff37c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff37c-125">-WhatIf</span></span>
<span data-ttu-id="ff37c-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ff37c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff37c-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ff37c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff37c-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ff37c-128">-AsJob</span></span>
<span data-ttu-id="ff37c-129">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ff37c-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ff37c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff37c-130">CommonParameters</span></span>
<span data-ttu-id="ff37c-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ff37c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff37c-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff37c-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff37c-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ff37c-133">INPUTS</span></span>

### <span data-ttu-id="ff37c-134">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="ff37c-134">ServerFarmWithRichSku</span></span>
<span data-ttu-id="ff37c-135">Параметр "AppServicePlan" принимает значение типа "ServerFarmWithRichSku" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="ff37c-135">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="ff37c-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff37c-136">OUTPUTS</span></span>

### <span data-ttu-id="ff37c-137">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ff37c-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="ff37c-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="ff37c-138">NOTES</span></span>

## <span data-ttu-id="ff37c-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ff37c-139">RELATED LINKS</span></span>

[<span data-ttu-id="ff37c-140">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ff37c-140">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="ff37c-141">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ff37c-141">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="ff37c-142">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ff37c-142">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


