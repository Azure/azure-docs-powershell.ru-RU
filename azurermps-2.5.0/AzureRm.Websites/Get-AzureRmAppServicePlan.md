---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermappserviceplan
schema: 2.0.0
ms.openlocfilehash: b85d22d1030eaa12e58cded1c7225231c7e8b964
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913537"
---
# <span data-ttu-id="3ab6f-101">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3ab6f-101">Get-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="3ab6f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3ab6f-102">SYNOPSIS</span></span>
<span data-ttu-id="3ab6f-103">Получает план служб приложений Azure в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3ab6f-103">Gets an Azure App Service plan in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ab6f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3ab6f-104">SYNTAX</span></span>

### <span data-ttu-id="3ab6f-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="3ab6f-105">S1</span></span>
```
Get-AzureRmAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ab6f-106">S2</span><span class="sxs-lookup"><span data-stu-id="3ab6f-106">S2</span></span>
```
Get-AzureRmAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ab6f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ab6f-107">DESCRIPTION</span></span>
<span data-ttu-id="3ab6f-108">Командлет **Get-AzureRmAppServicePlan** получает план служб приложений Azure в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3ab6f-108">The **Get-AzureRmAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="3ab6f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3ab6f-109">EXAMPLES</span></span>

### <span data-ttu-id="3ab6f-110">Пример 1: получение плана служб приложений из группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3ab6f-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="3ab6f-111">Эта команда получает план служб приложений с именем ContosoASP, который принадлежит группе ресурсов с именем Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="3ab6f-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="3ab6f-112">Пример 2: получение всех планов служб приложений в местоположении</span><span class="sxs-lookup"><span data-stu-id="3ab6f-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzureRmAppServicePlan -Location "West US"
```

<span data-ttu-id="3ab6f-113">Эта команда получает все планы служб приложений, которые находятся в регионе "Западная часть США".</span><span class="sxs-lookup"><span data-stu-id="3ab6f-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="3ab6f-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3ab6f-114">PARAMETERS</span></span>

### <span data-ttu-id="3ab6f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ab6f-115">-DefaultProfile</span></span>
<span data-ttu-id="3ab6f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3ab6f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ab6f-117">-Location</span><span class="sxs-lookup"><span data-stu-id="3ab6f-117">-Location</span></span>
<span data-ttu-id="3ab6f-118">Поиска</span><span class="sxs-lookup"><span data-stu-id="3ab6f-118">Location</span></span> 

```yaml
Type: String
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ab6f-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3ab6f-119">-Name</span></span>
<span data-ttu-id="3ab6f-120">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="3ab6f-120">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ab6f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ab6f-121">-ResourceGroupName</span></span>
<span data-ttu-id="3ab6f-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3ab6f-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ab6f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ab6f-123">CommonParameters</span></span>
<span data-ttu-id="3ab6f-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3ab6f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ab6f-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ab6f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ab6f-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3ab6f-126">INPUTS</span></span>

### <span data-ttu-id="3ab6f-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="3ab6f-127">None</span></span>
<span data-ttu-id="3ab6f-128">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="3ab6f-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3ab6f-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ab6f-129">OUTPUTS</span></span>

### <span data-ttu-id="3ab6f-130">Microsoft. Azure. Management. website. Models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="3ab6f-130">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

### <span data-ttu-id="3ab6f-131">Microsoft. Azure. Management. website. Models. ServerFarmCollection</span><span class="sxs-lookup"><span data-stu-id="3ab6f-131">Microsoft.Azure.Management.WebSites.Models.ServerFarmCollection</span></span>

## <span data-ttu-id="3ab6f-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="3ab6f-132">NOTES</span></span>

## <span data-ttu-id="3ab6f-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3ab6f-133">RELATED LINKS</span></span>

[<span data-ttu-id="3ab6f-134">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3ab6f-134">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="3ab6f-135">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3ab6f-135">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="3ab6f-136">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3ab6f-136">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


