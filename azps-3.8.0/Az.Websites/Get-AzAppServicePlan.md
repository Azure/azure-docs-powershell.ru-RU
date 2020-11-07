---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
ms.openlocfilehash: afbee0d6b13c1ce42931a2379cff6aa7ee0127b9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912114"
---
# <span data-ttu-id="e4e6a-101">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e4e6a-101">Get-AzAppServicePlan</span></span>

## <span data-ttu-id="e4e6a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e4e6a-102">SYNOPSIS</span></span>
<span data-ttu-id="e4e6a-103">Получает план служб приложений Azure в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e4e6a-103">Gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="e4e6a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e4e6a-104">SYNTAX</span></span>

### <span data-ttu-id="e4e6a-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="e4e6a-105">S1</span></span>
```
Get-AzAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4e6a-106">S2</span><span class="sxs-lookup"><span data-stu-id="e4e6a-106">S2</span></span>
```
Get-AzAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4e6a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4e6a-107">DESCRIPTION</span></span>
<span data-ttu-id="e4e6a-108">Командлет **Get-AzAppServicePlan** получает план служб приложений Azure в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e4e6a-108">The **Get-AzAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="e4e6a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e4e6a-109">EXAMPLES</span></span>

### <span data-ttu-id="e4e6a-110">Пример 1: получение плана служб приложений из группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e4e6a-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="e4e6a-111">Эта команда получает план служб приложений с именем ContosoASP, который принадлежит группе ресурсов с именем Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="e4e6a-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="e4e6a-112">Пример 2: получение всех планов служб приложений в местоположении</span><span class="sxs-lookup"><span data-stu-id="e4e6a-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzAppServicePlan -Location "West US"
```

<span data-ttu-id="e4e6a-113">Эта команда получает все планы служб приложений, которые находятся в регионе "Западная часть США".</span><span class="sxs-lookup"><span data-stu-id="e4e6a-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="e4e6a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e4e6a-114">PARAMETERS</span></span>

### <span data-ttu-id="e4e6a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4e6a-115">-DefaultProfile</span></span>
<span data-ttu-id="e4e6a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e4e6a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4e6a-117">-Location</span><span class="sxs-lookup"><span data-stu-id="e4e6a-117">-Location</span></span>
<span data-ttu-id="e4e6a-118">Поиска</span><span class="sxs-lookup"><span data-stu-id="e4e6a-118">Location</span></span> 

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

### <span data-ttu-id="e4e6a-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e4e6a-119">-Name</span></span>
<span data-ttu-id="e4e6a-120">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="e4e6a-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="e4e6a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4e6a-121">-ResourceGroupName</span></span>
<span data-ttu-id="e4e6a-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e4e6a-122">Resource Group Name</span></span>

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

### <span data-ttu-id="e4e6a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4e6a-123">CommonParameters</span></span>
<span data-ttu-id="e4e6a-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e4e6a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4e6a-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4e6a-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4e6a-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e4e6a-126">INPUTS</span></span>

### <span data-ttu-id="e4e6a-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="e4e6a-127">None</span></span>

## <span data-ttu-id="e4e6a-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4e6a-128">OUTPUTS</span></span>

### <span data-ttu-id="e4e6a-129">Microsoft. Azure. Commands. Apps. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e4e6a-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="e4e6a-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="e4e6a-130">NOTES</span></span>

## <span data-ttu-id="e4e6a-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e4e6a-131">RELATED LINKS</span></span>

[<span data-ttu-id="e4e6a-132">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e4e6a-132">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="e4e6a-133">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e4e6a-133">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="e4e6a-134">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e4e6a-134">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


