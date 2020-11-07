---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
ms.openlocfilehash: 064ccbcfa94137f5221a5d08e0a06e09328e0b1f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907661"
---
# <span data-ttu-id="cf2c5-101">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="cf2c5-101">Get-AzAppServicePlan</span></span>

## <span data-ttu-id="cf2c5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cf2c5-102">SYNOPSIS</span></span>
<span data-ttu-id="cf2c5-103">Получает план служб приложений Azure в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cf2c5-103">Gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="cf2c5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cf2c5-104">SYNTAX</span></span>

### <span data-ttu-id="cf2c5-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="cf2c5-105">S1</span></span>
```
Get-AzAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf2c5-106">S2</span><span class="sxs-lookup"><span data-stu-id="cf2c5-106">S2</span></span>
```
Get-AzAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf2c5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf2c5-107">DESCRIPTION</span></span>
<span data-ttu-id="cf2c5-108">Командлет **Get-AzAppServicePlan** получает план служб приложений Azure в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cf2c5-108">The **Get-AzAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="cf2c5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cf2c5-109">EXAMPLES</span></span>

### <span data-ttu-id="cf2c5-110">Пример 1: получение плана служб приложений из группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="cf2c5-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="cf2c5-111">Эта команда получает план служб приложений с именем ContosoASP, который принадлежит группе ресурсов с именем Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="cf2c5-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="cf2c5-112">Пример 2: получение всех планов служб приложений в местоположении</span><span class="sxs-lookup"><span data-stu-id="cf2c5-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzAppServicePlan -Location "West US"
```

<span data-ttu-id="cf2c5-113">Эта команда получает все планы служб приложений, которые находятся в регионе "Западная часть США".</span><span class="sxs-lookup"><span data-stu-id="cf2c5-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="cf2c5-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cf2c5-114">PARAMETERS</span></span>

### <span data-ttu-id="cf2c5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf2c5-115">-DefaultProfile</span></span>
<span data-ttu-id="cf2c5-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cf2c5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf2c5-117">-Location</span><span class="sxs-lookup"><span data-stu-id="cf2c5-117">-Location</span></span>
<span data-ttu-id="cf2c5-118">Поиска</span><span class="sxs-lookup"><span data-stu-id="cf2c5-118">Location</span></span> 

```yaml
Type: System.String
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf2c5-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cf2c5-119">-Name</span></span>
<span data-ttu-id="cf2c5-120">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="cf2c5-120">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf2c5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf2c5-121">-ResourceGroupName</span></span>
<span data-ttu-id="cf2c5-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="cf2c5-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf2c5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf2c5-123">CommonParameters</span></span>
<span data-ttu-id="cf2c5-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cf2c5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf2c5-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf2c5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf2c5-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cf2c5-126">INPUTS</span></span>

### <span data-ttu-id="cf2c5-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="cf2c5-127">None</span></span>

## <span data-ttu-id="cf2c5-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf2c5-128">OUTPUTS</span></span>

### <span data-ttu-id="cf2c5-129">Microsoft. Azure. Commands. Apps. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="cf2c5-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="cf2c5-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="cf2c5-130">NOTES</span></span>

## <span data-ttu-id="cf2c5-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf2c5-131">RELATED LINKS</span></span>

[<span data-ttu-id="cf2c5-132">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="cf2c5-132">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="cf2c5-133">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="cf2c5-133">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="cf2c5-134">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="cf2c5-134">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


